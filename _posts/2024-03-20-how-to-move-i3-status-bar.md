---
author:
  name: Paulo Henrique Zanoteli Santos
title: How to move i3 status bar
date: 2024-03-20 00:45:00 UTC-3
categories: [Guides, Window Manager]
tags: [i3-wm, i3-status]
---

## 1 - First let's make a backup of our original i3 WM config

```shell
cp ~/.config/i3/config ~/.config/i3/config.ori
```

## 2 - Edit i3 WM config 

I gonna use NVIM to edit the config, you can use whatever editor you want

```shell
nvim ~/.config/i3/config
```

## 3 - Inside of config file

Now we're gonna to add this line to move i3 status bar to top

```shell
bar {
    ....
    position top
}
```

## 4 - Save the changes and restart i3 WM

```shell
Super + Shift + r
```