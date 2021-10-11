# Introdução ao SQL | Filtrando linhas das tabelas - pt.1

[◀ _previous_](https://github.com/fegvilela/til/blob/main/sql/01-selecting-columns.md) | [ _next_ ▶️ ](https://github.com/fegvilela/til/blob/main/sql/03-filtering-rows-pt2.md) | [ 🏠 ](https://github.com/fegvilela/til/tree/main/sql)

Para isso, usamos o comando `WHERE` , podemos filtrar por valores de texto ou numéricos utilizando os **seguintes operadores**

```sql
= igual
<> diferente
< menor que
> maior que
<= menor ou igual que
>= maior ou igual que
```

O `WHERE` sempre vem depois do `FROM`

## Filtrando por um valor (`WHERE`)

```sql
SELECT *
FROM songs
WHERE release_year > 2010;
```

## Filtrando por mais de um valor (`WHERE` `AND`)

```sql
SELECT *
FROM songs
WHERE artist = 'Phil Collins'
AND release_year > 2000
AND release_year < 2020;
```

Lembrar que o nome do campo deve ser repetido a cada "valor a ser filtrado"

```sql
Deve ser:
...
AND release_year > 2000
AND release_year < 2020;

e não:
...
AND release_year > 2000 AND < 2020;
```

## Filtrando linhas e selecionando colunas

```sql
SELECT name, album
FROM songs
WHERE artist = 'Wallows';
```

## Filtrando linhas e contando o número de registros

```sql
SELECT COUNT(*)
FROM songs
WHERE rating > 8
AND release_year > 2018;
```

---

_66 days of data (3/66)_ \
https://campus.datacamp.com/courses/introduction-to-sql/filtering-rows?ex=5

---

[◀ _previous_](https://github.com/fegvilela/til/blob/main/sql/01-selecting-columns.md) | [ _next_ ▶️ ](https://github.com/fegvilela/til/blob/main/sql/03-filtering-rows-pt2.md) | [ 🏠 ](https://github.com/fegvilela/til/tree/main/sql)
