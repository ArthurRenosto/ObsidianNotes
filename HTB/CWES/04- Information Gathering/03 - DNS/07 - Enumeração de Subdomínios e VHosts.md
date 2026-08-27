# sublist3r

```bash
sublist3r -d jorge.com
```
# findomain

- **Configuração de API keys**
	- export findomain_securitytrails_token="API KEY"
	- export findomain_virustotal_token="API KEY"
```bash
findomain -t jorge.com
```

# crt.sh
https://crt.sh

```bash
curl -s "https://crt.sh/?q=jorge.com&output=json" | jq -r '.[]
 | select(.name_value | contains("dev")) | .name_value' | sort -u
```

**curl -s "https://crt.sh/?q=jorge.com&output=json"** -> obtendo resultado json do crt.sh

**jq -r '.[] | select(.name_value | contains("dev")) | .name_value'** -> a copiar

**sort -u** -> ordena em ordem alfabética e remove duplicatas
# censys
https://search.censys.io/

## gobuster
```bash
gobuster vhost -u jorge.com -w subdomains-top1million-110000.txt --append-domain
```

**gobuster vhost** -> enumerando vhosts

**--append-domain** -> usando para anexar o domínio as palavras da wordlist