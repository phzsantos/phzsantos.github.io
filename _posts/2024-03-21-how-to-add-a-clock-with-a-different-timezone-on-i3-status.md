---
author:
  name: Paulo Henrique Zanoteli Santos
title: How to add a clock with a different timezone on i3 status
date: 2024-03-21 00:15:00 UTC-3
categories: [Guides, Window Manager]
tags: [i3-wm, i3-status]
---

## 1 - First let's make a backup of our original i3 status config

```shell
cp /etc/i3status.conf ~/.config/i3/i3status.conf
```

## 2 - Edit i3status.conf 

I gonna use NVIM to edit the config, you can use whatever editor you want

```shell
sudo nvim /etc/i3status.conf
```

## 3 - Inside of config file

We gonna add a code like this, for this tutorial I'm gonna use Lisbon timezone

```shell
order += "tztime lisbon"

tztime lisbon {
        format = "%H:%M 🇵🇹"
        timezone = "Europe/Lisbon"
        hide_if_equals_localtime = true
}
```

## 4 - Save the changes and restart i3

```shell
Super + Shift + r
```
