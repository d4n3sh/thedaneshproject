---
title: How to list mounted volumes in TSM
author: Danesh
date: 2013-10-28T15:33:55+00:00
dsq_thread_id:
  - 1910842490

---
Use this command to display information about the status of one or more volumes that are mounted.

From the Administrative Command Line Client (dsmadmc) run,

`"query mount" or "q mount"<br />
`  
and for detailed output run,

`"query mount format=detailed" or "q mount f=d"`

`Syntax</p>
<p>                .-*-----------.  .-Format--=--Standard-----.<br />
>>-Query MOunt--+-------------+--+-------------------------+---><
                '-volume_name-'  '-Format--=--+-Standard-+-'
                                              '-Detailed-'
`