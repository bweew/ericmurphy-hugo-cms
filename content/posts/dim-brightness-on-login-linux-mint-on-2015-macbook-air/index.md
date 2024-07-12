---
title: dim brightness on login linux mint on 2015 macbook air
date: 2024-07-12T23:11:24.297Z
---
my fix for using a system d daemon on startup that uses intel_backlight

to check if thats the right one to use for you use 

```
ls /sys/class/backlight/

```

create the systemd service file

```
sudo vim /etc/systemd/system/backlight.service
```



write the file

```
[Unit]
Description=Set Intel backlight brightness on startup
After=multi-user.target

[Service]
Type=oneshot
ExecStart=/bin/bash -c 'echo 40 > /sys/class/backlight/intel_backlight/brightness'

[Install]
WantedBy=multi-user.target
```

reload system d and enable the service

```
sudo systemctl daemon-reload
sudo systemctl enable backlight.service
```

optional: manually test the service with

```
sudo systemctl start backlight.service
```

then sudo reboot