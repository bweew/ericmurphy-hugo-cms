---
title: linux mint 2008 imac set brightness from bash command
date: 2024-07-12T23:53:13.980Z
---
my other fix works great on login but if you ever change it using the brightness buttons it never goes back down as low as I had it before. so to darken it more i add this bash alias to my .bashrc

```
alias dim='sudo sh -c "echo 40 > /sys/class/backlight/intel_backlight/brightness"'
```