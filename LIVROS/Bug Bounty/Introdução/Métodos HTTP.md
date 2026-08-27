Os métodos são utilizados nas requisições que o cliente faz ao servidor, eles variam de acordo com a ação que se deseja realizar sobre determinado recurso.

GET -> Solicita Dados de um servidor, como dar um GET em uma imagem, aquela imagem vai ser carregada, o GET em uma pagina, ela vai ser carregada. Ele é feito via URL

POST - Envia dados ao servidor, porem via Cabeçalho, então todas as informações que ele quer enviar, são enviadas via cabeçalho 

DELETE - Remove um recurso específico, se eu quiser deletar algo em um servidor e ele tem o delete aberto, pode ser usado 

PUT - Cria ou substitui um recurso em um servidor, então eu tenho um dado e quero substituir ele por outra informação, pode ser usado o 

PUT OPTIONS - Verifica quais as opções de requisição que são permitidas pelo servidor, pode ser especificado por uma URL ou usado um * para indicar o servidor todo 

HEAD - Solicita as informações de cabeçalho. Nem todo servidor faz isso, nem todo http, nem toda comunicação cliente-servidor, vai ser possivel ves esses métodos