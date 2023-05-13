## Acesso simplificado

A interface de banco de dados do Python nos permite executar alguns comandos utilizando diretamente o objeto da conexão, sem criarmos explicitamente um cursor.

```python
import sqlite3

with sqlite3.connect('agenda.db') as conexao:
    for registro in conexao.execute('SELECT * FROM agenda'):
        print('Nome: %s\tTelefone: %s' % registro)
```

Essa utilização simplificada funciona muito bem com SQLite, mas não faz parte da interface padrão de banco de dados do Python, a DB-API 2.0. Ao utilizar cursores, você obedece a DB-API 2.0 que é implementada por outros bancos de dados, simplificando a migração de seu código para outros bancos de dados, como o MySQL ou MariaDB.

## Acessando os campos como em um dicionário

Acessar os campos por posição nem sempre é tão fácil. Em Python, usando SQLite, podemos acessá-los pelo nome, adicionando uma linha:

```python
import sqlite3

conexao = sqlite3.connect('agenda.db')
conexao.row_factory = sqlite3.Row #
cursor = conexao.cursor()

for registro in cursor.execute('SELECT * FROM agenda'):
    print('Nome: %s\tTelefone: %s' % (registro['nome'], registro['telefone']))

cursor.close()
conexao.close()
```

Dessa forma, registro pode ser acessado como se fosse um dicionário, onde o nome do campo é usado como chave.