# Consultando registros

- Pesquisas em SQL são feitas com a clausula `WHERE`

```SQL
SELECT * FROM agenda WHERE nome='Nilo';
```

Em Python isso ficaria algo assim:

```python
import sqlite3

conexao = sqlite3.connect('agenda.db')
cursor = conexao.cursor()

cursor.execute("SELECT * FROM agenda WHERE nome='Nilo'")

while True:
    resultado = cursor.fetchone()
    if resultado == None:
        break
    print("Nome: %s\tTelefone: %s" % resultado)

cursor.close()
conexao.close()
```

- Para tornar tornar as nossas pesquisas dinâmicas substituímos a constante do nome Nilo e armazenamos o nome em uma variável

```python
import sqlite3

nome = input("Nome a selecionar: ")

conexao = sqlite3.connect('agenda.db')
cursor = conexao.cursor()

cursor.execute(f'SELECT * FROM agenda WHERE nome="{nome}"') #
while True:
    resultado = cursor.fetchone()
    if resultado == None:
        break
    print('Nome: %s\tResultado: %s' % resultado)

cursor.close()
conexao.close()
```

Um problema surge com essa forma de escrever código, experimente inserir `X" or "1"="1` e verá algo surpreendente. Todos os valores serão exibidos. Esse tipo de vulnerabilidade é um exemplo de **SQLInjection**para evitar esse tipo de ataque sempre utilize parâmetros com valores variáveis.

```python
import sqlite3

nome = input('Nome a selecionar: ')
conexao = sqlite3.connect('agenda.db')
cursor = conexao.cursor()

cursor.execute('SELECT * FROM agenda WHERE nome = ?', (nome,)) #
x = 0

while True:
    resultado = cursor.fetchone()
    if resultado == None:
        if x == 0:
            print('Nada encontrado.')
        break
    print('Nome: %s\tTelefone: %s' % resultado)
    x += 1

cursor.close()
conexao.close()
```

Um detalhe importante é que escrevemos (nome,) , repare a vírgula após nome . Esse detalhe é importante, pois o segundo parâmetro do método execute é uma tupla, e, em Python, tuplas com apenas um elemento são escritas com uma vírgula após o primeiro valor.