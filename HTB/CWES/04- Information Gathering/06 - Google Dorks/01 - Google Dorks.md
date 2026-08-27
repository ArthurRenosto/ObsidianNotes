- Também conhecido como Google Hacking
- Utilização de operadores do Google para 
# Utilizando

Mais exemplos de querys prontas em: https://www.exploit-db.com/google-hacking-database 
# Páginas de login

- site:example.com inurl:login
- site:example.com (inurl:login OR inurl:admin) 
## Arquivos expostos
- site:example.com filetype:pdf
- site:example.com (filetype:xls OR filetype:docx)

## Arquivos de configuração
- site:example.com inurl:config.php
- site:example.com (ext:conf OR ext:cnf)(pesquisa por extensões comumente usadas para arquivos de configuração)

## Backups de dbs
- site:example.com inurl:backup
- site:example.com filetype:sql
# Exemplos

| Operador                    | Descrição do operador                                                        | Exemplo                                             | Exemplo Descrição                                                                                    |
| :-------------------------- | :--------------------------------------------------------------------------- | :-------------------------------------------------- | :--------------------------------------------------------------------------------------------------- |
| `site:`                     | Limita os resultados a um site ou domínio específico.                        | `site:example.com`                                  | Encontre todas as páginas acessíveis ao público em example.com.                                      |
| `inurl:`                    | Encontra páginas com um termo específico no URL.                             | `inurl:login`                                       | Procure por páginas de login em qualquer site.                                                       |
| `filetype:`                 | Procura por ficheiros de um tipo específico.                                 | `filetype:pdf`                                      | Encontre documentos PDF para download.                                                               |
| `intitle:`                  | Encontra páginas com um termo específico no título.                          | `intitle:"confidential report"`                     | Procure documentos intitulados "relatório confidencial" ou variações semelhantes.                    |
| `intext:`ou `inbody:`       | Procura por um termo dentro do texto corporal das páginas.                   | `intext:"password reset"`                           | Identificar páginas da Web contendo o termo “redefinição de senha”.                                  |
| `cache:`                    | Exibe a versão em cache de uma página da Web (se disponível).                | `cache:example.com`                                 | Visualize a versão em cache do example.com para ver seu conteúdo anterior.                           |
| `link:`                     | Encontra páginas que têm links para uma página web específica.               | `link:example.com`                                  | Identificar sites que vinculam a example.com.                                                        |
| `related:`                  | Encontra sites relacionados a uma página web específica.                     | `related:example.com`                               | Descubra sites semelhantes ao example.com.                                                           |
| `info:`                     | Fornece um resumo das informações sobre uma página da Web.                   | `info:example.com`                                  | Obtenha detalhes básicos sobre example.com, como seu título e descrição.                             |
| `define:`                   | Fornece definições de uma palavra ou frase.                                  | `define:phishing`                                   | Obtenha uma definição de "phishing" de várias fontes.                                                |
| `numrange:`                 | Pesquisa por números dentro de um intervalo específico.                      | `site:example.com numrange:1000-2000`               | Encontre páginas em example.com contendo números entre 1000 e 2000.                                  |
| `allintext:`                | Encontra páginas contendo todas as palavras especificadas no texto do corpo. | `allintext:admin password reset`                    | Procure por páginas contendo "admin" e "redefinição de senha" no texto do corpo.                     |
| `allinurl:`                 | Encontra páginas contendo todas as palavras especificadas na URL.            | `allinurl:admin panel`                              | Procure páginas com "admin" e "painel" na URL.                                                       |
| `allintitle:`               | Encontra páginas contendo todas as palavras especificadas no título.         | `allintitle:confidential report 2023`               | Procure por páginas com "confidencial", "relatório" e "2023" no título.                              |
| `AND`                       | Reduz os resultados exigindo que todos os termos estejam presentes.          | `site:example.com AND (inurl:admin OR inurl:login)` | Encontre páginas de administração ou login especificamente em example.com.                           |
| `OR`                        | Amplia os resultados incluindo páginas com qualquer um dos termos.           | `"linux" OR "ubuntu" OR "debian"`                   | Procure por páginas da Web mencionando Linux, Ubuntu ou Debian.                                      |
| `NOT`                       | Exclui resultados contendo o termo especificado.                             | `site:bank.com NOT inurl:login`                     | Encontre páginas no bank.com excluindo páginas de login.                                             |
| `*`(Wildcard)Tradução       | Representa qualquer caráter ou palavra.                                      | `site:socialnetwork.com filetype:pdf user* manual`  | Procure manuais do usuário (guia do usuário, manual do usuário) em formato PDF no socialnetwork.com. |
| `..`(pesquisa de intervalo) | Encontra resultados dentro de um intervalo numérico especificado.            | `site:ecommerce.com "price" 100..500`               | Procure produtos com preços entre 100 e 500 em um site de comércio eletrônico.                       |
| `" "`(marcas de cotação)    | Buscas por frases exatas.                                                    | `"information security policy"`                     | Encontre documentos mencionando a frase exata "política de segurança da informação".                 |
| `-`(menos sinal)            | Exclui termos dos resultados da pesquisa.                                    | `site:news.com -inurl:sports`                       | Procure artigos de notícias em news.com excluindo conteúdo relacionado a esportes.                   |

### Google Dorking



Veja alguns exemplos comuns do Google Dorks, para mais exemplos, consulte [o Banco de](https://www.exploit-db.com/google-hacking-database) Dados [de Hacking do](https://www.exploit-db.com/google-hacking-database) Google :

- Encontrando Páginas de Login:
    - `site:example.com inurl:login`
    - `site:example.com (inurl:login OR inurl:admin)`
- Identificando Arquivos expostos:
    - `site:example.com filetype:pdf`
    - `site:example.com (filetype:xls OR filetype:docx)`
- Descobrindo arquivos de configuração:
    - `site:example.com inurl:config.php`
    - `site:example.com (ext:conf OR ext:cnf)`(pesquisa por extensões comumente usadas para arquivos de configuração)
- Localizando backups de banco de dados:
    - `site:example.com inurl:backup`
    - `site:example.com filetype:sql`