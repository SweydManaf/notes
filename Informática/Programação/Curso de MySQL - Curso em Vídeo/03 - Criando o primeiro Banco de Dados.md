# Primeiro código

### Criando um banco de dados (um navio)

```mysql
create database cadastro;
```

Após criar o banco de dados **cadastro **você terá Tables (tabelas), Views (visões), Stored Procedures (procedimentos armazenados) e Functions (funções).

NB: Os comandos podem ser em maiúscula ou minúsculas.

### Criando tabelas

Para criar uma tabela temos que saber que o meu container de pessoas tem características padronizadas para todos eles. Todos da tabela Pessoas vão ter nome, idade, sexo, peso, altura e nacionalidade, essas características são chamadas de campos (fields).

**Banco de dados contem tabelas -> Tabelas contem registros -> Registros são compostos por campos.**

### Primeiro avisar ao mysql qual banco de dados iremos usar

```mysql
use database cadastro;
```

## Tipos primitivos do MySQL

- Numérico
    - Inteiro
        - TinyInt, SmallInt, Int, MediumInt, BigInt;
    - Real
        - Decimal, Float, Double, Real;
    - Lógico
        - Bit, Boolean
- Data/Tempo
    - - Date, DateTime, TimeStamp, Time, Year
- Literal
    - Caractere
        - Char (fixo), VarChar (variável);
    - Texto
        - TinyText, Text, MediumText, LongText;
    - Binário
        - TinyBlob, Blob, MediumBlob, LongBlob;
    - Coleção
        - Enum, Set;
- Espacial
    - - Geometry, Point, Polygon, MultiPolygon;

## Criando a tabela

```mysql
create table pessoas (
    nome varchar(30),
    idade tinyint,
    sexo char(1),
    peso float,
    altura float,
    nacionalidade varchar(20)
);
```

## Resumo

```mysql
[1] - show databases; -> mostra os bancos de dados disponiveis
[2] - use cadastro; -> seleciona o banco de dados
[3] - status; -> ver qual banco de dados está aberto
[4] - show tables; -> mostra as tabelas do banco selecionado 
[5] - describe pessoas; -> descreve a tabela com detalhes gráficos
```