# Passivo
## WHOIS

```bash
whois jorge.com
```
## DNS
https://dnsdumpster.com/
## Subdomínios

```bash
sublist3r -d jorge.com
```

```bash
findomain -t jorge.com
```

```bash
curl -s "https://crt.sh/?q=jorge.com&output=json" | jq -r '.[]
 | select(.name_value | contains("dev")) | .name_value' | sort -u
```

https://crt.sh | https://search.censys.io/
## Fingerprinting

```bash
curl -I jorge.com
```

```bash
wafw00f jorge.com
```

```bash
nikto -h jorge.com -Tuning b
```

## Crawlers

```
robots.txt
```

```
.well-known
```

https://web.archive.org/

## Google Dorks
```
site:example.com filetype:pdf
site:example.com (filetype:xls OR filetype:docx)
```

```
site:example.com inurl:config.php
site:example.com (ext:conf OR ext:cnf)(pesquisa por extensões comumente usadas para arquivos de configuração)
```

```
site:example.com inurl:backup
site:example.com filetype:sql
```

https://www.exploit-db.com/google-hacking-database

# Ativo

## DNS

```bash
dnsenum --enum jorge.com -f subdomains-top1million-20000.txt -r
```

## Subdomínios

```bash
gobuster dns -do inlanefreight.com -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt --no-error
```

```bash
ffuf -w common.txt -u http://FUZZ.exemplo.com.br/
```

## Crawlers

```bash
python3 ReconSpider.py http://inlanefreight.com
```
## VHosts

```bash
gobuster vhost -u jorge.com -w subdomains-top1million-110000.txt --append-domain
```

## Diretórios

```bash
ffuf -w common.txt -u http://jorge.com/FUZZ
```

## Arquivos

```bash
ffuf -w common_directories.txt:DIR -w raft-medium-extensions.txt:PARAM -u http://bancocn.com/DIRPARAM
```
## Recursivo

```bash
ffuf -w raft-large-directories.txt -ic -v -u http://jorge.com/FUZZ/ -e .html -recursion 
```

