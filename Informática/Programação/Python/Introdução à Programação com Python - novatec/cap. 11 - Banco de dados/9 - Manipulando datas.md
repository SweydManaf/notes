# Trabalhando com datas

Ao trabalharmos com datas no SQL utilizamos o tipo `date` com a padronização aceita pela ISO 8601 que é ANO-MÊS-DIA.

Ao solicitar o processamento dos tipos de campo em nossas consultas, devemos passar `detect_types=sqlite3.PARSE_DECLTYPES` como parâmetro.

- Solicitando o tratamento do tipo dos campos

```python
import sqlite3

with sqlite3.connect('brasil.db', detect_types=sqlite3.PARSE_DECLTYPES) as conexao:
    for feriado in conexao.execute('SELECT * FROM feriados'):
        print(feriado)
```

Veja que os valores do campo data agora são objetos da classe `datetime.date` . Isso evita termos que fazer a conversão manualmente de string para `datetime.date`.

Podemos utilizar método `strftime` do objeto da classe `datetime.date` para exibir apenas o dia e o mês da data, sem o ano.

```python
import sqlite3

with sqlite3.connect('brasil.db', detect_types=sqlite3.PARSE_DECLTYPES) as conexao:
    conexao.row_factory = sqlite3.Row
    for feriado in conexao.execute('SELECT * FROM feriados'):
        print('{0} {1}'.format(feriado['data'].strftime('%d/%m'), feriado['descricao']))
```

## Dica de ouro

- Feriados nos próximos 60 dias

```python
import sqlite3
import datetime

hoje = datetime.date.today()
hoje60dias = hoje + datetime.timedelta(days=60)

with sqlite3.connect('brasil.db', detect_types=sqlite3.PARSE_DECLTYPES) as conexao:
    conexao.row_factory = sqlite3.Row

    for feriado in conexao.execute('SELECT * FROM feriados WHERE data >= ? and data <= ?', (hoje, hoje60dias)):
        print('{0} {1}'.format(feriado['data'].strftime('%d/%m'), feriado['descricao']))
```

Em `hoje60dias` , utilizamos um objeto do tipo `datetime.timedelta` para acrescentar 60 dias à data atual. Com esses dois objetos `date` , podemos utilizar a cláusula `where` do SQLite para selecionar os feriados entre `hoje` e `hoje60dias` .