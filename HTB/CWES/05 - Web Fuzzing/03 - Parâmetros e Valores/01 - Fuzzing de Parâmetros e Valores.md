- Fuzzing de parâmetros em requests HTTP

# GET
- Aplicação retorna um erro ao inserirmos valores na query string
- Fuzzing para encontrar o valor que retorna 200 OK
![[Pasted image 20260103191534.png]]

```bash
ffuf -w common.txt -u http://94.237.121.111:39805/get.php?x=FUZZ -fc 404
```

**-fc** -> ocultando repostas 404

# POST
- No POST, não passamos valores na URL e sim no body da request
- Aplicação retorna um erro ao inserirmos valores no body
- Fuzzing para encontrar o valor que retorna 200 OK
![[Pasted image 20260103191744.png]]

```bash
ffuf -u http://94.237.121.111:39805/post.php -X POST -H "Content-Type: application/x-www-form-urlencoded" -d "y=F
UZZ" -w /common.txt -mc 200 -v
```
(Muito importante passar o Content-Type correto)

**-X POST** -> método POST
**-H** -> Definir um header
**-d** -> corpo da request
**-mc** -> apenas respostas 200k

![[Pasted image 20260103192133.png]]
 Pegamos o valor retornado e usamos como parâmetro em nossa request post