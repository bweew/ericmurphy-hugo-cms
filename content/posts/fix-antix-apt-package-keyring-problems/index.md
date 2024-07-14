---
title: fix antix apt package keyring problems
date: 2024-07-14T05:24:35.960Z
---
[the forum solution](https://www.antixforum.com/forums/topic/expkeysig-error-2/)

```
wget -c http://repo.antixlinux.com/antix-archive-keyring_20019.5.0_all.deb
sudo dpkg -i antix-archive-keyring_20019.5.0_all.deb
```