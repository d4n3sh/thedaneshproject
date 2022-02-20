---
title: Adding thunderbolt devices in Fedora server 30
author: Danesh
date: 2019-06-29T21:04:52+00:00
url: /posts/adding-thunderbolt-devices-in-fedora-server-30/

---
I recently purchased a thunderbolt 3 to 10GbE adapter ( QNA-T310G1S ) for my homelab NUC ( NUC7i5BNH ) running Fedora server 30.

The network interface was not showing up when I connected the adapter. Some googling later and I figured out what I was not doing.

Thunderbolt devices need to be authorized and added to the thunderbolt device manager before they can be used. This requirement can be changed in the BIOS if desired. 

Here&#8217;s how I added my 10GbE adapter.

Install the thunderbolt device manager.

<pre class="wp-block-code"><code>>_ sudo dnf install bolt</code></pre>

List connected thunderbolt devices. Take note of the UUID.

<pre class="wp-block-code"><code>>_ sudo boltctl list

 ? QNAP Systems, Inc. QNA-T310G1S
   ?? type:          peripheral
   ?? name:          QNA-T310G1S
   ?? vendor:        QNAP Systems, Inc.
   ?? uuid:          00a928e5-0ce2-5600-ffff-ffffffffffff &lt;--
   ?? status:        connected
   ?  ?? domain:     d2030000-0080-7718-a3c6-0d4a5f01a11d
   ?  ?? authflags:  none
   ?? connected:     Sat 29 Jun 2019 08:25:09 PM UTC
   ?? stored:        no</code></pre>

Authorize and add the device to the device database.

<pre class="wp-block-code"><code>>_ sudo boltctl enroll 00a928e5-0ce2-5600-ffff-ffffffffffff

 ? QNAP Systems, Inc. QNA-T310G1S
   ?? type:          peripheral
   ?? name:          QNA-T310G1S
   ?? vendor:        QNAP Systems, Inc.
   ?? uuid:          00a928e5-0ce2-5600-ffff-ffffffffffff
   ?? dbus path:     /org/freedesktop/bolt/devices/00a928e5_0ce2_5600_ffff_ffffffffffff
   ?? status:        authorized  &lt;--
   ?  ?? domain:     d2030000-0080-7718-a3c6-0d4a5f01a11d
   ?  ?? parent:     d2030000-0080-7718-a3c6-0d4a5f01a11d
   ?  ?? syspath:    /sys/devices/pci0000:00/0000:00:1c.0/0000:01:00.0/0000:02:00.0/0000:03:00.0/domain0/0-0/0-1
   ?  ?? authflags:  none
   ?? authorized:    Sat 29 Jun 2019 08:28:26 PM UTC
   ?? connected:     Sat 29 Jun 2019 08:25:09 PM UTC
   ?? stored:        Sat 29 Jun 2019 08:28:26 PM UTC
      ?? policy:     auto
      ?? key:        no</code></pre>

Device should now show up.

<pre class="wp-block-code"><code>>_ dmesg | tail -n5
&#91;26025.134557] atlantic 0000:06:00.0 enp6s0: renamed from eth0
&#91;26027.069740] atlantic: link change old 0 new 10000
&#91;26027.070131] IPv6: ADDRCONF(NETDEV_CHANGE): enp6s0: link becomes ready

>_ ethtool enp6s0
Settings for enp6s0:
        Supported ports: &#91; FIBRE ]
        Supported link modes:   100baseT/Full 
                                1000baseT/Full 
                                10000baseT/Full 
                                2500baseT/Full 
                                5000baseT/Full 
        Supported pause frame use: Symmetric
        Supports auto-negotiation: Yes
        Supported FEC modes: Not reported
        Advertised link modes:  100baseT/Full 
                                1000baseT/Full 
                                10000baseT/Full 
                                2500baseT/Full 
                                5000baseT/Full 
        Advertised pause frame use: Symmetric
        Advertised auto-negotiation: Yes
        Advertised FEC modes: Not reported
        Speed: 10000Mb/s
        Duplex: Full
        Port: FIBRE
        PHYAD: 0
        Transceiver: internal
        Auto-negotiation: on</code></pre>