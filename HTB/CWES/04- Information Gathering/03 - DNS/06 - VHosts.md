Servidores HTTP podem hospedar diversas aplicações que compartilham o mesmo IP e distingui-las com VHosts.

# Como Funciona

VHosts é a capacidade do servidor web de distinguir varios sites/aplicações que compartilham o mesmo endereço IP, para isso eles usam o header host na request HTTP.

# VHosts != Subdomínios

- Subdomínios
	- Extensões de um nome de dominio principal
	- Usado para separar diferentes sessões ou funcionalidades
	- Tem seu propio DNS Record apontando para o mesmo endereço IP que é o domain principal
- Virtual Hosts
	- Varios sites em um mesmo servidor
	- Podem ser associados ao domain principal ou ao subdomain


Se um VHost não tiver registro dns é possível acessa-lo 9definindo o IP manualmente no arquivo hosts ([[01 - Introdução ao DNS]]). 

# VHosts Lookup

![[Pasted image 20251215233749.png]]

## (1) HTTP Request 
- Você pesquisa o nome do domínio no navegador

## (2) Host Header
- Navegador inclui o domínio no Host Header da request

## (3) Servidor HTTP
- Verifica o header host
- Verifica a configuração de VHosts

## (4) HTTP Response
- Recupera os arquivos do document root (diretório raiz do site)
- Encaminha o conteúdo front end

# Tipos de VHost

## Name-Based
- Distingue os sites pelo domínio passado no Host Header

## IP-Based
- Atribui um IP para cada site, não depende do host header

## Port-Based
- Atribui uma porta para cada site
- Exige especificar numero da porta na URL

# Enumerando VHosts
[[07 - Enumeração de Subdomínios e VHosts]]
