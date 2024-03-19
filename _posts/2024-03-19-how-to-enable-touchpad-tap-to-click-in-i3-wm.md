---
author:
  name: Paulo Henrique Zanoteli Santos
title: How to enable touchpad tap to click in i3 WM
date: 2024-03-19 01:50:00 UTC-3
categories: [Guides, Window Manager]
tags: [i3-wm, touchpad]
---

## Disclaimer

Well, it actually isn't related to i3 WM, i3 WM is just a window manager, it means it just adjust windows on your screen and that’s it. But if you're on i3 WM and use a laptop like I do, it's gonna be really helpful

## 1 - Create `/etc/X11/xorg.conf.d/touchpad-tap.conf`

```shell
sudo nvim /etc/X11/xorg.conf.d/touchpad-tap.conf
```

## 2 - Paste it inside of conf file

```shell
Section "InputClass"
        Identifier "libinput touchpad catchall"
        MatchIsTouchpad "on"
        MatchDevicePath "/dev/input/event*"
        Driver "libinput"
        Option "Tapping" "on"
EndSection
```

## 3 - Save it and restart your xorg session (just logout and login)
