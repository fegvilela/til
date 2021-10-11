# Introdução ao SQL - Filtrando linhas das tabelas - pt.2

(`IN`, `OR`, `BETWEEN`, `NULL`, `LIKE`)

[◀ _previous_](https://github.com/fegvilela/til/blob/main/sql/02-filtering-rows-pt1.md) | [ _next_ ▶️ ](https://github.com/fegvilela/til/blob/main/sql/04-aggregate-functions-pt1.md)| [ 🏠 ](https://github.com/fegvilela/til/tree/main/sql)

## Filtrando linhas que contenham ao menos um dos valores (`OR`, `IN`)

```sql
SELECT title, author
FROM books
WHERE (publisher = 'Happer Collins' OR publisher = 'Cia das Letras');
```

Quando se tem muitas opções para `OR`, pode-se usar `IN`

```sql
Não faça assim:

SELECT title, author
FROM books
WHERE published_year = 1990
OR published_year = 1980
OR published_year = 1970
OR published_year = 1960;

Faça assim:

SELECT title, author
FROM books
WHERE published_year IN (1990, 1980, 1970, 1960);
```

## Filtrando por valores em um _range_ (`BETWEEN`)

Ou quando as opções são sequenciais entre dois valores, pode-se usar `BETWEEN`

```sql
Não faça assim:

SELECT title, author
FROM books
WHERE published_year >= 1990 AND published_year < 2000;

Faça assim:

SELECT title, author
FROM books
WHERE published_year BETWEEN 1990 AND 1999;
```

- `BETWEEN` é uma operação **inclusiva** então, incluiu os valores estabelecidos

## Filtrando por valores que são nulos (`IS NULL`)

No exemplo, queremos pessoas que não possuem animais de estimação

```sql
SELECT *
FROM people
WHERE pets IS NULL;
```

## Filtrando por valores usando padrões, ao invés de um valor específico (`LIKE`, `NOT LIKE`, `%` , `_`)

Podemos usar uma parte do texto que queremos e os _wildcards(_`%` e `_`) nos ajudam a encontrar determinados padrões.

`%` : vai procurar pela palavra exata ou por outras que comecem com essa palavra

```sql
SELECT breed
FROM dogs
WHERE breed LIKE 'Da%';

resultado
-----------------
Dalmata
Daschund
```

`_`: vai procurar pela palavra, aceitando qualquer letra no lugar desse _wildcard_

```sql
SELECT name
FROM dogs
WHERE name LIKE 'Nin_';

resultado
-----------------
Nina
Nini
Nino
```

O comando `NOT LIKE` vai filtrar por todos valores que não apresentam aquele padrão

---

_66 days of data (4/66)_ \
https://campus.datacamp.com/courses/introduction-to-sql/filtering-rows?ex=6

---

[◀ _previous_](https://github.com/fegvilela/til/blob/main/sql/02-filtering-rows-pt1.md) | [ _next_ ▶️ ](https://github.com/fegvilela/til/blob/main/sql/04-aggregate-functions-pt1.md)| [ 🏠 ](https://github.com/fegvilela/til/tree/main/sql)
