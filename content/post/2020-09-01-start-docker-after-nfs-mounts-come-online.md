---
title: Start docker after NFS mounts come online
author: Danesh
date: 2020-09-01T02:28:16+00:00
url: /posts/start-docker-after-nfs-mounts-come-online/

---
<div class="wp-block-jetpack-markdown">
  <h2>
    Problem
  </h2>
  
  <p>
    Some of my docker containers access resources from a NAS over NFS.
  </p>
  
  <p>
    On reboot, the Docker service comes up before the NFS paths are mounted, this causes the services within my containers to fail.
  </p>
  
  <p>
    Restating the docker service, <code>systemctl restart docker</code> fixes this but I&#8217;d rather the containers come up properly the first time.
  </p>
  
  <h2>
    Solution
  </h2>
  
  <p>
    Add a systemd drop-in unit for the docker service instructing it to wait for the NFS mount to come online before starting.
  </p>
  
  <h2>
    Steps
  </h2>
  
  <ol>
    <li>
      Identify the systemd unit for the NFS mount. In my case /nas/data .
    </li>
  </ol>
  
  <pre><code>danesh@antman:~$ mount -t nfs4
192.168.100.1:/volume8/data on /nas/data type nfs4 (rw,relatime,vers=4.1,rsize=131072,wsize=131072,namlen=255,hard,proto=tcp,timeo=600,retrans=2,sec=sys,clientaddr=192.168.100.2,local_lock=none,addr=192.168.100.1,_netdev)  

danesh@antman:~$ sudo systemctl list-units | grep nas-data
  nas-data.mount                                                                                                         loaded active mounted   /nas/data  
               
</code></pre>
  
  <ol start="2">
    <li>
      Create the systemd drop-in unit file for the docker service. Create the directory if it is not there.
    </li>
  </ol>
  
  <pre><code>danesh@antman:~$ sudo mkdir /etc/systemd/system/docker.service.d/  

danesh@antman:~$ sudo echo "[Unit]
After=nas-data.mount
Wants=nas-data.mount" &gt;&gt; /etc/systemd/system/docker.service.d/wait-for-nfs.conf

danesh@antman:~$ sudo cat /etc/systemd/system/docker.service.d/wait-for-nfs.conf 
[sudo] password for danesh: 
[Unit]
After=nas-data.mount
Wants=nas-data.mount
</code></pre>
  
  <p>
    <strong>After</strong>: Start after NFS /nas/data is mounted.<br /> <strong>Wants</strong>: If not already mounted, go ahead and mount /nas/data
  </p>
  
  <p>
    If <strong>Wants</strong> is changed to <strong>Requires</strong>, the docker service will not start unless /nas/data is mounted.
  </p>
  
  <ol start="3">
    <li>
      Restart the docker service to verify that the drop-in is picked up.
    </li>
  </ol>
  
  <pre><code>danesh@antman:~$ sudo systemctl restart docker

danesh@antman:~$ sudo systemctl status docker
? docker.service - Docker Application Container Engine
     Loaded: loaded (/lib/systemd/system/docker.service; enabled; vendor preset: enabled)
    Drop-In: /etc/systemd/system/docker.service.d
             ??wait-for-nfs.conf
     Active: active (running) since Mon 2020-08-31 20:45:40 UTC; 5h 21min ago
TriggeredBy: ? docker.socket
</code></pre>
  
  <p>
    If the drop-in is showing then the change will now be persistent across reboots.
  </p>
  
  <h4>
    Sources
  </h4>
  
  <p>
    <a href="https://soichi.us/blog/systemd-tips/">Soichi Hayashi</a><br /> <a href="https://fauxzen.com/docker-issues-with-nfs-mount/">Fauxzen</a><br /> <a href="https://www.freedesktop.org/software/systemd/man/systemd.unit.html">Freedesktop Systemd</a>
  </p>
</div>