# Introdução ao SQL - Agrupando resultados

(`ORDER BY`, `HAVING`)

[◀ _previous_](https://github.com/fegvilela/til/blob/main/sql/06-sorting.md) | [ _next_ ▶️ ](https://github.com/fegvilela/til/blob/main/sql/08-inner-join.md)| [ 🏠 ](https://github.com/fegvilela/til/tree/main/sql)

Geralmente, usa-se `GROUP BY` com funções de agregação

## Agrupando por característica/campo

```sql

SELECT breed, COUNT(name)
FROM dogs
GROUP BY breed;

--- resultado ----
breed       count
...          ...
dalmata      50
daschund     100
...          ...
```

## Usando ordenação e agrupamento

```sql
SELECT breed, COUNT(name)
FROM dogs
GROUP BY breed
ORDER BY breed DESC;

--- resultado ---
breed       count
...          ...
daschund     100
dalmata      50
...          ...
```

## Selecionando e filtrando dados com agrupamento

```sql
SELECT user_type, COUNT(first_name) AS total_users
FROM users
WHERE created_at > '2020-12-01'
GROUP BY user_type;

--- resultado ---
user_type      total_users

admin             5
user             200
```

## Agrupando e usando funções de agregação como filtros (`HAVING`)

Para usar funções de agregação como filtro, precisamos usar o `HAVING` ao invés de `WHERE`

```sql
SELECT label
FROM albums
GROUP BY label
HAVING COUNT(grammy_awards) > 3;

--- resultado ---
vai mostrar as labels que possuem mais do que 3 albums premiados pelo grammy
```

---

_66 days of data (8/66)_ \
https://campus.datacamp.com/courses/introduction-to-sql/sorting-and-grouping?ex=6

---

[◀ _previous_](https://github.com/fegvilela/til/blob/main/sql/06-sorting.md) | [ _next_ ▶️ ](https://github.com/fegvilela/til/blob/main/sql/08-inner-join.md)| [ 🏠 ](https://github.com/fegvilela/til/tree/main/sql)
