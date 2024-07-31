---
title: Antix - Remap Grave to Left Click
date: 2024-07-31T21:51:38.443Z
---
```
sudo apt install xdotool
sudo apt install xbindkeys
touch ~/.scripts
cd ~/.scripts
vim graveclick.sh
```

```
#!/bin/bash
# Delay to allow the system to register the key press
sleep 0.1
# Perform a left mouse click
xdotool click 1
```

```
vim ~/.xbindkeysrc
```

```
"bash ~/.scripts/graveclick.sh"
grave
```

icewm toolbar settings manager > autostart add the line 

```
xbindkeys &
```

after that open up a terminal and run 

```
icewm --restart
```

or log out and back in