# SIX

Daily overview: alias, inteiros e floats

LINK: https://campus.datacamp.com/courses/introduction-to-sql/aggregate-functions?ex=6

Learning: SQL

Productiveness: ⭐️⭐️⭐️

Status: In progress

# Introdução ao SQL - Alias e operações aritméticas (float vs int)

### Utilizando alias (`AS`) e operações aritméticas

```sql
SELECT MAX(age) - MIN(age) AS age_difference
FROM people;
```

### Operações com float ou inteiro

Ao fazer alguma operação, caso você use um inteiro dividido por um inteiro, por exemplo, o resultado retornado será um inteiro

```sql
SELECT 45 / 10;
--- resultado ----
4

SELECT 45 / 10 * 100.0;
--- resultado ----
400.0000

```

Ao fazer alguma operação com float, o resultado retornado é um float

```sql
SELECT 45 * 100.0;
---- resultado ----
4500.0000

SELECT 45 * 100.0 / 10
--- resultado ----
450.00000
```
