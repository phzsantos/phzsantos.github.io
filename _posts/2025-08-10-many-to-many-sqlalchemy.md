---
author:
  name: Paulo Henrique Zanoteli Santos
title: Many to many SQLAlchemy
date: 2025-08-10 23:15:00 UTC-3
categories: [Guides, SQLAlchemy]
tags: [python, sqlachemy, sql, orm]
---

## Many to many

Eu sempre esqueço isso aqui, então fica ai o exemplo

### PONTO DE ATENÇÃO

Se for criar as tabelas e a relação delas do ZERO, crie primeiro as tabelas principais e depois você cria a tabela de relação e insere a relação na primeira tabela. No caso de tabelas já existentes basta seguir isso ai.

### 1. Primeiro cria uma tabela como variavel

```python
# Tabela intermediária para a relação many-to-many
students_courses = sa.Table(
    "students_courses",
    Base.metadata,
    sa.Column(
        "student_id", 
        sa.Integer, 
        sa.ForeignKey("students.id"), 
        primary_key=True
    ),
    sa.Column(
        "course_id", 
        sa.Integer, 
        sa.ForeignKey("courses.id"), 
        primary_key=True
    ),
)
```

### 2. Coloca as tabelas que vão ser ligadas depois desse codigo

```python
class Student(Base):
    __tablename__ = "students"

    id = sa.Column(sa.Integer, primary_key=True)
    name = sa.Column(sa.String, nullable=False)


class Course(Base):
    __tablename__ = "courses"

    id = sa.Column(sa.Integer, primary_key=True)
    title = sa.Column(sa.String, nullable=False)
```

### 3. A ligação é isso aqui:

```python
    # Relação many-to-many
    courses = sa.orm.relationship(
        "Course",
        secondary=students_courses,
        backref="students"
    )
```

Você vai colocar isso na primeira tabela que você vai ligar. APENAS na PRIMEIRA. Motivo:

```python
backref="students"
```

Isso vai criar automaticamente um campo na outra tabela que contem todo o conteudo do mesmo campo da outra tabela.

PRONTO É ISSO AI!
