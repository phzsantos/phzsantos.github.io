---
author:
  name: Paulo Henrique Zanoteli Santos
title: Type hinting
date: 2025-08-11 00:50:00 UTC-3
categories: [Guides, Python]
tags: [python3, type-hinting]
---

## Type hinting

Basicamente simplifcar a leitura de codigo mostrando o tipo de cada variavel ou retorno.

O type hinting não deixa ela estaticamente tipada, você pode ate colocar que quer receber uma string mas se receber um int... problema é seu.

### A partir do Python 3.5!

A PEP que deu origem a ela é [484](https://peps.python.org/pep-0484/)

### Mais usados

```python
palavra_ou_letra: str
numero_inteiro: int
numero_flutuante: float
valor_booleano: bool
```

### Coleções

```python
lista: list[str]
tupla: tuple[float]
dicionario: dict[str, float]
conjunto: set[int]
```

### Com funções

Você usa o `-> tipo:` para definir o tipo de retorno

```python
def alguma_funcao_qualquer(palavra: str) -> str:
    return palavra

# Exemplo se tiver que colocar um valor padrão
def alguma_funcao_qualquer(numero: int = 0) -> int:
    return numero

# Exemplo de uma função que não retorn nada
def funcao_que_nao_retorna_nada(palavra: str) -> None:
    print(palavra)
```