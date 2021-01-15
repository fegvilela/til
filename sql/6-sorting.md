# SEVEN

Daily overview: Ordenando resultados

LINK: https://campus.datacamp.com/courses/introduction-to-sql/sorting-and-grouping?ex=4

Learning: SQL

Productiveness: ⭐️⭐️⭐️⭐️

Status: In progress

# Introdução ao SQL - Ordenando resultado

(`ORDER BY`)

### Ordenando um resultado com base em alguma coluna

```sql
SELECT first_name
FROM people
WHERE age BETWEEN 20 AND 30
ORDER BY birthdate;
```

Para ordenar de modo decrescente, usando apenas uma coluna como referência (`DESC`)

```sql
SELECT *
FROM beers
WHERE type = 'IPA'
ORDER BY brewing_date DESC;

---- resultado -----
dado com brewing_date mais atual...
.
.
.
dado com brewing_date mais antiga
```
