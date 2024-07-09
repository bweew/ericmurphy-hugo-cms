---
title: antiX linux - fix brightness in herbstluftwm
date: 2024-07-09T09:31:45.891Z
---
vim ~/.config/herbstluftwm/autostart

```
xrandr --output LVDS --brightness 0.5
```