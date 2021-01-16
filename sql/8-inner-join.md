# NINE

Daily overview: inner join
LINK: https://campus.datacamp.com/courses/joining-data-in-postgresql/introduction-to-joins?ex=1
Learning: SQL
Productiveness: ⭐️⭐️⭐️⭐️⭐️
Status: Complete

# SQL Join - INNER JOIN

Essa operação serve para "juntar" tabelas, baseando-se em um ou mais "valores-chave" que relacionam as tabelas.

Vamos usar essa estrutura de dados relacional para os exemplos. 

![https://relational.fit.cvut.cz/assets/img/datasets-generated/university.svg](https://relational.fit.cvut.cz/assets/img/datasets-generated/university.svg)

### Com uma tabela

```sql
SELECT prof_id, popularity, salary
FROM prof AS p
INNER JOIN RA AS r
ON p.prof_id = r.prof_id
```

- É uma *boa prática* usar **alias** para todas as tabelas quando usamos `INNER JOIN`, sendo a primeira letra do nome da tabela. Ex. `prof AS p`

Nos casos em que temos o valor-chave com nome igual em ambas tabelas, podemos usar `USING`

ao invés de `ON`

```sql
SELECT prof_id, popularity, salary
FROM prof AS p
INNER JOIN RA AS r
USING (prof_id);
```

### Com múltiplas tabelas

```sql
SELECT intelligence, diff AS course_difficulty, r.grade
FROM registration AS r
INNER JOIN student AS s
USING (student_id)
INNER JOIN course AS c
USING (course_id);
  
```

- Quando temos **mais do que um valor-chave** entre as tabelas e estamos trabalhando com `INNER JOIN` de múltiplas tabelas, precisamos usar `ON` com todos esses valores-chave.