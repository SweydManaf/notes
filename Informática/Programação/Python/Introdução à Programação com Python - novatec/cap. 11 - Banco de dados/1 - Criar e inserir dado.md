# Primeiro contacto

Structured Query Language (SQL – Linguagem de Consulta Estruturada) é a linguagem usada para criar bancos de dados, gerar consultas, manipular (inserir, atualizar, alterar e apagar) registros e, principalmente, realizar consultas. É uma linguagem de programação especializada na manipulação de dados, baseada na álgebra relacional e no modelo relacional criado por [Edgar F. Codd.](http://pt.wikipedia.org/wiki/Edgar_Frank_Codd)

O SQLite é um gerenciador de banco de dados leve e completo, muito utilizado e presente mesmo em telefones celulares. Uma de suas principais características é não precisar de um servidor dedicado, sendo capaz de se iniciar a partir de seu programa.

## Criando um banco de dados

```python
import sqlite3 ❶

conexão = sqlite3.connect("agenda.db") ❷
cursor = conexão.cursor() ❸

cursor.execute('''
    create table agenda(
        nome text,
        telefone text)
        ''') ❹

cursor.execute('''insert into agenda (nome, telefone) values(?, ?)''', 
        ("Nilo", "7788-1432")) ❺

conexão.commit() ❻
cursor.close() ❼
conexão.close() ❽
```

1.  (ignorado)
    
2.  A conexão com o banco de dados se assemelha à manipulação de um arquivo, é a operação análoga a abrir um arquivo. O nome do banco de dados que estamos criando será gravado no arquivo agenda.db . A extensão .db é apenas uma convenção, mas é recomendado diferenciar o nome do arquivo de um arquivo normal, principalmente porque todos os seus dados serão guardados nesse arquivo.
    
3.  Cursores são objetos utilizados para enviar comandos e receber resultados do banco de dados. Um cursor é criado para uma conexão, chamando-se o método cursor() . Uma vez que obtivemos um cursor, nós podemos enviar comandos ao banco de dados.
    
4.  O método execute de nosso cursor para enviar o comando ao banco de dados.
    
5.  (ignorado)
    
6.  Considere o comando commit em ❻ como parte das operações necessárias para modificar o banco de dados.
    
7.  Antes de terminarmos o programa, fechamos ( close ) o cursor e a conexão com o
    
    banco de dados, respectivamente em ❼ e ❽ .