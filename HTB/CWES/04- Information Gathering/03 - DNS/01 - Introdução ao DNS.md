O Domain Name System traduz nomes de domínio em endereços IP.
# Funcionamento

## (1) Navegador
- Você pesquisa o nome do domínio
## (2) DNS Query
- Seu computador verifica a memoria cache
- Caso não encontre o IP, ele solicita ao DNS resolver
## (3) Recursive Lookup
- O resolver verifica seu cache
- Caso não encontre, ele solicita ao servidor root
## (4) Root Server
- Servidor root aponta para o Top-Level Domain (TLD) responsável pelo fim do domínio (.com, .org, .br)

## (5) Servidor de nomes de domínio superior (TLD)
- Encaminha a solicitação para o servidor DNS responsável pelo domínio

## (6) Authoritative Name Server
- Encaminha o IP do domínio para o resolver

## (7) DNS Resolver 
- Encaminha o IP ao pc
- Salva o IP em seu cache

## (8) Seu PC
- Se conecta ao Servidor

# Arquivo H![[Pasted image 20260503140948.png]]osts

- Arquivo de configuração DNS manual
- Verificado antes do resolver
- Pode-se bloquear um domínio especifico apontando ele para um IP inválido
- Forçar o navegador a usar o arquivo hosts

![[Pasted image 20251228231606.png]]
# Zona DNS

Um espaço administrativo que é usado para gerenciar nomes de domínio, e pode ser tanto um painel com GUI quanto um arquivo zone file.

Exemplo de zone file:
![[Pasted image 20251228233944.png]]
# Tipos de Registro DNS

| Tipo de Registro | Nome Completo      | Descrição                            | Exemplo                                                 |
| ---------------- | ------------------ | ------------------------------------ | ------------------------------------------------------- |
| A                | IPv4               | Domínio para IPv4                    | www.jorge.com para 192.53.98.6                          |
| AAAA             | IPv6               | Domínio para IPv6                    | www.jorge.com para 2001:db8:85a3::8a2e:370:7334         |
| CNAME            | Canonical Name     | Um domínio aponta para outro domínio | blog.jorge.com aponta para www.jorge.com                |
| MX               | Mail Exchange      | Servidor de email do domínio         | www.jorge.com para mail.example.com                     |
| NS               | Name Server        | Servidor autoritativo                | www.jorge.com para ns1.example.com                      |
| TXT              | Text               | Informações em texto plano           | www.jorge.com para `"v=spf1 mx -all"`                   |
| SOA              | Start of Authority | Informações sobre a Zona DNS         | www.jorge.com  para ns1.example.com. admin.example.com. |
| SRV              | Service Record     | Serviços especificos                 | 1.2.0.192.in-addr.arpa para PTR www.jorge.com<br>       |
| PTR              | Reverse DNS        | DNS reverso                          | 1.2.0.192.in-addr.arpa. para www.jorge.com              |
