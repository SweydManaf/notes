## Inserindo vários dados

```python
# comandos ignorados

produtos = [('Banana', '10,00'), ('Maçã', '15,00'), ('Ananás', '25,00')]

cursor.executemany("""INSERT INTO precos (nome, preco) VALUES (?, ?)""", produtos)

conexao.commit()
cursor.close()
conexao.close()
```

## Consultando dados

```python
# comandos ignorados

cursor.execute("SELECT * FROM precos")
resultado = cursor.fetchall()

for registro in resultado:
    print("Produto: %s\tPreço: %s" % registro)
    
cursor.close()
conexao.close()
```

## Uso do with para fechar a conexão

```python
import sqlite3
from contextlib import closing ❶

with sqlite3.connect("agenda.db") as conexão:
with closing(conexão.cursor()) as cursor:
        
cursor.execute("select * from agenda")
         while True :
            resultado = cursor.fetchone()
             if resultado == None :
                 break
             print ("Nome: %s\nTelefone: %s" % (resultado))
```

1\. Cursores não possuem o método `__exit__` daí a necessidade de usar o `closing` para adaptar o cursor com o método de enceramento.