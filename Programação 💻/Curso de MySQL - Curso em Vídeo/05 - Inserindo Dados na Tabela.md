# Inserindo Dados na Tabela (INSERT INTO)

- Dados como id não precisam ser definidos pois eles são automáticos

```mysql
INSERT INTO pessoas
(nome, nascimento, sexo, peso, altura, nacionalidade)
VALUES
('Sweyd', '1979-12-30','M', '50.2','1.85', 'Irlanda');
```

- Você também pode fazer a inserção de dados sem especificar as chaves, se os valores estiveram na mesma ordem das colunas

```mysql
INSERT INTO pessoas VALUES
('Sweyd', '1979-12-30','M', '50.2','1.85', 'Irlanda');
```

- Você também pode inserir vários dados separando cada entrada por virgula.

### Visualizando as inserções

```mysql
SELECT * FROM pessoas;
```