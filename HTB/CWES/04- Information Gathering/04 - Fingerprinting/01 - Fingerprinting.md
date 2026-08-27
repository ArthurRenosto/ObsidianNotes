Coleta de dados técnicos como:
- Identificação de tecnologias (CVEs, Exploits)
- Falhas de configuração (Misconfiguration)

# Técnicas

| Técnica                | Descrição                               |
| ---------------------- | --------------------------------------- |
| Banner Grabbing        | Banners apresentados por serviços       |
| Analysing HTTP Headers | Analise de headers HTTP                 |
| Specific Response      | Analise de resposta e mensagens de erro |

# Banner Grabbing

```bash
curl -I jorge.com -> server: Apache/2.4.41
```
**-I** -> visualizar os headers

Utilizar o banner grabbing no domínio localizado no header location da request HTTP para termos mais banners
# wafw00f

```bash
warw00f http://jorge.com
```

![[Pasted image 20251216215442.png]]

# nikto

![[Pasted image 20251216215543.png]]