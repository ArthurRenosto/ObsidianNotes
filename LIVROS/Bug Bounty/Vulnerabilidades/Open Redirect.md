O open redirect é uma vulnerabilidade que ocorre quando os usuários visitam um site, e são redirecionados para outra URL, ele explora a confiança que os usuários possuem em determinado domínio para atrai-los para um domínio malicioso, assim permitindo combinar o open redirect com uma pagina de phishing, ou permitir que os atacantes espalhem malwares.
# Como Funciona

Ocorre quando a aplicação usa os dados fornecidos pelo usuário para redirecionar o navegador para outra pagina. 

Geralmente acontece quando o destino do redirecionamento é passado na URL, por tags de atualização HTML como <meta> ou pelo JS da aplicação, utilizando da DOM window location.

A maioria dos sites redirecionam seus usuários intencionalmente, após telas de login, anúncios e etc. Normalmente é feito pela URL, onde é passado a URL de destino na URL original, para informar ao navegador que faça uma requisição GET no domínio especificado.

```
https://www.google.com/?redirect_to=https://www.gmail.com
```

No exemplo acima, está sendo feito uma request com o método GET, usando o valor do redirect_to para determinar para onde a aplicação do Google deve direcionar o navegador.

Após isso o servidor encaminha a response, que contém o status code dizendo que a pagina foi encontrada e que o navegador deve redirecionar o usuário, fazendo uma requisição GET no valor do parâmetro redirect_to. O status code geralmente é 302, mas pode variar entre 301, 303, 307 e 308. O valor https://www.gmail.com é indicado no cabeçalho Location.

```
https://www.google.com/?redirect_to=https://www.ovorobasuaconta.com
```

No exemplo acima temos uma URL adulterada por um atacante, se o Google não validar se o valor do redirect_to se refere a um de seus sites legítimos, o atacante pode redirecionar a vitima para um site malicioso e realizar outros ataques.

# Parâmetros de Redirecionamento

Ao procurar por vulnerabilidades de open redirect é de extrema importancia ficar atento a URLs que incluem:

- url=
- redirect=
- next=
- returnTo=
- goto=
- rurl=
- destination=
- continue=
- target=
- dest=
- redir=
- redirectTo=
- back=
- forward=
- path=
- link=
- location=
- to=
- out=

E assim sucessivamente. É importante ressaltar que nem sempre os parâmetros de redirecionamento terão nomes tao óbvios, em alguns casos podem ser rotulados, como **r=** ou **u=.**

É possível também utilizar de google dorks para encontrar parastemos em um site específicos

site: google.com | inurl:url | inurl:redirect | inurl:returm | inurl:src=http | inurl:r=http
# Tags HTML

A tag HTML <meta> pode instruir o navegador a redirecionar o usuário, para a URL definida no atributo content da tag:

<meta http-equiv="refresh" content="0; url=https://www.google.com/">

a tag content possui 2 parametros, o tempo que o navegador ira demorar para redirecionar o user, e a URL para qual sera feito o redirecionamento

# JS

O atacante pode modifical a propiedade location da janela, que indica para onde o navegador deve redirecionar o usuario, isso pode ser feito por meio do DOM.

O DOM é uma API para documentos HTML e XML que permite aos desenvolvedores
modificar a estrutura, o estilo e o conteúdo de uma página web.

window.location = https://www.google.com/
window.location.href = https://www.google.com
window.location.replace(https://www.google.com)

Normalmente o valor do window.location pode ser alterado quando o invasor pode executar codigo JS na pagina por meio de XSS

# Em resumo

Ao procurar por vulnerabilidades de open redirect, normalmente será monitorado as requisições com burp, em busca de um GET que inclui o redirecionamento na URL