quando acessamos uma pagina com autenticacao HTTP, a autenticacao e feita completamente pelo servidor http e nao interaje com a aplicacao web
![[Pasted image 20251020164814.png]]

quando usamos o curl na pagina temos
![[Pasted image 20251020165015.png]]

e o WWW-authenticate confirma que de fato a pagina usa autenticacao HTTP basica

para fazermos esse login com o cURL podemos fazer

curl -u admin:admin 94.237.53.81:52545

ou pelo navegador

http://admin:admin@94.237.53.81:52545

com o curl -v podemos ver que
![[Pasted image 20251020165400.png]]

o authorization foi definido como Basic YWRtaW46YWRtaW4=
que e a codificacao base 64 de admin:admin

podemo usar isso para nos autenticarmos com o curl

curl -H 'Basic YWRtaW46YWRtaW4=' http://94.237.53.81:52545/

a aplicacao em questao procura por nomes de cidades, quando passamos um nome de cidade ele faz uma requisicao com uma query string
![[Pasted image 20251020170251.png]]

nos podemos usarmos o curl para obtermos o mesmo resultado
![[Pasted image 20251020170309.png]]

![[Pasted image 20251020180329.png]]

