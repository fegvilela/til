# SEVEN

Daily overview: Ordenando resultados

LINK: https://campus.datacamp.com/courses/introduction-to-sql/sorting-and-grouping?ex=4

Learning: SQL

Productiveness: ⭐️⭐️⭐️⭐️

Status: In progress

# Introdução ao SQL - Ordenando resultado

(`ORDER BY`)

### Ordenando resultados com base em uma coluna

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

### Ordenando resultados com base em múltiplas colunas

Pode-se utilizar a ordenação por mais de uma coluna, nesse caso, a ordenação respeitará a ordem das colunas apresentadas na *query*

```sql
SELECT release_year, album, artist
FROM songs
WHERE artist = 'Nirnava' OR artist = 'Pearl Jam'
ORDER BY release_year, album;

---- resultado -----

release_year     album        artist
    ...           ...           ...
    1991        Nevermind     Nirvana   
    1991          Ten        Pearl Jam
    ...           ...           ...
```
