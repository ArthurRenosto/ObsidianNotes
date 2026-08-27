Sao bancos de dados que rodam em um servidor back-end

armazena arquivos, imagens, senhas, logins, usuarios

o banco de dados escolhido para a aplicacao depende da:
velocidade
tamanho
escalabilidade
custo

# Relacional(SQLq)

Bancos de dados relacionais funcionam com tabelas que possuem linhas e colunas, cada tabela pode ter um ID unico assim podendo vincular tabelas a outras tabelas

![[Pasted image 20251107112824.png]]

a tabela users possui:
- id (identificador unico de cada user)
- username, first_name e last_name

a tabela posts possui:
- id (idenficador unico de cada post)
- user id (podem ter varios, pois um unico user pode fazer varios posts)
- data
- conteudo do post

com essa vinculacao do id da tabela users para o user_id na tabela posts, podemos recuperar os detalhes do user sem precisarmos passar todos esses dados novamente

tambem e possivel usar o id da tabela posts para relacionar ela com uma tabela contendo comentarios

*a relacao entre tabelas e chamada de schema*

isso torna possivel por exemplo, recuperar os dados de um usuario de todas as tabelas

- MySQL
- MSSQL
- Oracle
- PostgreSQL
- SQLite
- MariaDB
- Amazon Aurora
- Azure SQL

# Nao relacionais (NoSQL)

Bancos de dados nao relacionais nao usam tabelas, linhas,colunas, chaves primarias etc.

Modelos comuns para armazenamento em NoSQL:

- valor-chave (key-Value)
- baseado em documentos
- grande coluna
- grafico

cada modelo possui uma maneira diferente de armazenar dados.
No exemplo do Key-Value, geralmente em json ou XML:

```json
{
  "100001": {
    "date": "01-01-2021",
    "content": "Welcome to this web application."
  },
  "100002": {
    "date": "02-01-2021",
    "content": "This is the first post on this web app."
  },
  "100003": {
    "date": "02-01-2021",
    "content": "Reminder: Tomorrow is the ..."
  }
}
```

Bancos de dados NoSQL
- MongoDB
- ElasticSearch
- Apache Cassandra
- Redis
- Neo4j
- CouchDB
- Amazon DynamoDB
- Firebase Database do Google

# uso em aplicacoes web

Com PHP e MySQL

```php
$conn = new mysqli("localhost", "user", "pass");
```

Criando novo banco de dados

```php
$sql = "CREATE DATABASE database1";
$conn->query($sql)
```

conectamos no banco de dados e usamos MySQL sintaxe
```php
$conn = new mysqli("localhost", "user", "pass", "database1");
$query = "select * from table_1";
$result = $conn->query($query);
```

os aplicativos web usam entradas do usuario para recuperar dados do banco de dados
exemplo buscando por usuarios
```php
$searchInput =  $_POST['findUser'];
$query = "select * from users where name like '%$searchInput%'";
$result = $conn->query($query);
```

devolvendo resultado para user
```php
while($row = $result->fetch_assoc() ){
	echo $row["name"]."<br>";
}
```

