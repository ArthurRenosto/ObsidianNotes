# APIs REST

| Parâmetro                      | Descrição                                                      | Exemplo                                   |
| ------------------------------ | -------------------------------------------------------------- | ----------------------------------------- |
| Consulta de parâmetros         | query string                                                   | /users?limit=10&sort=name                 |
| Parâmetros do caminho          | usado na url do end-point para identificar recuros especificos | /products/{id}pen_spark                   |
| Solicitar Parâmetros Corporais | Enviado no corpo de solicitações                               | { "name": "New Product", "price": 99.99 } |
## API Documentation
- Consultar a documentação da API
- Lista de end-points disponíveis, parâmetros, formatos

## Analise de Trafego
- Analisar as requests da API com um proxy

## Fuzzing
- Fuzzing de parâmetros

# APIs SOAP
- Depende de mensagens baseadas em  XML
- Único end-point que recebe as requests
- O conteúdo da mensagem especifica a ação
- Parâmetros definidos no corpo da mensagem em um documento XML
- Os parâmetros são definidos pelo WSDL

## Analise de WSDL
- Operações disponíveis (endpoints)
- Analise de arquivos WSDL

## Analise de Trafego
- Analisar as requests da API com um proxy

## Fuzzing
- Fuzzing de parâmetros

# API GraphQL
- Possui um end-point /graphql para todas as consultas na API

| Componente        | Descrição                                | Exemplo               |
| ----------------- | ---------------------------------------- | --------------------- |
| Campo             | dado a ser recuperado                    | name, email           |
| Relação           | Conexão entre diferentes tipos de dados  | posts                 |
| Objetivo alinhado | Um campo que retorna outro objeto        | posts { title, body } |
| Argumento         | Modifica o comportamento de uma consulta | posts(limit: 5)       |
```graphql
query {
  user(id: 123) {
    name
    email
    posts(limit: 5) {
      title
      body
    }
  }
}
```
- Consultamos informações sobre um `user`com o ID 123.
- Solicitamos o seu `name`e `email`.
- Também buscamos os seus primeiros 5 `posts`, incluindo o `title`e `body`de cada post.

# Introspection
- Ferramenta para descoberta

## API Documentation
- Consultar a documentação da API
- Lista de end-points disponíveis, parâmetros, formatos

# API GraphQL
- Possui um end-point /graphql para todas as consultas na API

# Tipos de Fuzzing em APIs

## Parameter Fuzzing
- Testar diferentes valores para parâmetros
- Parâmetros de consulta na URL do end point
- Cabeçalhos
- Corpo

## Data Format
- Fuzzing de JSON e XML

## Sequence Fuzzing
- Mostra vulnerabilidades como
- Race condition
- IDOR
- Desvios de autorizaçãow