---
title: i3 On Raspberry Pi Desktop OS On Mac
date: 2024-11-30T09:41:31.971Z
---
a﻿ll you need to do after installing i3 is no need to mess around in /etc/xdg/LXDE or whatever.

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

### Switching Between Multiple DEs

2 ways:

\#1 - sudo apt install tasksel

\#2 - run this command:

```
sudo update-alternatives --config x-session-manager
```

### Getting Rofi Working in LXDE with CMD+D

sudo apt install xbindkeys and vim ~/.xbindkeysrc

```
# Launch Rofi drun with Mod+d
"rofi -show drun"
    mod4 + d
```

### R﻿enoise Is Installed But Won't Run

P﻿roblem is this imac is amd64 and its looking packages that are installed but on the wrong architecture. If you are trying to install all required 64-bit dependencies for a particular program (like Renoise) and you don’t want to manually install each package, you can use the following method:

* First, ensure all the required dependencies are identified:

```
ldd $(which renoise)
# then install missing packages
sudo apt install libasound2:amd64 libxext6:amd64 libstdc++6:amd64 pulseaudio:amd64
```