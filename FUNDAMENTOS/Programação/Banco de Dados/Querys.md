CREATE DATABASES nomedobanco; -> criando banco de dados

SHOW DATABASES; -> exibir os bancos disponiveis

USE nomedobanco; -> entrando no banco

DROP DATABASE nomedobanco; -> deletando banco de dados


# Tipos de dados

quanto mais especifico for para salvar os dados da maneira correta, mais performace o banco terá

- VARCHAR -> texto de 0 a 65535 caracteres
- TEXT -> texto com até 65535 bytes
-  INT -> numeros inteiros
- BIGINT -> numeros inteiros com proporção maior que o INT
- DATE -> data no fomato YYYY-MM-DD

# Criando tabelas

banco -> tabela -> dados

CREATE TABLE usuarios(
	nome VARCHAR(200),       -> criando uma tabela
	idade INT
);

DESCRIBE usuarios -> exibe a estrutura de uma tabela

DROP TABLE usuarios -> deleta a tabela

## modificando tabelas

ALTER TABLE usuarios ADD id INT; -> adiciona uma coluna

ALTER TABLE usuarios MODIFY COLUMN id VARCHAR(500); -> modifica uma coluna

ALTER TABLE usuarios DROP id; -> remove uma coluna

# Constrains

- caracteristicas que podem ser adicionadas na hora da criação de uma tabela
- podemos definir: campos que nao podem ser nulos, campos unicos, chaves primarias etc

#### NOT NULL

- criando uma tabela com um campo que nao pode ser vazio/nulo

```SQL
CREATE TABLE carro(
	nome VARCHAR(100) NOT NULL,
	banco_couro VARCHAR(100)
);
```

#### UNIQUE

- criando tabela com dados que nao podem ser repetidos e nem nulos e repetidos
```SQL
CREATE TABLE carro(
	nome VARCHAR(100) NOT NULL UNIQUE,
	PLACA VARCHAR(100) UNIQUE
);
```


#### PRIMARY KEY

- uma chave primaria deve ter um valor unico e nao podem ser nulas, geralmente colocadas como ID
- uma tabela possui apenas uma primary key
- ao adicionarmos itens na tabela a primery key vai se adicionar sozinha

```SQL
CREATE TABLE carros(
	id INT UNSIGNED AUTO_INCREMENT PRIMARY KEY,
	nome VARCHAR(255)
);
```
- UNSIGNED(sem sinal) -> apenas numeros positiovos