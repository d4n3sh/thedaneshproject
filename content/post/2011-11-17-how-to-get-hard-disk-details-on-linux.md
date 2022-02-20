---
title: How to get Hard Disk Details on Linux
author: Danesh
date: 2011-11-16T17:27:51+00:00
url: /posts/how-to-get-hard-disk-details-on-linux/
pvc_views:
  - 6405
dsq_thread_id:
  - 889866145

---
Here&#8217;s a quick way to find out more about your hard disk. You can get the serial number, part number, firmware level, size and much more. Just see the sample below.  
hdparm -I [device]  
`hdparm -I /dev/sda`  
`[danesh@pandora Movies]$ sudo hdparm -I /dev/sda`

`/dev/sda:<br />
ATA device, with non-removable media<br />
Model Number: WDC WD2500JS-75NCB3<br />
Serial Number: WD-WCANKF265386<br />
Firmware Revision: 10.02E04<br />
Standards:<br />
Supported: 7 6 5 4<br />
Likely used: 8<br />
Configuration:<br />
Logical max current<br />
cylinders 16383 16383<br />
heads 16 16<br />
sectors/track 63 63<br />
--<br />
CHS current addressable sectors: 16514064<br />
LBA user addressable sectors: 268435455<br />
LBA48 user addressable sectors: 488281250<br />
Logical/Physical Sector size: 512 bytes<br />
device size with M = 1024*1024: 238418 MBytes<br />
device size with M = 1000*1000: 250000 MBytes (250 GB)<br />
cache/buffer size = 8192 KBytes<br />
Capabilities:<br />
LBA, IORDY(can be disabled)<br />
Queue depth: 32<br />
Standby timer values: spec'd by Standard, with device specific minimum<br />
R/W multiple sector transfer: Max = 16 Current = 16<br />
Recommended acoustic management value: 128, current value: 128<br />
DMA: mdma0 mdma1 mdma2 udma0 udma1 udma2 udma3 udma4 udma5 *udma6<br />
Cycle time: min=120ns recommended=120ns<br />
PIO: pio0 pio1 pio2 pio3 pio4<br />
Cycle time: no flow control=120ns IORDY flow control=120ns<br />
Commands/features:<br />
Enabled Supported:<br />
* SMART feature set<br />
Security Mode feature set<br />
* Power Management feature set<br />
* Write cache<br />
* Look-ahead<br />
* Host Protected Area feature set<br />
* WRITE_BUFFER command<br />
* READ_BUFFER command<br />
* NOP cmd<br />
* DOWNLOAD_MICROCODE<br />
Power-Up In Standby feature set<br />
* SET_FEATURES required to spinup after power up<br />
SET_MAX security extension<br />
* Automatic Acoustic Management feature set<br />
* 48-bit Address feature set<br />
* Device Configuration Overlay feature set<br />
* Mandatory FLUSH_CACHE<br />
* FLUSH_CACHE_EXT<br />
* SMART error logging<br />
* SMART self-test<br />
* General Purpose Logging feature set<br />
* Gen1 signaling speed (1.5Gb/s)<br />
* Gen2 signaling speed (3.0Gb/s)<br />
* Native Command Queueing (NCQ)<br />
* Host-initiated interface power management<br />
* Phy event counters<br />
DMA Setup Auto-Activate optimization<br />
Device-initiated interface power management<br />
* Software settings preservation<br />
* SMART Command Transport (SCT) feature set<br />
* SCT Long Sector Access (AC1)<br />
* SCT LBA Segment Access (AC2)<br />
* SCT Error Recovery Control (AC3)<br />
* SCT Features Control (AC4)<br />
* SCT Data Tables (AC5)<br />
unknown 206[12] (vendor specific)<br />
Security:<br />
Master password revision code = 65534<br />
supported<br />
not enabled<br />
not locked<br />
frozen<br />
not expired: security count<br />
not supported: enhanced erase<br />
Checksum: correct<br />
`  
Hope it comes in handy for you. Know a better way? Please share