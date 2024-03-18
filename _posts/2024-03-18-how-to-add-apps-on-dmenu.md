---
author:
  name: Paulo Henrique Zanoteli Santos
title: How to add apps on dmenu
date: 2024-03-18 00:50:00 UTC-3
categories: [Guides, Window Manager]
tags: [i3-wm, dmenu]
---

## Disclaimer

Well, it actually isn't related to i3 WM, i3 WM is just a window manager, it means it just adjust windows on your screen and that’s it. However, a lot of i3 WM users use dmenu as applications menu

## 1 - Create a symbolic link to /usr/bin

dmenu just show executables that are on `/usr/bin` so what we need to do is create a symbolic link to our application to there

```shell
sudo ln -s /your_app_path/executable /usr/bin/the_name_you_want_to_be_displayed_at_dmenu
```
