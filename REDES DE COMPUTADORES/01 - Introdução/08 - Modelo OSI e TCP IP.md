# Modelo OSI

- Open System Interconnection.
- Modelo de demonstração para estudos sobre como a comunicação de rede ocorre.

![[Pasted image 20260124200819.png]]

| Número | Camada       | Função                                             | Protocolos                                      |
| ------ | ------------ | -------------------------------------------------- | ----------------------------------------------- |
| 7      | Aplicação    | Prover serviços de rede as aplicações              | HTTP, FTP, SSH, Telnet, RDP, DNS, SNMP, POP3... |
| 6      | Apresentação | Criptografia, compressão e formatação de dados     | TLS/SSL...                                      |
| 5      | Sessão       | Manter e finalizar sessões                         | NetBIOS...                                      |
| 4      | Transporte   | Transmissão e segmentação de dados                 | TCP, UDP...                                     |
| 3      | Rede         | Endereçamento e Roteamento                         | IP, ICMP, RIP, OSPF, BGP...                     |
| 2      | Enlace       | Detecção de eventuais erros e endereçamento físico | Ethernet, IEEE 802, Frame, Relay, MAC, ATM...   |
| 1      | Física       | Comunicação física com os meios de transmissão     | Par trançado, Fibra óptica                      |
# EXPLICAR

| Camada | Nome da camada  | Unidade de dados (PDU)                   | Exemplo / Observação      |
| -----: | --------------- | ---------------------------------------- | ------------------------- |
|      7 | Aplicação       | **Dados**                                | HTTP, FTP, SMTP           |
|      6 | Apresentação    | **Dados**                                | Criptografia, compressão  |
|      5 | Sessão          | **Dados**                                | Controle de sessão        |
|      4 | Transporte      | **Segmento** (TCP) / **Datagrama** (UDP) | Portas, controle de fluxo |
|      3 | Rede            | **Pacote**                               | IP, roteamento            |
|      2 | Enlace de Dados | **Frame (Quadro)**                       | MAC, Ethernet             |
|      1 | Física          | **Bits**                                 | Sinais elétricos/ópticos  |
# OSI Hacking

![[Pasted image 20260124210940.png]]

# Modelo TCP/IP

- Transmission Control Protocol / Internet Protocol.
- Modelo prático utilizado comercialmente.
- Agrupa as funções e protocolos do modelo OSI em 4 camadas.

![[Pasted image 20260124210001.png]]

| Número | Camada        | Função                                                                | Protocolos                                            |
| ------ | ------------- | --------------------------------------------------------------------- | ----------------------------------------------------- |
| 4      | Aplicação     | Prover serviços de rede, sessão e apresentação                        | HTTP, HTTPS, FTP, SSH, SMTP, POP3, IMAP, DNS, SNMP... |
| 3      | Transporte    | Transmissão e segmentação de dados                                    | TCP, UDP...                                           |
| 2      | Internet      | Endereçamento e Roteamento                                            | IP, ICMP                                              |
| 1      | Acesso a Rede | Comunicação física com os meios de transmissão e endereçamento físico | Ethernet, ARP, Wi-Fi                                  |
