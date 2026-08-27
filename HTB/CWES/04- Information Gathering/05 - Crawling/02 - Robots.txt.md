- Arquivo de texto colocado no diretório root do site
- Instruções aos crawlers

# Estrutura

- User-agent: Especifica a quais bots as diretivas se aplicam, pode-se usar um curinga para todos (\*), ou especificar (Googlebot, Bingbot)
- Directives: instruções para o user agent especificado


| Directive  | Descrição                                                                | Exemplo                                     |
| ---------- | ------------------------------------------------------------------------ | ------------------------------------------- |
| Disallow   | Diretórios que o bot não deve rastrear                                   | Disallow: /wp-admin/<br>                    |
| Allow      | Permite explicitamente acesso, mesmo que passe por um diretório disallow | Allow: /wp-admin/admin-ajax.php             |
| Craw-delay | Atraso para as requests do bot não sobrecarregarem o server              | Crawl-delay: 10                             |
| Sitemap    | Fornece um sitemap XML para um melhor rastreamento                       | Sitemap: https://www.roger.com/sitemap1.xml |
![[Pasted image 20260101225055.png]]
# Função

- Mapear a estrutura do site para encontrar paineis administrativos, arquivos de backup e etc.

Alguns sites incluem intencionalmente diretórios "honeypot" em robots.txt para atrair bots maliciosos.
