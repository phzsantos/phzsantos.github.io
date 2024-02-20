---
author:
  name: Paulo Henrique Zanoteli Santos
title: How to install fonts on linux 
date: 2024-02-20 17:00:00 UTC-3
categories: [Guides, Linux]
tags: [fonts]
---

## 1 - First download your font

For this tutorial I'm gonna use Hack Nerd Font, you can get it here: [Nerd Fonts download](https://www.nerdfonts.com/font-downloads)

## 2 - Create .fonts directory

```shell
mkdir ~/.fonts
```

## 3 - Copy your fonts to .fonts directory

```shell
cp ~/Downloads/Hack.zip ~/.fonts/
```

## 4 - Unzip your fonts

```shell
unzip ~/.fonts/Hack.zip
```

## 5 - Delete unused files

```shell
rm -rf ~/.fonts/Hack.zip
rm -rf ~/.fonts/*.md
rm -rf ~/Downloads/Hack.zip
```

## 6 - Refresh fonts cache

```shell
fc-cache -fv
```

## 7 - Now you can set your font in whatever part of your system
