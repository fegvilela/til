# OLAP vs OLTP

Esses são dois tipos de sistemas fundamentais para processamento e persistência de dados em um banco de dados.
Basicamente, são duas formas diferentes de desenhar como vão ser as bases de dados do sistemas, levando em conta o tipo de utilização mais frequente, o que está ligado diretamente às regras de negócio.

## OLTP

*OLTP = Online Transacation Processing* \
Sistemas que utilizam a abordagem OLTP são orientados à transação, sua captura e persistência. O foco da OLTP é em processamento rápido, é um banco de dados com CRUD completo.
Portanto, esse tipo de abordagem é mais usado em sistemas com caráter **operacional**.

## OLAP
*OLAP = Online Analytical Processing* \
Sistemas que utilizam OLAP são orientados à análise, então possuem um foco histórico. A maioria das operações desse banco de dados é de *select* e costuma possuir queries mais pesadas e complexas, com funções de agregação em muitas linhas da tabela.
Portanto, esse tipo de abordagem é mais usado em sistemas com caráter **analítico**.