API sao usadas para interagir com as tabelas do banco de dados, especificamos a tabela e linha, e usamos um metodo HTTP para realizamos a acao que queremos.

Exemplo atualizando a tabela City, e a linha london

curl -X PUT http://sitegamer.com/api.php/city/london

CRUD

Operacaoes que podemos fazer com o HTTP no banco de dados

| operacao | metodo | descicao                                       |
| -------- | ------ | ---------------------------------------------- |
| Create   | POST   | adiciona dados em uma tabela do banco de dados |
| Read     | GET    | Le a entidade especificada no banco de dados   |
| Update   | PUT    | atualiza determinada tabela do banco de dados  |
| Delete   | DELETE | remove a linha especificada do banco de dados  |

# READ

![[Pasted image 20251028200548.png]]
![[Pasted image 20251028200622.png]]

# CREATE

![[Pasted image 20251028201002.png]]

# UPDATE

![[Pasted image 20251028201820.png]]

estamos na linha london do json, logo os parametros que estamos passando para atualizacao, vao subistituir ela

# DELETE

![[Pasted image 20251028202215.png]]

deletamos a cidade especificada