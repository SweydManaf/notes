# Comandos SELECT 

## PARTE 1 

- Seleciona e exibe todos os registros da tabela

```sql
SELECT * FROM tabela;
```

- Seleciona e exibe todos os registros da tabela ordenados por uma coluna (campo)

```sql
SELECT * FROM tabela ORDER BY coluna;
```

- Seleciona e exibe todos os registros da tabela ordenados por uma coluna (campo) em ordem descendente `DESC` ou ascendente `ASC`

```sql
SELECT * FROM tabela ORDER BY coluna DESC;

SELECT * FROM tabela ORDER BY coluna ASC;
```

- Seleciona e exibe os registros da tabela somente da(s) coluna(s) especificadas (pode usar também o parametro `ORDER BY`

```sql
SELECT coluna1, coluna2, colunaN FROM tabela;
```

- Seleciona e exibe registros da tabela somente da(s) coluna(s) especificadas e ordenadas por uma coluna ou mais

```sql
SELECT coluna1, coluna2, colunaN FROM tabela ORDER BY coluna1, coluna2, colunaN;
```

Operadores relacionais

- Exibe apenas os registros que tem ano = 2016

```sql
SELECT * FROM cursos WHERE ano=2016 ORDER BY nome;
```

- Exibe registros específicos mas que tenham ano = 2016 e ainda ordena pelo nome. No `where` pode ser usado "&lt;, &gt;, &lt;=, &gt;=, !=, <>"

```sql
SELECT nome, carga FROM cursos WHERE ano=2016 ORDER BY nome;
```

Operadores lógicos

- Exibe registros entre (`between` X `and` Y) uma faixa de valores de uma coluna especifica.

```SQL
SELECT nome, ano FROM cursos WHERE ano BETWEEN 2014 AND 2016;
```

- Exibe registros específicos que estão dentro de determinados valores que estão dentro do `in`.

```sql
SELECT nome, ano FROM cursos WHERE ano in (2014, 2016);
```

- Exibe registros específicos que estão dentro de determinados valores especificados pela logica do `and`, poderia ser também `or`.

```sql
SELECT nome, carga, totaulas FROM cursos WHERE carga > 25 AND totaulas < 30;
```

## PARTE 2

- Aqui o uso do `where` com operador `like` permite filtrar registros com uso do coringa "%" que significa "nada" ou "qualquer quantidade de caractere".

```SQL
SELECT * FROM cursos WHERE nome LIKE 'A%';
```

- Aqui o uso do `where`com operador `like` permite filtrar registros com uso do coringa "_" que significa "um único caractere".

```sql
SELECT * FROM cursos WHERE nome LIKE '_a';
```

- Aqui o `distinct` serve para mostrar apenas uma vez cada ocorrência de um registro.

```sql
SELECT DISTINCT carga FROM cursos ORDER BY carga;
```

- `count` é uma função de agregação que serve pra mostra a quantidade de ocorrências.

```sql
SELECT COUNT(*) FROM cursos WHERE carga>40;
```

- `max` ou `min` exibe a maior ou menor ocorrência dentro de uma coluna especificada.

```sql
SELECT MAX(carga) FROM cursos;

SELECT MIN(totaulas), nome FROM cursos WHERE ano=2016;
```

- `sum` faz exibir a somatória de uma determinada coluna.

```sql
SELECT SUM(totaulas) FROM cursos;
```

- `avg` exibe a média de uma determinada coluna

```sql
SELECT AVG(totaulas) FROM cursos WHERE ano=2016;
```