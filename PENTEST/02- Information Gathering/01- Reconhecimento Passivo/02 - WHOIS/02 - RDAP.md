- O RDAP(Registration Data Access Protocol ou Protocolo de Acesso a Dados de Registrio) é um sucessor moderno ao protocolo WHOIS.
- Utiliza HTTPS.
- Retorna dados em JSON.
- Padrão utilizado atualmente.

# Utilizando
```bash
curl -s 'https://rdap.verisign.com/com/v1/domain/tryhackme.com' | jq .
```
