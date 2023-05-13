# Alterando a Estrutura da Tabela (ALTER TABLE e DROP TABLE)

## Adicionado colunas

- Adicionando uma nova coluna

```mysql
ALTER TABLE pessoas ADD COLUMN profissao varchar(10);
```

NB: Adiciona na última posição por padrão;

- Adicionado uma nova coluna no inicio da tabela

```mysql
ALTER TABLE pessoas ADD COLUMN profissao varchar(20) FIRST;
```

- Adicionando uma nova coluna em uma posição específica

```mysql
ALTER TABLE pessoas ADD COLUMN profissao varchar(20) AFTER nome;
```

## Eliminando uma coluna

```mysql
ALTER TABLE pessoas DROP COLUMN profissao;
```

## Modificando definições

- Modificando as constrains (tipos primitivos e valores padrões)

```mysql
ALTER TABLE pessoas
MODIFY COLUMN profissao varchar(20);
```

Caso queira mudar o valor padrão e tirar do NULL

```mysql
UPDATE pessoas SET profissao = '' WHERE profissao is NULL;
ALTER TABLE pessoas MODIFY profissao varchar(20) NOT NULL DEFAULT '';
```

- Renomeando a coluna

```mysql
ALTER TABLE pessoas CHANGE COLUMN profissao prof varchar(20) NOT NULL DEFAULT '';
```

- Renomeando Tabela

```mysql
ALTER TABLE pessoas RENAME TO gafanhotos;
```

## Mais dicas de tabelas

- Criando uma tabela se não existir

```mysql
CREATE TABLE IF NOT EXISTS cursos (
    nome varchar(30) NOT NULL UNIQUE,
    descricao text,
    carga int UNSIGNED,
    totaulas int,
    ano year DEFAULT '2016'
) DEFAULT CHARSET=utf8;
```

Constrains:

- - UNIQUE - impede de 
    - UNSIGNED - impede números negativos significa sem sinal;
- Adicionando Chave Primaria

```mysql
ALTER TABLE cursos ADD COLUMN idcurso int FIRST;
ALTER TABLE cursos ADD PRIMARY KEY (idcurso);
```

- Apagando a Tabela

```mysql
DROP TABLE cursos;
```