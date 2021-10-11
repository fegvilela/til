# Introdução ao SQL - Selecionando colunas

[ _next_ ▶️ ](https://github.com/fegvilela/til/blob/main/sql/02-filtering-rows-pt1.md) | [ 🏠 ](https://github.com/fegvilela/til/tree/main/sql)

SQL = **S**tructured **Q**uery **L**anguage

## Selecionando uma única coluna

```sql
SELECT name
FROM films;
```

## Selecionando múltiplas colunas

```sql
SELECT name, director
FROM films;
```

## Selecionando todas colunas

```sql
SELECT *
FROM films;
```

## Selecionando dados de uma coluna que sejam distintos entre si

Esse comando permite com que você não tenha repetição de dados. Por exemplo, existem vários filmes do mesmo diretor, então, para saber apenas os diretores contidos naquela tabela (sem repetição), podemos usar esse comando.

```sql
SELECT DISTINCT director
FROM films;
```

## Contando dados

- Todos os registros de uma tabela

```sql
SELECT COUNT(*)
FROM films;
```

- Todos os registros não-nulos de uma coluna

```sql
SELECT COUNT(release_year)
FROM films;
```

- Todos os registros distintos entre si de uma colunas

```sql
SELECT COUNT(DISTINCT director)
FROM films;
```

---

_66 days of data (2/66) \
https://campus.datacamp.com/courses/introduction-to-sql/filtering-rows?ex=1_

---

[ _next_ ▶️ ](https://github.com/fegvilela/til/blob/main/sql/02-filtering-rows-pt1.md) | [ 🏠 ](https://github.com/fegvilela/til/tree/main/sql)
