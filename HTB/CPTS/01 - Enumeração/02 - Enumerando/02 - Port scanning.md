 - Ao realizarmos um port scanning procuramos encontrar:
	 - Portas abertas
	 - Serviços
	 - Versões de serviços
	 - OS
 
# Estados das portas

| Estado             | Descrição                                                                                                                         |
| ------------------ | --------------------------------------------------------------------------------------------------------------------------------- |
| open               | A conexão com a porta foi estabelecida. Essas conexões podem ser TCP, datagramas UDP, associações SCTP                            |
| closed             | A porta é exibida como fechada, o protocolo TCP indica que recebemos uma flag RST.                                                |
| filtered           | O nmap não consegue determinar o estado da porta, pois não recebeu resposta ou recebeu um erro                                    |
| unfiltered         | O nmap encaminha um ACK e recebe um RST, ele não determina se a porta está aberta ou fechada, mas sabe que a porta está acessível |
| open \| filtered   | Caso não receba resposta de uma porta especifica, indica que um firewall pode estar protegendo está porta                         |
| closed \| filtered | Não consegue determinar se a porta está fechada ou filtrada, geralmente aparece em scans IP IDLE                                  |
# Descobrindo portas TCP

- Por padrão o quando executamos o nmap como root, ele scaneia as 1000 principais portas TCP, com SYN scan (-sS).
- Quando executamos o nmap sem root, é feito um scan TCP (-sT)

| Flag               | Descrição                                                                          |
| ------------------ | ---------------------------------------------------------------------------------- |
| -p 22,25,80,139    | Definindo portas manualmente                                                       |
| -p 22-445          | Defiinindo range de portas                                                         |
| --top-ports=10     | Definido por portas mais utilizadas                                                |
| -p-                | Todas as portas                                                                    |
| -F                 | 100 portas mais comuns                                                             |
| -sS                | Força o uso do SYN scan, sendo mais furtivo                                        |
| -sT                | Força o 3-way-handshake, completando a conexão, sendo menos furtivo e mais preciso |
| -Pn                | Desativa o ICMP Request                                                            |
| --packet-trace     | Mostra todos os pacotes enviados e recebidos                                       |
| --disable-arp-ping | Desativa o arp ping                                                                |
| -n                 | Desativa resolução DNS                                                             |
| -sU                | Scan UDP                                                                           |
| -sV                | Scan de versão                                                                     |
| -oN                | Salva os resultados do nmap em .nmap                                               |
| -oG                | Salva os resultados do nmap em .gnmap                                              |
| -oX                | Salva os resultados do nmap em .xml                                                |
| -oA                | Salva os resultados do nmap em todos os formatos permitidos                        |
# Compreendendo Resultado

![[Pasted image 20260417220520.png]]
### Envio do Pacote SYN (S)

```
SENT (0.0429s) TCP 10.10.14.2:63090 > 10.129.2.28:21 S ttl=56 id=57322 iplen=44  seq=1699105818 win=1024 <mss 1460>
```

### Recebimento do Pacote RST e ACK (RA)

```
RCVD (0.0573s) TCP 10.129.2.28:21 > 10.10.14.2:63090 RA ttl=64 id=0 iplen=40  seq=0 win=0
```

# Portas Filtradas

 - Firewalls possuem regras para droparem ou rejeitarem pacotes, assim fazendo com que não recebamos nem uma resposta.
 - Por padrao o nmap possui o --max-retries em 10, onde ele reenvia a solicitação 10 vezes, para garantir que não foi algo acidental ou mal tratado.

| Regra  | Resposta                                                                                                                                                                                         |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| DROP   | O firewall dropa o pacote, assim fazendo o nmap não receber resposta e fazendo ele encaminhar outra solicitação, assim o scan fica mais lento                                                    |
| REJECT | O firewall encaminha um pacote que rejeita a conexão, assim fazendo com que a resposta do nmap seja mais rápida, e fazendo com que ele não reencaminhe pacotes, pois ele ja obteve uma resposta. |
# Descobrindo Portas UDP

- Scan mais lento, pois como o UDP não requer o 3-Way-Handshake o tempo limite do nmap é muito maior, fazendo o scan ser muito mais lento

![[Pasted image 20260502154510.png]]

- Como o nmap envia datagrams vazios e não temos confirmação dos dados enviados por ser uma conexão UDP, muitas vezes, não é possível saber.
- Podemos saber se a porta está aberta, caso o sistema esteja configurado para responder a solicitação

![[Pasted image 20260503092059.png]]

 - Se obtivermos uma resposta ICMP erro code 3, sabemos que a porta está fechada pois é inalcançavel.

![[Pasted image 20260503092211.png]]

- Todas as outras respostas do ICMP marcam a porta como open|filtered, pois são alcançáveis mas o UDP não responde

![[Pasted image 20260503092417.png]]

# Salvando Resultados

- É possível utilizar a ferramenta xsltproc para transformar tabelas xml em relatórios HTML

```shell
xsltproc target.xml -o target.html
```

![[Pasted image 20260503093347.png]]



