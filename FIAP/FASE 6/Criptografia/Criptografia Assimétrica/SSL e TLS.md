O SSL (Secure Socket Layer) estabele um canal criptografado entre o servidor web e o navegador do cliente, com objetivo de garantir a **privacidade, integridade e autenticidade** dos dados trafegados.

O TLS (Transport Layer Security) assim como o SSL também estabelece um canal criptografado de comunicação, em sumo, ambos os protocolos são substancialmente o mesmo,  porém nos dias atuais o TLS vem substituindo o SSL

# 3Handshake

Quando o SSL/TLS vai estabelecer uma comunicação cliente-servidor, ele segue um processo chamado Triple Handshake (ou 3Handshake), para a garantia de uma comunicação segura.

```ad-passo_1

- O cliente solicita ao servidor uma conexão segura, eviando a versão do protocolo suportada (TLS 1.2, TLS 1.3) e uma lista de algoritmos criptograficos suportados (RSA, DAS, ECDSA)
```

```ad-passo_2
title: Passo 2

- O servidor recebe a requisição e escolhe o algoritmo mais forte em comum respondendo para o cliente qual algoritmo será usado
- O servidor realiza a autenticação enviado seu certificado digital, emitido pela AC (Autoridade Certificadora) juntamente com sua chave pública
- Ambos trocam as chaves públicas (RSA e Diffie-Hellman)
```

```ad-passo_3
title: Passo 3


- O cliente e o servidor utilizam sua chave de sessão para criptografar as mensagens de forma simétrica
- A autenticação das mensagens ocorre por funções hash HMAC-MD5 ou HMAC-SH

```
