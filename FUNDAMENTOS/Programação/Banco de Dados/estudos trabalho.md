
# Criando Usuarios

 - criando um usuario no banco de dados e setando a senha
 
```sql
CREATE USER 'balio'@'localhost' IDENTIFIED BY 'kali';
```

- definindo todos os privilegios para o usuario

```sql
GRANT ALL PRIVILEGES ON *.* 'balio'@'localhost';
```

- limpando o cache

```sql
FLUSH PRIVILEGES;
```

# msqli

- Extensao do propio PHP 
- Mais rapida que o PDO

# PDO

- API para conexao de banco de dados nao limitada ao MySQL
- 