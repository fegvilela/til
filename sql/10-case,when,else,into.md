# ELEVEN

Daily overview: case, when, else, into (categorização)
LINK: https://campus.datacamp.com/courses/joining-data-in-postgresql/introduction-to-joins?ex=10
Learning: SQL
Productiveness: ⭐️⭐️⭐️
Status: Complete

# SQL Join - CASE, WHEN, ELSE, INTO

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

### Utilizando CASE, WHEN, ELSE para categorização

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