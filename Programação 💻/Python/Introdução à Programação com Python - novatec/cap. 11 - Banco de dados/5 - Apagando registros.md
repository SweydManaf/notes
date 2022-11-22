# Apagando registros

O comando SQL para apagar registros é:

```sql
DELETE FROM agenda WHERE nome="Maria"
```

Em Python teríamos mais ou menos:

```python
import sqlite3

conexao = sqlite3.connect('agenda.db')
cursor = conexao.cursor()

cursor.execute('DELETE FROM agenda WHERE nome="Maria"')

print('Registros apagados: ', cursor.rowcount)

if cursor.rowcount == 1:
    conexao.commit()
    print('Alterações gravadas')
else:
    conexao.rollback()
    print('Alterações abortadas')

conexao.close()
```

Utilizamos o método `rowcount` para ter certeza de que estávamos apagando apenas um registro. Assim como no comando `insert` e `update` , você precisa chamar `commit` para gravar as alterações ou `rollback` , caso contrário.