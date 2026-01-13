---
author:
  name: Paulo Henrique Zanoteli Santos
title: Ruby setup
date: 2025-08-11 00:10:00 UTC-3
categories: [Guides, Ruby]
tags: [ruby, rbenv]
---

## Ruby setup

Eu sempre esqueço isso aqui, então fica ai o exemplo

### 1. Instala o RBENV (Fedora)

Se você tiver usando Fedora, se for outra [distro](https://github.com/rbenv/rbenv)

```shell
sudo dnf install rbenv
```

### 1. No Debian/Ubuntu based

#### Primeiro instala o RBENV com o git

[link](https://github.com/rbenv/rbenv?tab=readme-ov-file#basic-git-checkout)

#### Depois instala o Ruby-build

[link](https://github.com/rbenv/ruby-build#readme)

#### Inicia o RBENV

```shell
rbenv init
```

#### Eu uso zsh então também tenho que fazer isso, coloca no final do `.zshrc`:

```shell
export RBENV_ROOT="$HOME/.rbenv"
export PATH="$RBENV_ROOT/bin:$PATH"

eval "$(rbenv init - zsh)"

# assuming that rbenv was installed to `~/.rbenv`
FPATH=~/.rbenv/completions:"$FPATH"

autoload -U compinit
compinit
```

#### Fecha e abre o terminal

### 3. Instala a versão que quiser
#### (lembrando que Ubuntu/Debian based podem faltar dependências na hora de compilar)

```shell
rbenv install 3.0.0
```

### 4. Setando a versão

```shell
# setando a versão pra maquina inteira
rbenv global 3.0.0

# setando a versão apenas para esse diretorio
rbenv local 3.0.0
```
