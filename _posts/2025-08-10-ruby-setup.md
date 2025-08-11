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

### 1. Instala o RBENV

Se você tiver usando Fedora, se for outra [distro](https://github.com/rbenv/rbenv)

```shell
sudo dnf install rbenv
```

### 2. Inicia o RBENV

```shell
rbenv init
```

Depois de rodar ele, fecha e abre o terminal

### 3. Instala a versão que quiser

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
