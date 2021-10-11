# SQL Join - CASE, WHEN, ELSE, INTO

[ ◀ _previous_ ](https://github.com/fegvilela/til/blob/main/sql/09-self-join.md)| [ 🏠 ](https://github.com/fegvilela/til/tree/main/sql)

Estrutura condicional para separarmos os dados em grupos, de acordo com critérios que estabelecemos.

Vamos utilizar novamente o exemplo de cervejas. Queremos classificá-las de acordo com sua data de fabricação (`fab_date`) em `new`, `normal`, `old`

```sql
-- MODELO DA TABELA --
-- -- -- -- -- -- -- --
-------- BEERS ------
--| name    varchar |
--| beer_id     int |
--| city        int |
--| fab_date   date |
----------------------
```

## Utilizando `CASE`, `WHEN`, `ELSE` para categorização

```sql
SELECT name, fab_date
	CASE WHEN fab_date < '2018-01-01' THEN 'old'
			 WHEN fab_date < '2020-01-01' THEN 'normal'
			 ELSE 'new' END
	AS age_group
FROM beers;

```

Também podemos querer criar uma nova tabela (`beers_age`) com essa nova organização dos dados em categorias. Para isso, podemos usar o `INTO`

```sql
SELECT name, fab_date
	CASE WHEN fab_date < '2018-01-01' THEN 'old'
			 WHEN fab_date < '2020-01-01' THEN 'normal'
			 ELSE 'new' END
	AS age_group
FROM beers
INTO beers_age;

```

---

_66 days of data (11/66)_ \
https://campus.datacamp.com/courses/joining-data-in-postgresql/introduction-to-joins?ex=10

---

[ ◀ _previous_ ](https://github.com/fegvilela/til/blob/main/sql/09-self-join.md)| [ 🏠 ](https://github.com/fegvilela/til/tree/main/sql)
