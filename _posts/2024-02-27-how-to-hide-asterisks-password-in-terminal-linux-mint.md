---
author:
  name: Paulo Henrique Zanoteli Santos
title: How to hide asterisks password in terminal Linux Mint
date: 2024-02-27 17:35:00 UTC-3
categories: [Guides, Linux]
tags: [linux-mint]
---

## 1 - Go to sudoers.d

```shell
cd /etc/sudoers.d
```

## 2 - Rename 0pwfeedback to 0pwfeedback.disabled

```shell
sudo mv 0pwfeedback 0pwfeedback.disabled
```

## 3 - That's done!
