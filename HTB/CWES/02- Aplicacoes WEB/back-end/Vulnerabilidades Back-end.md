Se nao encontrarmos exploits publicos para uma aplicacao web, podemos procurar as vulnerabilidades manualmente.

https://owasp.org/www-project-top-ten/

# Broken Authentication/Access Control

Broken Authentication - permitir que um atacante ignore fatores de autenticacao, permitindo logins indesejados ou privilegios de administradores

Broken Access Control - Acessos a paginas e recursos que nao deveria, como paineis de administracao

# Malicious File Upload

Se uma aplicacao tiver uma funcao para uparmos arquivos, podemos upar um script (em php por exemplo) que sera executado e poderia abrir uma shell

# Command injection

As aplicacoes web executam comandos do sistema operacional, entao podemos instalar plugins usando comandos para termos acesso ao servidor back-end

# SQLI

Quando aplicacoes web executam uma consulta SQL usando parametros que o usuario passa sem validacao


