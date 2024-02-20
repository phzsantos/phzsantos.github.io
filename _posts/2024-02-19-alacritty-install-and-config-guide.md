---
author:
  name: Paulo Henrique Zanoteli Santos
title: Alacritty install and config guide 
date: 2024-02-19 22:55:00 UTC-3
categories: [Guides, Linux]
tags: [terminal, alacritty]
---

## 1 - Install alacritty

I’m a fedora user, so I’m gonna use DNF but if you’re Ubuntu user try APT instead of DNF:

```shell
sudo dnf install alacritty
```

## 2 - Create config file

```shell
nvim ~/.alacritty.toml
```

## 3 - Inside of config file

```shell
[shell]
program = "/bin/zsh"

[font]
normal = { family = "Hack Nerd Font", style = "Regular" }
size = 14

[cursor]
style = { shape = "Underline" }
unfocused_hollow = false
```

## 4 - Save it and open alacritty again
