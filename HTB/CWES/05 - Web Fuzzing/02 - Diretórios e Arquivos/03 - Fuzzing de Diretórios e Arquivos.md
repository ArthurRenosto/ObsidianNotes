# Diretórios

```bash
ffuf -w common.txt -u http://jorge.com/FUZZ
```

# Arquivos
```bash
ffuf -w raft-large-directories.txt -u http://jorge.com/admin/FUZZ -e .php,.html,.bak,.txt,.js -v
```
**-e** -> itera as extensões de arquivo as wordlist
**-v** -> saida extensa com status code, tamanho, etc
**Quando listar as extensões, nunca dar espaço após a virgula**

# Recursivo
```bash
ffuf -w raft-large-directories.txt -ic -v -u http://jorge.com/FUZZ -e .html -recursion 
```

**-ic** -> ajuda no tratamento de erros removendo case-sensitive(admin == Admin) e ignorando linhas comentadas em wordlists
**-recursion** -> ativa a busca recursiva

```bash
ffuf -w raft-large-directories.txt -ic -u http://IP:PORT/FUZZ -e .html -recursion -recursion-depth 2 -rate 500
```

**--recursion-depth** -> profundidade máxima (diretório e subdiretórios)
**-rate** -> request por segundo
**-timeout** -> tempo limite para requests