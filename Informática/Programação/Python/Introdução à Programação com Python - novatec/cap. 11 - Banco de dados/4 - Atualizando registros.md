# Atualizando registros

O comando para atualizar um registro é basicamente assim:

```sql
UPDATE agenda SET telefone = '12345-6789' WHERE nome='Nilo'
```

A cláusula `where` funciona como no comando `select` , ou seja, ela avalia uma expressão lógica que, quando verdadeira, inclui o registro na lista de registros a modificar. A segunda parte do comando `update` é a cláusula `set` . Essa cláusula é usada para indicar o que fazer nos registros selecionados pela expressão do `where` .

\* Atualizando o registro de forma estatica

```python
import sqlite3

conexao = sqlite3.connect('agenda.db')
cursor = conexao.cursor()

cursor.execute("UPDATE agenda SET telefone='12345-6789' WHERE nome='Nilo'")

conexao.commit()

cursor.close()
conexao.close()
```

Se não dermos o parâmetro `WHERE` o `UPDATE` fará atualizações em todos os registros. Podemos usar a propriedade `rowcount` do nosso cursor para saber quantos registros foram alterados pelo nosso update

```python
import sqlite3

conexao = sqlite3.connect('agenda.db')
cursor = conexao.cursor()

cursor.execute('UPDATE agenda SET telefone="12345-6789"')

print(f'Registros alterados: {cursor.rowcount}')

conexao.commit()
cursor.close()
conexao.close()
```

Podemos usar o `rowcount` para verificar quantas alterações foram feitas, lembrar que as alterações só serão aplicadas após o `commit`. Caso queiramos abortar a alteração podemos dar um `rollback`. Que o inverso do `commit`.Basicamento o `commit` \-\- aplica e o  `rollback` \-\- aborta.

```python
import sqlite3

conexao = sqlite3.connect('agenda.db')
cursor = conexao.cursor()

cursor.execute('UPDATE agenda SET telefone="12345-6789"')

print('Registros alterados:', cursor.rowcount)

if cursor.rowcount == 1:
    conexao.commit()
    print('Alterações gravadas')
else:
    conexao.rollback()
    print('Alterações abortadas.')

conexao.close()
```