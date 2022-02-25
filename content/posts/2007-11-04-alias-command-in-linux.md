---
title: Alias command in Linux
author: Danesh
date: 2007-11-04T14:32:34+00:00
pvc_views:
  - 7681
dsq_thread_id:
  - 889737916

---
The alias command is used to create shortcuts to commands. Let's see how it works.

I use the alias command to create shortcuts for commands I use frequently. For example the _**cp**_(copy) and _**mv**_(move) commands, my alias simply adds _**-i**_ to _**cp**_ and _**mv**_ commands causing them to be interactive thus preventing any accidental deletes or file overwrites.

Running the _**alias**_ command will show you all the current aliases available.

> [dummy@macho ~]$ alias  
> alias l.='ls -d .* -color=tty'  
> alias ll='ls -l -color=tty'  
> alias ls='ls -color=tty'  
> alias vi='vim'

_**alias cp='cp -i'**_. This command will ad _**-i**_ to the_ **cp**_(copy) command. Now, every time the _**cp**_ command is executed it will be interactive. No more accidental deletes 🙂

_**alias mv='mv -i'**_. This command will ad _**-i**_ to the _**mv**_(move) command. Now, every time the _**mv**_ command is executed it will be interactive. No more accidental overwrites 🙂

> [dummy@macho ~]$ alias cp='cp -i'  
> [dummy@macho ~]$ alias mv='mv-i'  
> [dummy@macho ~]$ alias  
> alias cp='cp -i'  
> alias l.='ls -d .* -color=tty'  
> alias ll='ls -l -color=tty'  
> alias ls='ls -color=tty'  
> alias mv='mv-i'  
> alias vi='vim'