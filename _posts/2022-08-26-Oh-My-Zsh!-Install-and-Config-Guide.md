---
author:
  name: Paulo Henrique Zanoteli Santos
title: Oh-My-Zsh! Install and Config Guide
date: 2022-08-26 20:00:00 UTC-3
categories: [Guides, Shell]
tags: [install-guide, config-guide, shell, zsh]
---

## 1 - Install zsh and oh-my-zsh

1 - First you've to install the shell zsh.

I'm a fedora user, so I'm gonna use DNF but if you're Ubuntu user try APT instead of DNF:
```shell
sudo dnf install zsh
```

2 - Install oh-my-zsh:
```shell
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

3 - Set zsh as your default shell:
```shell
chsh -s /usr/bin/zsh
```

## 2 - Nerd Fonts (optional)

Feel free to choose your nerd font: [Nerd Fonts download](https://www.nerdfonts.com/font-downloads)

I'm gonna use Hack Nerd Font.

## 3 - PowerLevel10k (optional)

PowerLevel10k is a theme to oh my zsh.

1 - Download it:
```shell
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

2 - Set `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`.

```shell
ZSH_THEME="powerlevel10k/powerlevel10k"
```

## 4 - zsh-syntax-highlighting (optional)

zsh-syntax-highlighting is a syntax highlighter for shell commands.

1 - Download it:
```shell
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

2 - Set in your `~/.zshrc`:

```shell
plugins=( 
    git
    zsh-syntax-highlighting
)
```

## 5 - zsh-autosuggestions (optional)

zsh-autosuggestions is a autocomplete tool for your shell.

1 - Download it:
```shell
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

2 - Set in your `~/.zshrc`:

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
