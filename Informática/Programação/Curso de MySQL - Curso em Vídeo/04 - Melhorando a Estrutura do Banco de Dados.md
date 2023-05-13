# Melhorando a Estrutura do Banco de Dados

### Eliminado um banco de dados

```mysql
drop database cadastro;
```

###  Parâmetros Constraints e Collation - adicionando suporte a caracteres latim

```mysql
create database cadastro
default character set utf8
default collate utf8_general_ci;
```

### Otimizando a estrutura da tabela

```mysql
create table pessoas (
    nome varchar(30) NOT NULL,
    nascimento date,
    sexo enum('M','F'),
    peso decimal(5,2),
    altura decimal(3,2),
    nacionalidade varchar(20) DEFAULT 'Brasil'
) DEFAULT CHARSET = utf8;
```

### Definindo uma chave primaria

```mysql
create table pessoas (
    #id int NOT NULL AUTO_INCREMENT,
    nome varchar(30) NOT NULL,
    nascimento date,
    sexo enum('M','F'),
    peso decimal(5,2),
    altura decimal(3,2),
    nacionalidade varchar(20) DEFAULT 'Brasil',
    #PRIMARY KEY (id)
) DEFAULT CHARSET = utf8;
```