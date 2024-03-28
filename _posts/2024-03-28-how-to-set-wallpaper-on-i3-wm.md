---
author:
  name: Paulo Henrique Zanoteli Santos
title: How to set wallpaper on i3 WM
date: 2024-03-28 01:00:00 UTC-3
categories: [Guides, Window Manager]
tags: [i3-wm, wallpaper]
---

## 1 - Let's install nitrogen

Use `apt` for debian based distros

```shell
sudo dnf install nitrogen
```

## 2 - Open nitrogen and set wallpaper

This is really straightforward so no tutorial for this

## 3 - Let's make a backup of our original i3 WM config

```shell
cp ~/.config/i3/config ~/.config/i3/config.ori
```

## 4 - Edit i3 WM config 

I gonna use NVIM to edit the config, you can use whatever editor you want

```shell
nvim ~/.config/i3/config
```

## 5 - Inside of config file

We gonna add this code to set wallpaper everytime i3 WM starts

```shell
exec --no-startup-id nitrogen --restore
```

## 6 - Save the changes and restart i3 WM

```shell
Super + Shift + r
```
