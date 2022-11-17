# Chaves Estrangeiras

## Engines mais conhecidas:

\- MyISAM (antiga)

\- InnoDB (padrão, suporte a chave estrangeira)

\- XtraDB (mais recente, suporta a chave estrangeira)

As duas ultimas engines InnoDB e XtraDB suportam o que se chama de ACID que são as quatro principais regras de uma boa transação.

## Para uma transação acontecer deve seguir as 4 principais regras: 

- **Atomicidade** \- uma transação tem que ser atômica ou seja ela não pode se subdividir em sub-tarefas. De uma forma simples isso significa que se houver uma tarefa ou toda tarefa é feita ou nada vai ser considerado.
- **Consistência** \- se antes de fazer a transação o banco de dados estava OK, depois que terminar a transação ele também tem que estar OK. Não podem ocorrer falhas, não podem ocorrer inconsistências e se ocorrer tudo é desfeito para o estado anterior.
- **Isolamento** \- quando tenho duas transação acontecendo em paralelo elas devem ser executadas de forma isolada.
- **Durabilidade** \- uma transação tem que ser durável isso é, ela tem que durar o tempo que for necessário. Por exemplo se você salvou o dado de um cliente voc6e quer que o dado do cliente fique lá o tempo necessario que voce precisa dele.

### Adicionado uma chave estrangeira

```sql
ALTER TABLE gafanhotos ADD COLUMN cursopreferido int;
```

### Tornando a nova coluna como nossa chave estrangeira

```sql
ALTER TABLE gafanhotos ADD FOREIGN KEY (cursopreferido) REFERENCES cursos(idcurso);
```

### Fazendo o JOIN ou INNER JOIN

```SQL
SELECT g.nome, g.cursopreferido, c.nome, c.nome FROM gafanhotos AS g JOIN cursos AS c ON c.idcurso=g.cursopreferido;
```

NB: Também podemos adicionar o parâmetro `ORDER BY ...` no final do código;

- Definindo a nossa tabela preferencial

```sql
SELECT g.nome, g.cursopreferido, c.nome, c.nome FROM gafanhotos AS g LEFT JOIN cursos AS c ON c.idcurso=g.cursopreferido;
```