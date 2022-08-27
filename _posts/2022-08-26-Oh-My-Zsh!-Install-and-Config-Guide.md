---
author:
  name: Paulo Henrique Zanoteli Santos
title: Oh-My-Zsh! Install and Config Guide
date: 2022-08-26 20:00:00 UTC-3
categories: [Guides, Install/config]
tags: [install-guide, config-guide]
---

## Install zsh and oh-my-zsh

First you've to install the shell zsh.

I'm a fedora user, so I'm gonna use DNF but if you're Ubuntu user try APT instead of DNF:
```shell
sudo dnf install zsh
```

Install oh-my-zsh:
```shell
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

Set zsh as your default shell:
```shell
chsh -s /usr/bin/zsh
```

## Nerd Fonts

Feel free to choose your nerd font: [Nerd Fonts download](https://www.nerdfonts.com/font-downloads)

I'm gonna use Hack Nerd Font.

## PowerLevel10k

PowerLevel10k is a theme to oh my zsh.

```shell
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

Set `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`.

```shell
ZSH_THEME="powerlevel10k/powerlevel10k"
```

## zsh-syntax-highlighting

zsh-syntax-highlighting is a syntax highlighter for shell commands.

```shell
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

Set in your `~/.zshrc`:

```shell
plugins=( 
    git
    zsh-syntax-highlighting
)
```

## zsh-autosuggestions

zsh-autosuggestions is a autocomplete tool for your shell.

```shell
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

Set in your `~/.zshrc`:

```shell
plugins=( 
    git
    zsh-syntax-highlighting
    zsh-autosuggestions
)
```

## Documentation and Utilities

[Oh-My-Zsh offical documentation](https://ohmyz.sh/#install)

[PowerLevel10k offical documentation](https://github.com/romkatv/powerlevel10k#oh-my-zsh)

[zsh-syntax-highlighting offical documentation](https://github.com/zsh-users/zsh-syntax-highlighting)

[zsh-autosuggestions offical documentation](https://github.com/zsh-users/zsh-autosuggestions)
