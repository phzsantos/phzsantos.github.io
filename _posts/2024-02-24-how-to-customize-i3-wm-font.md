---
author:
  name: Paulo Henrique Zanoteli Santos
title: How to customize i3 WM font
date: 2024-02-24 22:05:00 UTC-3
categories: [Guides, Window Manager]
tags: [i3-wm, font]
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

Now we're gonna to change this line

```shell
font pango:monospace 8
```

what I do is just copy and edit it for the font of my preference and comment the older line

```shell
#font pango:monospace 8
font pango:Hack Nerd Font:Regular 12
```

## 4 - Save the changes and restart i3 WM

```shell
Super + Shift + r
```
