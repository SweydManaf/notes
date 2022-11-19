# INNER JOIN com várias tabelas

Tendo duas tabelas com relação N-N para fazermos o INNER JOIN precisaremos de mais uma tabela

```sql
CREATE TABLE gafanhoto_assiste_curso (
    id int not null auto_increment,
    data date,
    idgafanhoto int,
    idcurso int,
    PRIMARY KEY(id),
    FOREIGN KEY (idgafanhoto) REFERENCES gafanhotos(id),
    FOREIGN KEY (idcurso) REFERENCES cursos(idcurso)
)  DEFAULT charset=utf8;
```

Visualizando os dados N-N

```SQL
SELECT g.nome, c.nome FROM gafanhotos g join gafanhoto_assiste_curso a 
on g.id=a.idgafanhoto JOIN cursos c ON c.idcurso=a.idcurso ORDER BY g.nome;
```