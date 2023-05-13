##  Gerando uma chave primaria

Podemos gerar uma chave primaria com incremento automatico com o seguinte comando em SQL:

```SQL
CREATE TABLE estados (id integer PRIMARY KEY AUTOINCREMENT, nome text)
```

Em Python teriamos algo assim:

```python
# comandos ignorados

cursor.execute("""
                    CREATE TABLE estados(
                        id integer PRIMARY KEY AUTOINCREMENT,
                        nome text,
                        populacao integer
                        ) 
                """)
                
cursor.executemany('INSERT INTO estados(nome, populacao) VALUES (?, ?)', dados)

conexao.commit()
cursor.close()
conexao.close()
```

O valor do campo id será gerado automaticamente.

## Consulta ordenada

Podemos ordenar a nossa consulta adicionando o parâmetro `ORDER BY` e se quisermos em ordem decrescente adicionamos a tag `DESC`.

```python
import sqlite3

conexao = sqlite3.connect('brasil.db')
conexao.row_factory = sqlite3.Row

print('%3s %-20s %12s' % ('Id', 'Estado', 'População'))
print('='*37)

for estado in conexao.execute('SELECT * FROM estados ORDER BY populacao DESC'): #
    print('%3d %-20s %12d' % (estado['id'], estado['nome'], estado['populacao']))

conexao.close()
```

## Alterando a tabela

Em SQL, o comando utilizado para alterar os campos de uma tabela é o `alter table` .

```sql
ALTER TABLE estados ADD sigla text
```

O comando `alter table` do SQLite é limitado se comparado com outros bancos de dados. Em outros bancos, pode-se alterar vários campos com um só `alter table` , mas no SQLite, somos obrigados a alterar um campo de cada vez. As limitações do `alter table` do SQLite não param por aí.

Em python teremos:

```python
import sqlite3

with sqlite3.connect('brasil.db') as conexao:
    conexao.execute('ALTER TABLE estados ADD sigla text')
```