---
title: archbang linux
date: 2024-07-07T18:26:19.686Z
---
[Archbang Download](https://archbang.org/download/)

I like it

it comes with i3

internet works once you click on the wifi icon niiiiice!



```
#get packages setup
#packey

#search packages with
#sudo pacman -Ss

#install vim
sudo pacman -S vim

#fix screen brightness
sudo pacman -S xorg-xbacklight
xbacklight -set 2

# laptop battery improvement
sudo pacman -S tlp
sudo systemctl enable --now tlp

# change wallpaper
cd ~/Backgrounds
wget https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhEm334AKoGG4A7ZWvqPuqwyTLMoyAvidnw34ignM_z0g8-oH8ZWI-iTCix4QUxqWnifp474Uc1t8zBlXi-ElEwpgyhJdZlNbKPCS_swAhvT_awySVTkrzFYaqInjnC-9RUOdv9GCqZh0pAO4CXAFCv-7UF_8-J9kbIPW6ZuaOk12h6Gxeq6HvN_9iof4M/s1920/fleur.jpg
vim ~/.config/openbox/autostart
feh -bg-scale ~/Backgrounds/fleur.jpg
```