---
title: reborn os i3 screen brightness on 2008 imac
date: 2024-07-10T13:31:06.217Z
---
after chown and chmod664-ing the brightness file

```
sudo chown reborn /sys/class/backlight/radeon_bl0/brightness
sudo chmod 664 /sys/class/backlight/radeon_bl0/brightness
```

```
# Increase brightness
bindsym XF86MonBrightnessUp exec --no-startup-id sh -c 'echo $(($(cat /sys/class/backlight/radeon_bl0/brightness) + 10)) > /sys/class/backlight/radeon_bl0/brightness'

# Decrease brightness
bindsym XF86MonBrightnessDown exec --no-startup-id sh -c 'echo $(($(cat /sys/class/backlight/radeon_bl0/brightness) - 10)) > /sys/class/backlight/radeon_bl0/brightness'
```

Hiding the Mouse

* first install gvim so you can copy paste 
* might as well set wallpaper while youve got the config open
* logout without clicking on mouse nagbar
* remap caps lock to escape


```
vim ~/.setxkbmap_caps_escape.sh

#!/bin/bash
setxkbmap -option caps:escape

chmod +x ~/.setxkbmap_caps_escape.sh
```


```
sudo pacman -S gvim
sudo pacman -S unclutter
sudo pacman -s nitrogen

vim ~/.config/i3/config

#hide mouse on idle
exec --no-startup-id unclutter -idle 2

#load background wallpaper on login
exec --no-startup-id nitrogen --restore

# NO NAGBAR LOGOUT
bindsym $mod+Shift+q exec --no-startup-id i3-msg exit

#caps to escape
exec --no-startup-id ~/.setxkbmap_caps_escape.sh
```
