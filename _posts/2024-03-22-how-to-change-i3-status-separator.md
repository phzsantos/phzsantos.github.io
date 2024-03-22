---
author:
  name: Paulo Henrique Zanoteli Santos
title: How to change i3 status separator
date: 2024-03-22 02:40:00 UTC-3
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

Now we're gonna to add this line to make separator a blank space

```shell
bar {
    ....
    separator_symbol " "
}
```

## 4 - Save the changes and restart i3 WM

```shell
Super + Shift + r
```
