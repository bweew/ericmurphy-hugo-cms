---
title: i3 On Raspberry Pi Desktop OS On Mac
date: 2024-11-30T09:41:31.971Z
---
a﻿ll you need to do after installing i3 is no need to mess around in /etc/xdg/LXDE or whtever

v﻿im ~/.dmrc

```
[Desktop]
# Session=lightdm-xsession
Session=i3

```

A﻿lso for getting renoise setup on this kingston a400 250gb ssd with raspberry pi desktop with persistence you need to add :amd64 to the end of the packages it says it can't find on this imac.

### G﻿ETTING RENOISE TO NOT STUTTER

```
sudo apt install cpufrequtils
sudo cpufreq-set -r -g performance
sudo vim /etc/init.d/cpufrequtils

## change GOVERNOR="ondemand" to
GOVERNOR="performance"

sudo vim /etc/security/limits.conf

#at the end of the file add username (where pi is)
# make sure you change to your username if its not pi!
pi - rtprio 99
pi - nice -10
```