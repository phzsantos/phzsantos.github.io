---
author:
  name: Paulo Henrique Zanoteli Santos
title: How to change default terminal of i3 WM
date: 2024-03-27 01:00:00 UTC-3
categories: [Guides, Window Manager]
tags: [i3-wm, terminal]
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

Now we're gonna change this line (I'm alacritty user so I'm gonna change it to alacritty)

```shell
bindsym $mod+Return exec alacritty
```

## 4 - Save the changes and restart i3 WM

```shell
Super + Shift + r
```