# Introdução ao SQL - Funções de agregação pt.1

(`AVG`, `MAX`, `MIN`, `SUM`)

[◀ _previous_](https://github.com/fegvilela/til/blob/main/sql/03-filtering-rows-pt2.md) | [ _next_ ▶️ ](https://github.com/fegvilela/til/blob/main/sql/05-aggregate-functions-pt2.md)| [ 🏠 ](https://github.com/fegvilela/til/tree/main/sql)

## Soma

```sql
SELECT SUM(budget)
FROM projects;
```

## Máximo

```sql
SELECT MAX(age)
FROM people
WHERE city = 'London';
```

## Mínimo

```sql
SELECT MIN(release_year)
FROM albums
WHERE artist = 'Prince';
```

## Média

```sql
SELECT AVG(score)
FROM cartoons;
```

---

_66 days of data (5/66)_ \
https://campus.datacamp.com/courses/introduction-to-sql/aggregate-functions?ex=5

---

[◀ _previous_](https://github.com/fegvilela/til/blob/main/sql/03-filtering-rows-pt2.md) | [ _next_ ▶️ ](https://github.com/fegvilela/til/blob/main/sql/05-aggregate-functions-pt2.md)| [ 🏠 ](https://github.com/fegvilela/til/tree/main/sql)
