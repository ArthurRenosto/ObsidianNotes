# browser
- HTTP/3 usa protocolo QUIC
- QUIC -> protocolo de transporte que combina funções TCP e TLS rodando sobre UDP na porta 443


# ping


ping -c 5 IP_ALVO -> -c define o numero de pacotes

ping -6 IP_ALVO -> define uma versao especifica do ip
- muitos roteadores diminuiem o TTL ou seja, se chegar 58 pode ser considerado um linux

# traceroute
- marca quantos hops sao dados ate chegar no destino
- cada roteador diminui o TTL quando chega a 0 devolve ICMP time to live exceeded, porem alguns roteadores podem nao enviar essa mensagem, sendo devolvido como *
- usa udp por padrao, mas pode ser usado traceroute -T IP_ALVO ou -I para ICMP

# telnet

pode ser usado para se conectar a qualquer porta TCP para banner grabbing
como por exeplo na porta 80

necessario mandar GET /aquivodesejado
```shell-session
pentester@TryHackMe$ telnet 10.65.129.123 80
Trying 10.65.129.123...
Connected to 10.65.129.123.
Escape character is '^]'.
GET / HTTP/1.1
host: telnet

HTTP/1.1 200 OKServer: nginx/1.6.2Date: Tue, 17 Aug 2021 11:13:25 GMTContent-Type: text/htmlContent-Length: 867Last-Modified: Tue, 17 Aug 2021 11:12:16 GMTConnection: keep-aliveETag: "611b9990-363"Accept-Ranges: bytes...
```

# netcat

- Usado para escutar ou se conectar a uma porta. 
- Suporta TCP e UDP.

nc IP_ALVO PORTA

![[Pasted image 20260922133620.png]]

mtr -> monitoramento do caminho em tempo real
