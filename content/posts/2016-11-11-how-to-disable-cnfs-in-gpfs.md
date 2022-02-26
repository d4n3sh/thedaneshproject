---
title: How to disable cnfs in GPFS
author: Danesh Manoharan
date: 2016-11-11T08:44:04+00:00
dsq_thread_id:
  - 5295593831

---
Review your current cnfs setup.

```
mmlscluster --cnfs
```

Delete the nodes returned from the previous command from your cnfs configuration.

```
mmchnode --cnfs-interface=DELETE -N foonsd1,foonsd2
```

Verify cnfs has been disabled.

```
mmlscluster --cnfs
```

 