waf -> firewall de aplicacoes web, roda na camada 7

Ele monitora, filtra e bloqueia tráfego HTTP(S). Se uma requisição chega contendo um payload malicioso conhecido (ex: assinaturas de ataques comuns), o WAF detecta e bloqueia a requisição antes que ela chegue à aplicação web interna

Tecnicas de bypass:

- Criar payloads com sintaxe alternativa para o regex nao detectar
- Obsfuscation Usar _URL encoding_, _double encoding_, ofuscação com _wildcards_ (curingas) ou codificação mista.
- Misturar maiúsculas e minúsculas (ex: mudar `alert` para `aLeRt` ou `ALERT`).
- **Modificação de Headers:**

- Alterar o `Content-Type`.
    
- Adicionar conjuntos de caracteres diferentes.
    
- Alterar headers como o `Referer` ou o `Host` (ex: injetar `127.0.0.1` ou `localhost` para parecer tráfego interno confiável).

# pratica
fail
![[Pasted image 20251122113729.png]]

right
![[Pasted image 20251122113748.png]]

![[Pasted image 20251122113900.png]]

![[Pasted image 20251122113906.png]]


