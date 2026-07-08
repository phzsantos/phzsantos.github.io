---
author:
  name: Paulo Henrique Zanoteli Santos
title: How to install PostgreSQL Linux Mint
date: 2026-07-08 16:00:00 UTC-3
categories: [Guides, Linux]
tags: [linux, install-guide, database, postgresql]
---

### 1. Instala o PostgreSQL

```shell
sudo apt install postgresql postgresql-contrib
```

### 2. Inicia o PostgreSQL

```shell
sudo systemctl start postgresql
```

### 3. Cria seu usuario

```shell
sudo -i -u postgres
```

```shell
psql
```

```sql
CREATE ROLE admin
WITH LOGIN
PASSWORD '123456'
SUPERUSER;
```
