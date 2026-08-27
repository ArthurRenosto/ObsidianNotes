para solicitarmos um recurso ou fazermos alguma pesquisa usamos GET, mas sempre que precisamos enviar algum dado, arquivo usamos o POST

GET coloca paramertros de usuario dentro de URL

POST coloca parametros dentro do corpo da requisicao

- Lack of Logging(Falta de registro): se fosse carregado um arquivo por uma requisicao GET ao inves de carregado pelo post, ele teria que ser enviado na URL e nao seria eficiente
  
solicitacao POST com o cURL
curl -X POST -d 'username=admin&password=admin' http://94.237.48.51:39768/index.php

podemos logar na pagina e vermos que estamos autenticados vendo o cod html

![[Pasted image 20251028173151.png]]
alterando o valor do cookie para login
![[Pasted image 20251028174303.png]]