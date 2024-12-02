---
title: How To Set Up DevuanPi
date: 2024-12-02T09:17:53.328Z
---

The Arm64 Raspberry Pi image
It creeps me out how there's a bunch of skulls in the term when it loads.
I didn't bother to do a checksum
that's how they get ya ;')

Its really minimal
boots straight to a terminal really quick.

- Step 1 
```
# run the command:
menu-config
# use VGA font make it huge! utf-8, optimal, vga, 16X28 
```

- Step 2
```
# create a user named bweew with
useradd bweew
```

- Step 3
```
# Install desktop
apt install xorg-xserver xinit i3
```
```
# add this to .profile:
vim .profile
#start i3 if tty shows up
if [ -z "$DISPLAY" ] && [ "$(tty)" = "/dev/tty1" ]; then
  startx
fi
```
```
# add this to .xinitrc
vim .xinitrc
exec i3
```

- Step 5
```
sudo vim /etc/inittab
# on line 55
# change it to:
1:2345:respawn:/sbin/agetty --autologin bweew --noclear 38400 tty1
```

- Step 6
```
# edit .bashrc uncomment lines for bash highlighting
```