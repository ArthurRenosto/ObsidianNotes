A maioria dos aplicativos web sao desenvolvidos utilizando algum framework web

- Laravel (PHP)
- Express (Node.JS)
- Django (python)
- Rails (Ruby)

Muitas aplicacoes web hj em dia utilizam mais de um framework

# APIs

Componente do front end utiliza uma API para pedir ao back-end que realize alguma tarefa especifica, back-end processa essa tarefa e retorna

## Parametros de consulta (Query Parameters)

Usamos GET e POST para permitir que o front-end passe valores especificos para um parametro do back end

Exemplo

/search.php leva um parametro na query string como
/search.php?item=apple

# APIs da Web

Uma API (Application Programming Interface)

Um aplicativo web meteorológico, por exemplo, pode ter uma determinada API para recuperar o tempo atual para uma determinada cidade. Podemos solicitar a URL da API e passar o nome da cidade ou o id da cidade, e ele retornaria o clima atual em um `JSON`objeto. Outro exemplo é a API do Twitter, que nos permite recuperar os Tweets mais recentes de uma determinada conta em `XML`ou `JSON`formatos, e até mesmo nos permite enviar um Tweet 'se autenticado', e assim por diante.

Para permitir o uso de APIs dentro de um aplicativo da Web, os desenvolvedores precisam desenvolver essa funcionalidade no back-end do aplicativo da Web usando os padrões da API como `SOAP`ou `REST`.

# SOAP (Simple Objects Access)

Tanto o request como o response sao feitos pedindo e retornando em XML

```xml
<?xml version="1.0"?>

<soap:Envelope
xmlns:soap="http://www.example.com/soap/soap/"
soap:encodingStyle="http://www.w3.org/soap/soap-encoding">

<soap:Header>
</soap:Header>

<soap:Body>
  <soap:Fault>
  </soap:Fault>
</soap:Body>

</soap:Envelope>
```

# REST

O REST (Representation State Transfer) compartilha dados atraves de URL (search/user/1) e retorna os dados em JSON

As APIs rest geralmente sao utilizadas para dados search, sort ou filter.

As requests a APIs rest sao feitas em json

Resposta ao GET /category/posts:
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


`REST`usa vários métodos HTTP para executar diferentes ações na aplicação web:

- `GET`solicitação para recuperar dados
- `POST`solicitação para criar dados (não-idempotentes)
- `PUT`solicitação para criar ou substituir dados existentes (idempotente)
- `DELETE`solicitação para remover dados