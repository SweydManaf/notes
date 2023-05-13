## Agrupamento de dados

As funções de agregação são: count, sum, avg, min , max.

Agrupando estados e usando a função de agregação `count`:

```sql
select região, count(*) from estados group by região
```

Esse comando utilizada a cláusula `group by` região para especificar a chave de grupo. Dessa forma, todos os registros que pertencem a mesma região são agrupados.

- Agrupando e contando os estados por região

```python
import sqlite3

print('Região Número de Estados')
print('===== ==================')

with sqlite3.connect('brasil.db') as conexao:
    for regiao in conexao.execute('SELECT regiao, count(*) FROM estados GROUP BY regiao'):
        print('{0:6} {1:17}'.format(*regiao))
```

- Usando as funções de agregação

```python
import sqlite3

print('Região Estados População  Mínima   Máxima     Média   Total (soma)')
print('====== =======          ======== ========= ==========  ===========')

with sqlite3.connect('brasil.db') as conexao:
    for regiao in conexao.execute("""SELECT regiao, 
                                    count(*), min(populacao), 
                                    max(populacao), avg(populacao), 
                                    sum(populacao) 
                                    FROM estados GROUP BY regiao"""):

        print('{0:6} {1:7} {2:18,} {3:10,} {4:10,.0f} {5:13,}'.format(*regiao))

    print('\nBrasil: {0:6} {1:18,} {2:10,} {3:10,.0f} {4:13,}'.format(*conexao.execute("""SELECT count(*), 
    min(populacao), max(populacao), avg(populacao), sum(populacao) FROM estados""").fetchone()))
```

- Utilizando o `HAVING` para listar apenas regiões com mais de 5 estados

```python
import sqlite3

print('Região Estados População  Mínima   Máxima     Média   Total (soma)')
print('====== =======          ======== ========= ==========  ===========')

with sqlite3.connect('brasil.db') as conexao:
    for regiao in conexao.execute('''SELECT regiao, count(*), 
                                    min(populacao), max(populacao), 
                                    avg(populacao), sum(populacao) as tpop 
                                    FROM estados
                                    GROUP BY regiao
                                    HAVING count(*)>5
                                    ORDER BY tpop DESC'''):

       print('{0:6} {1:7} {2:18,} {3:10,} {4:10,.0f} {5:13,}'.format(*regiao))
```