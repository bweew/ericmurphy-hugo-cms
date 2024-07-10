---
title: antiX linux - fix brightness in herbstluftwm
date: 2024-07-09T09:31:45.891Z
---
vim ~/.config/herbstluftwm/autostart

```
xrandr --output LVDS --brightness 0.6
```

also add picom for transparency in terminal. i swapped roxterm for xfce4-terminal

nitrogen for a gui to change the background.

\- remove the help keybinds txt 

sudo apt install picom

sudo apt install nitrogen

vim ~/.config/herbstluftwm/autostart

```
picom &
nitrogen --restore &
```