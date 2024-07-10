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