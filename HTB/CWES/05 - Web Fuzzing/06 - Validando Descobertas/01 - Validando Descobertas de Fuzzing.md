- Validar uma vulnerabilidade de forma responsável, sem prejudicar o sistema ou expor dados confidenciais
- Ao fazermos o fuzzing de diretórios, encontramos um diretório cheio de arquivos, vamos validar se eles possuem arquivos sensíveis
# Curl
```bash
curl -I http://94.237.53.134:48939/ur-hiddenmember/backup.tar.gz
```

![[Pasted image 20260103225520.png]]
- **Content-Length: 210** -> maior que 0, significa que o arquivo pode conter informações sensíveis

- **Content-Type: application/x-gtar-compressed** -> corresponde com o tipo do arquivo