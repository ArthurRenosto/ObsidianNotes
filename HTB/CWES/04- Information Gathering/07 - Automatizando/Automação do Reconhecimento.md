- Reconhecimento manual é lento e propenso a erros
- Permite reconhecimento continuo

| Ferramenta      |
| --------------- |
| FinalRecon      |
| Recon-ng        |
| TheHarvester    |
| SpiderFoot      |
| OSINT Framework |

# FinalRecon

https://github.com/thewhiteh4t/FinalRecon.git

| Flag      | Descrição                       |
| --------- | ------------------------------- |
| --url     | especificar url                 |
| --headers | Informações de headers          |
| --sslinfo | Informações de certificados SSL |
| --whois   | Pesquisa whois                  |
| --craw    | Crawler no site                 |
| --dns     | Enumeração DNS                  |
| --sub     | Subdomínios                     |
| --dir     | Diretorios                      |
| --wayback | URLs do Wayback machine         |
| --ps      | Varredura de portas             |
| --full    | Reconhecimento completo         |

```bash
./finalrecon.py --full --url https://ixcsoft.com
```
