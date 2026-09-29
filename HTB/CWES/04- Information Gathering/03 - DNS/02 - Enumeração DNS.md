
# DIG

| Comando                      | Descrição                                                                    |
| ---------------------------- | ---------------------------------------------------------------------------- |
| dig jorge.com                | Pesquisa padrão                                                              |
| dig jorge.com A              | Endereço IPv4                                                                |
| dig jorge.com AAAA           | Endereço IPv6                                                                |
| dig @1.1.1.1 jorge.com       | Especifica o servidor DNS para consulta                                      |
| dig +trace jorge.com         | Exibe o caminho da resolução DNS                                             |
| dig -x 192.168.1.1           | Reverse DNS                                                                  |
| dig +short jorge.com         | Resposta curta                                                               |
| dig +noall +answer jorge.com | Apenas parte da resposta                                                     |
| dig jorge.com ANY            | Todos os registros DNS disponíveis para o domínio (Servidores podem ignorar) |
## Saída

Esta saída é o resultado de uma consulta DNS usando o `dig`comando para o domínio `google.com`. O comando foi executado em um sistema em execução `DiG`versão `9.18.24-0ubuntu0.22.04.1-Ubuntu`. A saída pode ser dividida em quatro seções principais:

1. Cabeçalho
    
    - `;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 16449`: Esta linha indica o tipo de consulta (`QUERY`), o status de sucesso (`NOERROR`), e um identificador único (`16449`) para esta consulta específica.
        
        - `;; flags: qr rd ad; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 0`: Isso descreve as bandeiras no cabeçalho DNS:
            - `qr`: Bandeira de resposta de consulta - indica que esta é uma resposta.
            - `rd`: Recursão Bandeira desejada - significa que foi solicitada recursão.
            - `ad`: Bandeira de dados autêntica - significa que o resolvedor considera os dados autênticos.
            - Os números restantes indicam o número de entradas em cada seção da resposta DNS: 1 pergunta, 1 resposta, 0 registros de autoridade e 0 registros adicionais.
    - `;; WARNING: recursion requested but not available`: Isso indica que a recursão foi solicitada, mas o servidor não suporta.
        
2. Secção de perguntas
    
    - `;google.com. IN A`: Esta linha especifica a pergunta: "Para que é o endereço IPv4 (Um registro) `google.com`?"
3. Seção de Resposta
    
    - `google.com. 0 IN A 142.251.47.142`: Esta é a resposta para a consulta. Indica que o endereço IP associado a `google.com`é `142.251.47.142`. O "`0`" representa o `TTL`(tempo de vida), indicando quanto tempo o resultado pode ser armazenado em cache antes de ser atualizado.
4. Rodapé
    
    - `;; Query time: 0 msec`: Isso mostra o tempo necessário para que a consulta fosse processada e a resposta fosse recebida (0 milissegundos).
        
    - `;; SERVER: 172.23.176.1#53(172.23.176.1) (UDP)`: Isso identifica o servidor DNS que forneceu a resposta e o protocolo utilizado (UDP).
        
    - `;; WHEN: Thu Jun 13 10:45:58 SAST 2024`: Este é o carimbo de data/hora de quando a consulta foi feita.
        
    - `;; MSG SIZE rcvd: 54`: Isso indica o tamanho da mensagem DNS recebida (54 bytes).
        

Um `opt pseudosection`Às vezes pode existir em um `dig`consulta. Isto é devido a Mecanismos de Extensão para DNS (`EDNS`), que permite recursos adicionais, como tamanhos de mensagens maiores e extensões de segurança DNS (`DNSSEC`) apoio.

# dnsenum

- Recupera vários tipos de registros
- Transferencia de Zona
- Brute Force
- Google Scraping
- Reverse Lookup
- WHOIS Lookup

```bash
dnsenum --enum jorge.com -f subdomains-top1million-20000.txt -r
```

**--enum** -> permite opções de ajuste

**-f** -> caminho para wordlist, caso não especificado, utiliza uma default

**-r** -> subdomínio recursivo (se ele achar um subdomínio, ele tenta enumera-lo)

# dnsrecon

```bash
dnsrecon -d jorge.com
```

# dnsdumpster

- Possui informações como:
	- Cache de mecanismos de pesquisa.
	- Bbancos de dados de transferencias de zona. 
	- Registros de certificado.
	- Gráficos de informações relacionadas entre si.

https://dnsdumpster.com/
