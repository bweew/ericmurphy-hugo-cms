---
title: adding i3 on mxlinux
date: 2024-07-10T01:42:01.148Z
---
{{< youtube MMRVG9jk >}}



```
sudo apt install i3
sudo apt install dmenu
```

* from start menu, > keyboards> delete all the xfce shortcuts
* session and startup > application autostart add i3

  * name: i3
  * description: i3wm
  * command: i3
* session and startup >current session. disable these:

  * xfwm4
  * xfce4-panel
  * xfdesktop

```
# if you want rofi instead of dmenu
sudo apt install rofi
cd ~/.config/rofi
git clone https://github.com/dracula/rofi
cp rofi/theme/config1.rasi ~/.config/rofi/config.rasi

vim ~/.config/i3/config
#/ to search dmenu uncomment it replace it with rofi
```