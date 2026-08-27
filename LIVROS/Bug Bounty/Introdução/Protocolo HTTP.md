Os protocolos são essenciais para que aja uma comunicação padronizada, o protocolo HTTP define como seu navegador vai trocar pacotes com o servidor.

# Passo a Passo do HTTP

```
É inserido o nome de domínio(exemplo https://www.google.com/search?q=fotos-legais) na URL e o navegador faz a separação em:

- Protocolo: HTTPS
- Domínio: www.google.com
- Caminho: search?q=fotos-legais
  ```

```
O navegador e o sistema operacional verificam se possuem IP do domínio em seu cache(DNS cache local)

Caso nao possuirem, eles fazem uma consulta ao servidor DNS que está configurado no roteador
```

```
O navegador pergunta ao servidor DNS
O servidor DNS responde com o IP do domínio
O navegador armazena o IP em seu cache local para próximas consultas
```

```
O navegador inicia a conexão TCP com o IP do domínio
Se o domínio for HTTP ele se conecta a porta 80, se for HTTPS se conecta a porta 443

O TCP faz o 3Handshake:

1- Client SYN
2- Server SYN-ACK
3- client ACK
```

```
Caso a comunicação seja HTTPS, ocorre um handashake TLS:

1- Negociação da versão do TLS e negociação dos algoritmos criptograficos
2- Servidor envia o certificado
3- Cliente Válida o certificado e gera a chave de sessão
4- É estabelecido um canal criptografado
```

```
Navegador envia a requisição(request) HTTP ao servidor:
```
[[HTTP Request e Response]]

```
Servidor Recebe a requisição
Processa
Gera uma resposta(response) HTTP e a envia
```
[[HTTP Request e Response]]

```
O navegador interpreta o conteudo HTML da response
Baixa os recursos adicionais usando novas requisições HTTP
Executa o JS e aplica o CSS montando uma pagina visivel para o usuario
```

[[HTTP Sateless]]