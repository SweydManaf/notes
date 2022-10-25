---
title: Live de Python 18 - Compreensão de containers e geradores
updated: 2022-10-18 18:13:27Z
created: 2022-10-17 19:09:03Z
---

# List/dics/set comps e gen expr

## Functor

Na Teoria das categorias, é um mapeamento entre categorias que \*\*preserva estruturas. \*\*Os functores podem ser entendidos como homomorfismos na categoria de todas as categorias pequenas (ou seja, a categoria quem tem como objetos todas as categorias compostas por objetos que são conjuntos).

Ou seja: Associa para cada objeto x em um conjunto \*\*C \*\*um objeto F(x) em um conjunto **D.**

## Aplicação de uma função simples

```python
def mais_2(x):
    return x + 2
```

## Aplicação de uma função anonima \[0\]

```python
lambda x: x + 2

// OU

In [1]: (lambda x: x + 2)(2)
Out [1]: 4
```

Aplicação de uma função anonima \[1\]

```python
In [1]: from fn import _

In [2]: (_+2)(2)
Out [2]: 4
```

## Lazy evaluation - Avaliação preguiçosa

São retornos (as vezes de funções que só são computados quando chamados). Comumente são chamados pelo método `__next__()` pela função `next()`.

## Map

O Map é uma função com retorno preguiçoso, que dada uma função **f(x),** aplicada a uma sequência **S**, retorna uma nova sequência lazy da aplicação de f(x) para todos os elementos de S formando assim uma nova sequência que podemos chamar de Z.

Ou seja:

```python
map(f, S) -> Z => map(lambda x: x*2, [1,2,3]) -> [2, 4, 5]
```

 OBS: a função (f(x)) só pode receber um único argumento. NB: funciona com operados aritméticos.

## Filter

O Filter com retorno preguisoço, que dada uma função f(x), aplicada a uma sequência S, retorna uma nova sequência lazy da aplicação de f(x) para todos os elementos de S formando assim uma nova sequência que vamos chamar de Z.

Ou seja:

```python
filter(f, S) -> Z => filter(lambda x: x>2, [1,2,3]) -> [3]
```

**OBS**: a função (f(x)) só pode receber um único argumento. NB: funciona com operadores lógicos.

## map, filter VS List comprehension

```python
In [1]: list(map(lambda x: x**2, filter(lambda x: x>2, [1,2,3,4,5])))
Out [1]: [9, 16, 25]

// VS

In [2]: [x**2 for x in [1,2,3,4,5] if x>2]
Out [2]: [9, 16, 25]
```

##  Usando o zip

```python
In [1]: zip([1,2,3,4], [5,6,7,8])

In [2]: list(zip([1,2,3,4], [5,6,7,8]))
Out [2]: [(1, 5), (2, 6), (3, 7), (4, 8)]

// No formato list comprehension

In [3]: [(x,y) for x in [1,2,3,4] for y in [5,6,7,8]]
Out [3]: [(1,5), (1,6), (1,7), (1,8), (2,5)...]
```