- **Scan Passivo:**  Analisa o código client-side em busca de possíveis DOM XSS.
- **Scan Ativo:** Envia diversos payloads XSS e verifica o souce-code para ver se o payload está contido lá.

# Scanneres

| Nome     | Link                                       |
| -------- | ------------------------------------------ |
| XSStrike | https://github.com/s0md3v/XSStrike         |
| BruteXSS | https://github.com/rajeshmajumdar/BruteXSS |
| xsser    | https://github.com/epsylon/xsser           |
# XSStrike

```bash
python xsstrike.py -u http://jorge.com/
```

Ainda sim mesmo que os payloads tenham sido injetados, não significa que serão executados, então sempre é necessário a verificação manual.

# Payloads list

https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/XSS%20Injection/README.md