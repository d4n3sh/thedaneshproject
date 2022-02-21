---
title: Running previous commands in Linux
author: Danesh
date: 2007-10-17T16:38:53+00:00
pvc_views:
  - 14300
dsq_thread_id:
  - 889736617

---
Most non linux people tend to be taunted by the Linux command line, it&#8217;s no beast nor is the user behind it a super geek just because you see him hammering away at the keyboard with lines after lines of commands. Chances are he is repeating commands or changing commands here and there to get some results. In Linux the first time takes time and practice to produce accurate results. This is what most sysadmins spend their time doing but once you get the hang of it, it became a walk in the park.

How often do you repeat commands while using the command line? I do this all the time but sometimes it&#8217;s good to learn some shortcuts now and then to reduce repetitive tasks and improve efficiency.

When you type a command in the command line, it&#8217;s saved into the .bash_history file within the home directory. The history file will hold the last 500 commands. To view them you can use &#8220;**_history_**&#8221; or &#8220;_**history | less**_&#8221; if the result is too long. The history file is also frequently use for user/security audits and RCA work.

You will that within the output below each line is numbered, these numbers will come in handy later in this tutorial.

    danny@python:~> history
    1  uname -r
    2  man mount
    3  PS -EF
    4  ps -ef
    5  ps -ef | grep kopete
    6  kill -9 22632
    7  /sbin/ifconfig
    8  ping google.com
    9  ping 192.168.0.1

If you want to execute the last command you typed in again you would normally have to scroll up with the arrow key but this can also be done with &#8220;_**!!**_&#8220;. See sample below.

    danny@python:~> ls -l
    total 40
    drwxr-xr-x 2 danny users 4096 2007-10-11 13:16 bin
    drwxr-xr-x 4 danny users 4096 2007-10-11 16:11 deluge
    drwx------ 4 danny users 4096 2007-10-17 22:38 Desktop
    drwx------ 2 danny users 4096 2007-10-11 13:16 Documents
    drwxr-xr-x 2 danny users 4096 2007-10-11 13:16 public_html
    danny@python:~> !!
    ls -l
    total 40
    drwxr-xr-x 2 danny users 4096 2007-10-11 13:16 bin
    drwxr-xr-x 4 danny users 4096 2007-10-11 16:11 deluge
    drwx------ 4 danny users 4096 2007-10-17 22:38 Desktop
    drwx------ 2 danny users 4096 2007-10-11 13:16 Documents
    drwxr-xr-x 2 danny users 4096 2007-10-11 13:16 public_html

You could also execute a command from the history file by referring to the corresponding line number by using &#8220;_**![##]**_&#8220;. See sample below.

    danny@python:~> history
    1  ls -l
    2  ls -la
    3  history
    4  cd /
    5  cd -
    6  cd /nfs
    7  cd /sto
    8  ls
    9  history
    danny@python:~> !3
    history
    1  ls -l
    2  ls -la
    3  history
    4  cd /
    5  cd -
    6  cd /nfs
    7  cd /sto
    8  ls
    9  history
    10  history

Using a string in place of the line number is also possible. The syntax for this is &#8220;_**![string]**_&#8220;. See sample below. The string value is matched against entries in the .bash_history file and the first matching entry will be excuted. For example if the &#8220;history&#8221; command existed on line 10, 100 and 450, line 450 would be returned.

    danny@python:~> history
    1  ls -l
    2  ls -la
    3  history
    4  cd /
    5  cd -
    6  cd /nfs
    7  cd /sto
    8  ls
    9  history
    10  history
    danny@python:~> !history
    history
    1  ls -l
    2  ls -la
    3  history
    4  cd /
    5  cd -
    6  cd /nfs
    7  cd /sto
    8  ls
    9  history
    10  history

Hope you find this helpful. Drop me a comment if you have questions or comments.