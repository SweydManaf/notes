---
title: 'Live de Python 86 - Iteradores e geradores '
updated: 2022-10-17 08:05:56Z
created: 2022-09-26 01:42:00Z
latitude: -25.89196800
longitude: 32.60513510
altitude: 0.0000
---

# Iteradores e geradores

Qualquer coisa que e possível fazer um `for`, pode ser considerado um iterador. Ou, seja, qualquer coisa que pode ser "desmontada" ou "ter coisas dentro" e que permite acessar essas coisas sequencialmente (a grosso modo), pode ser considerado um iterrador.

Entre os tipos "nativos" temos:

- Listas
- Tuplas
- Strings
- Dicionários
- Conjuntos

## Slice

Quando falamos de sequências em Python. contamos com slice. Que é uma maravilha, diga-se de passagem: Isso é implementado pelo protocolo de sequencia. (Live 32). Onde implementamos ****getitem**.**

Iterador é qualquer coisa que é passível de ser iterada ou seja, de ser desmontada via sequências. Toda vez que o python vai "iterar" sobre algo, ele chama uma função, chamada iter().

Exemplos:
A função `enumerate()` é um bom exemplo de iterador. Você não consegue acessar os itens da sequencia individualmente, mas o for sabe como fazer isso.

Exemplos:

- map
- filter
- zip
- reversed
- Modulo itertools (count, takewhile, groupby)

Todos os objetos iteráveis implementam um método chamada **iter**, que e responsável por retornar um iterador.

### Iterável VS Iterador

**iterável** é qualquer coisa que é chamado pela função `iter()` retorna um iterador.

**iterador** é a coisa que sabe como chamar o próximo da sequencia usando a função `next()`.

==O iterador itera no iterável.==

Então, a função `iter()`, retorna um objeto iterador <iterator>.</iterator> Que dentro dele tem um método chamador **next**, que sabe "como chamar o próximo."

**Geradores -** ==geradores são maneiras de "fazer" um iterador. Sem toda aquela confusão de classes.==

**Yield -** A palavra reservada `yield` pode ser usado no corpo de qualquer função*. Isso vai transformar a sua função em um iterável.

**Nomenclatura -** Quando usamos `return`, dizemos que a função 'retorna algo'. Quando usamos `yield` dizemos que a função faz/era algum tipo de valor.