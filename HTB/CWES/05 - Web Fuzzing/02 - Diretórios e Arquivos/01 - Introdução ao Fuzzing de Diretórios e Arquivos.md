# Wordlists

- Uma das wordlists mais utilizada é a SecLists 
- https://github.com/danielmiessler/SecLists
- Caso instalada com apt, localizada em /usr/share/seclists

## Mais utilizadas para web

- Discovery/Web-Content/common.tdxt
- Discovery/Web-Content/DirBuster-2007_directory-list-2.3-medium.txt
- Discovery/Web-Content/raft-large-directories.txt
- Discovery/Web-Content/big.txt

# Fuzzing de Diretórios
- Descoberta de diretórios
- Analise de status codes 200 e 301

# Fuzzing de Arquivos
- Iteração de extensões de arquivos a wordlists
# FFUF

## (1) Wordlist
- Fornece a wordlist
## (2) FUZZ
- Seta o parametro FUZZ no local da URL que deseja testar
## (3) Requests
- Itera a wordlists a URL
- Faz as requests HTTP
## (4) Response
- Analisa as respostas com base em status code, tamanho, etc
- Filtra os resultados

# Utilizando FFUF
[[03 - Fuzzing de Diretórios e Arquivos]]