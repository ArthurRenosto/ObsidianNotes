# Descrição

Ocorre quando o payload JS é enviado ao servidor back-end e retornado para nós sem nem um tipo de validação.

Uma vez atualizada a página o Reflected XSS não será executado pois ele não fica armazenado em local algum.
# Identificando

Precisamos verificar o método HTTP utilizado para envio das informações, pois caso seja utilizado o método GET, as informações são passadas na URL, permitindo o envio da URL para as vitimas já com o payload embutido.

![[Pasted image 20260118010706.png]]
![[Pasted image 20260118010740.png]]

```javascript
<script>alert(1)</script>
```
