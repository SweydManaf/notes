# Manipulando Registros

## Modificando Linhas incorretas

```sql
UPDATE cursos SET nome = 'HTML5' WHERE idcurso = '1';
```

### Caso queira modificar varias linhas ao mesmo tempo

```sql
UPDATE cursos SET nome = 'PHP', ano = '2015' WHERE idcurso = '4';
```

Também existe o parâmetro `limit` para limitar a quantidade de mudanças

```sql
UPDATE cursos SET ano = '2050', carga = '800' WHERE ano = '2018' LIMIT 2;
```

## Removendo uma linha

```sql
DELETE FROM cursos WHERE idcurso = '8';
```

## Removendo TODAS as linhas

```sql
TRUNCATE TABLE cursos;
```