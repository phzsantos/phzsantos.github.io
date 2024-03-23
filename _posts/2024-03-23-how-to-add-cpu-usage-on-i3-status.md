---
author:
  name: Paulo Henrique Zanoteli Santos
title: How to add cpu usage on i3 status
date: 2024-03-23 00:15:00 UTC-3
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

We gonna add this code

```shell
order += "cpu_usage"

cpu_usage {
	format = "%usage 📈"
}
```

## 4 - Save the changes and restart i3

```shell
Super + Shift + r
```
