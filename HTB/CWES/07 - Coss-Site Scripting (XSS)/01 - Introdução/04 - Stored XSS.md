- Stored XSS / Persistent XSS
# Descrição

Ocorre quando o payload JS é armazenado no banco de dados e executado ao visitar a pagina novamente. Isso significa que caso ela seja armazenada em um campo carregado por todos os usuários, os mesmos executarão o script.

# Identificando

```javascript
<script>alert(1)</script>
```
