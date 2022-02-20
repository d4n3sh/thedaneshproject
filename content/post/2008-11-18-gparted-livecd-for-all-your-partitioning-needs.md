---
title: GParted LiveCD for all your partitioning needs
author: Danesh
date: 2008-11-18T19:12:07+00:00
url: /posts/gparted-livecd-for-all-your-partitioning-needs/
robotsmeta:
  - index,follow
pvc_views:
  - 2835
dsq_thread_id:
  - 916392951

---
A friend needed to re-size his Windows NT OS partition from the default 4GB to 8GB. The easiest way to do this is with Linux, specifically with the GParted LiveCD.

[<img loading="lazy" src="http://farm4.static.flickr.com/3164/3039583419_995d3556d8.jpg" alt="gparted_screenshot" width="500" height="337" />][1]

GParted is a Gnome based partition editor which uses the libparted library from the popular [GNU Parted][2] package to do all it&#8217;s fancy partitioning stuff.

Current supported file systems are ext2, ext3, fat16, fat32, hfs, hfs+, jfs, linux-swap, ntfs, reiser-4, reiserfs, ufs and xfs. GParted lets you detect, read, create, grow, shrink, move ,copy, check and label your partitions. However, not all the features will work across all file systems. See table below.

[<img loading="lazy" src="http://farm4.static.flickr.com/3290/3040422382_65d832b70e_o.jpg" alt="gparted_features" width="400" height="426" />][3]

Where to get the LiveCD? [SourgeForge of course!][4]

Source: [GParted][5]

 [1]: http://www.flickr.com/photos/dannyportal/3039583419/ "gparted_screenshot by Danesh Manoharan, on Flickr"
 [2]: http://www.gnu.org/software/parted/index.shtml
 [3]: http://www.flickr.com/photos/dannyportal/3040422382/ "gparted_features by Danesh Manoharan, on Flickr"
 [4]: http://sourceforge.net/project/showfiles.php?group_id=115843&package_id=271779
 [5]: http://gparted.sourceforge.net/index.php