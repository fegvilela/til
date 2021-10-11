# Introdução ao SQL - Alias e operações aritméticas (float vs int)

[◀ _previous_](https://github.com/fegvilela/til/blob/main/sql/04-aggregate-functions-pt1.md) | [ _next_ ▶️ ](https://github.com/fegvilela/til/blob/main/sql/06-sorting.md)| [ 🏠 ](https://github.com/fegvilela/til/tree/main/sql)

## Utilizando alias (`AS`) e operações aritméticas

```sql
SELECT MAX(age) - MIN(age) AS age_difference
FROM people;
```

## Operações com float ou inteiro

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

---

_66 days of data (6/66)_ \
https://campus.datacamp.com/courses/introduction-to-sql/aggregate-functions?ex=6

---

[◀ _previous_](https://github.com/fegvilela/til/blob/main/sql/04-aggregate-functions-pt1.md) | [ _next_ ▶️ ](https://github.com/fegvilela/til/blob/main/sql/06-sorting.md)| [ 🏠 ](https://github.com/fegvilela/til/tree/main/sql)
