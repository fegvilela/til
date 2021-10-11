# SQL Join - Self-join usando INNER JOIN

[◀ _previous_](https://github.com/fegvilela/til/blob/main/sql/08-inner-join.md) | [ _next_ ▶️ ](https://github.com/fegvilela/til/blob/main/sql/10-case%2Cwhen%2Celse%2Cinto.md)| [ 🏠 ](https://github.com/fegvilela/til/tree/main/sql)

Usamos `self join` quando os dados de uma tabela referenciam dados nela mesma. Alguns exemplos de aplicação:

- buscar dados hierárquicos (contidos na mesma tabela)
- comparação entre linhas da tabela

## Buscar dados hierárquicos

```sql
-- MODELO DA TABELA --
-- -- -- -- -- -- -- --
-------- STAFFS ------
--| name     varchar |
--| staff_id     int |
--| manager_id   int |
----------------------

SELECT
    e.name as employee,
    m.name as manager
FROM
    staffs as e
INNER JOIN staffs as m ON m.staff_id = e.manager_id
ORDER BY
    manager;
```

## Comparação entre linhas

```sql
-- MODELO DA TABELA --
-- -- -- -- -- -- -- --
-------- BEERS ------
--| name    varchar |
--| beer_id     int |
--| city        int |
----------------------

SELECT
    b1.city,
    b1.name beer_1,
    b2.name beer_2
FROM
    beers b1
INNER JOIN beers b2 ON b1.beer_id > b2.beer_id
AND b1.city = b2.city
ORDER BY
    city,
    beer_1,
    beer_2;
```

nesse caso, usamos `>` ao invés de `<>` para que não venham dados duplicados pela combinação entre `beer_1` e `beer_2`, por exemplo

```sql
--   city   |   beer_1   |   beer_2   --
-- Brasília |     143    |    12
-- Brasília |     12     |    143
```

---

_66 days of data (10/66)_ \
 https://campus.datacamp.com/courses/joining-data-in-postgresql/introduction-to-joins?ex=9

---

[◀ _previous_](https://github.com/fegvilela/til/blob/main/sql/08-inner-join.md) | [ _next_ ▶️ ](https://github.com/fegvilela/til/blob/main/sql/10-case%2Cwhen%2Celse%2Cinto.md)| [ 🏠 ](https://github.com/fegvilela/til/tree/main/sql)
