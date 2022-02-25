---
title: Improve ALPS touchpad response speed
author: Danesh Manoharan
date: 2008-02-18T10:01:09+00:00
pvc_views:
  - 12491
dsq_thread_id:
  - 890861455

---
ALPS touchpad generaly have slower response when compared to the synaptic based touchpads.

Here's a simple X hack to boost the sensitivity of my ALPS touchpad which has dramatically improved my experience with my touchpad. This worked on my openSUSE 10.3

1. First, check if you really do have a ALPS touchpad.

<pre>cat /proc/bus/input/devices | grep ALPS</pre>

sample output;

<pre>N: Name="AlpsPS/2 ALPS GlidePoint"</pre>

2. Make a backup of your xorg.conf file.

<pre>cp /etc/X11/xorg.conf  /etc/X11/xorg.conf.bkp</pre>

3. Edit the xorg.conf file.

<pre>vi /etc/X11/xorg.conf</pre>

4. Navigate to the InputDevice Section and look for the "synaptics" driver portion.

5. Replace everything between the Identifier line and EndSection with the settings below.  
<!--more-->

<pre>Section "InputDevice"


<pre>   Identifier   "Synaptics Touchpad"
########################################Start replace from here
   Driver       "synaptics"
   Option       "SendCoreEvents"        "true"
   Option       "Device"                "/dev/psaux"
   Option       "Protocol"              "auto-dev"

   Option       "LeftEdge"              "130"
   Option       "RightEdge"             "840"
   Option       "TopEdge"               "130"
   Option       "BottomEdge"            "640"
   Option       "FingerLow"             "14"
   Option       "FingerHigh"            "15"
   Option       "MaxTapTime"            "180"
   Option       "MaxTapMove"            "110"
   Option       "ClickTime"             "0"
   Option       "MaxDoubleTapTime"      "100"
   Option       "EmulateMidButtonTime"  "75"
   Option       "VertScrollDelta"       "20"
   Option       "HorizScrollDelta"      "20"
   Option       "MinSpeed"              "0.60"
   Option       "MaxSpeed"              "1.10"
   Option       "AccelFactor"           "0.030"
   Option       "EdgeMotionMinSpeed"    "200"
   Option       "EdgeMotionMaxSpeed"    "200
   Option       "UpDownScrolling"       "1"
   Option       "CircularScrolling"     "1"
   Option       "CircScrollDelta"       "0.1"
   Option       "CircScrollTrigger"     "2"
   Option       "SHMConfig"             "true"
   Option       "Emulate3Buttons"       "on"
########################################End replace here
EndSection</pre>


<p>
  Here's a screenshot of my xorg.conf file.
</p>