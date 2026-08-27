Sao executados em algum servidor de back-end
sao responsaveis por lidar com requisicoes HTTP
Sao executados geralmente na porta 80(HTTP) ou 443(HTTPS)

# workflow

funciona com uma request do client e uma resposta

![[Pasted image 20251107011648.png]]

ele aceita entradas do usuario como jsons, strings, arquivos e fotos.

Responsavel por rotear o trafego do cliente para o destino final, como por exemplo:

quando o usuario acessa www.jorge.com/conta

o diretorio /conta fica dentro da aplicacao web, e o servidor web apenas leva a solicitacao get ate la e faz a captura do conteudo, devolvendo ele para o user na response


## Status Code HTTP

- Resposta de informação(100-199)
    
- Respostas de sucessos(200-299)
    
- Redirecionamentos(300-399)
    
- Erros do Cliente(400-499)
    
- Erros do Servidor(500-599)


# Tipos de servidores web

Apache: 
- usado em 40% de todos os servidores da internet
- vem instalado por padrao na maioria dos linux mas pode ser usado no win e mac
- Por padrao e usado com PHP mas suporta .net, python, pearl, bash

NGINX:
- usado em 30% de todos os servidores web do mundo
- Atende multiplas solicitacoes simultaneamente, utlizando de arquitetura assincrona para isso
- Muito confiavel e utlizado em sites com muito trafego

IIS (Internet Information Service):
- usado em 15%
- mantido pela microsoft
- usado principalmente em windows server e aplicacos .net
- otimizado para active directory
- inclui windows auth para autenticar usuarios usando o AD em aplicacoes web

Apache Tomcat: java
Node.JS: Javascript