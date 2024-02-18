---
author:
  name: Paulo Henrique Zanoteli Santos
title: How to customize i3 status 
date: 2024-02-18 16:20:00 UTC-3
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

Well now you do whatever you wanna do. What I like to do is to remove some info from i3status (I just comment it out)

```shell
#order += "ipv6"
#order += "wireless _first_"
#order += "ethernet _first_"
order += "battery all"
#order += "disk /"
#order += "load"
order += "memory"
order += "tztime local"
```

## 4 - Save the changes and restart i3

```shell
Super + Shift + r
```
