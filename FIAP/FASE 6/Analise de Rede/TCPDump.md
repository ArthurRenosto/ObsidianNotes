```
sudo apt install tcpdump
```

Exibe as interface de rede disponíveis
```
tcpdump -D
```

Filtrando nossa conexão apenas por pacotes ICMP
```
sudo tcpdump icmp
```

Filtrando por placa de rede
```
sudo tcpdump -i eth0 icmp
```

Salvando as informações em um aquivo para ser aberto to wireshark
```
sudo tcpdump icmp -w arquivo.cap
```

Visualizando as informações salvas
```
sudo tcpdump -r arquivo.cap
```

```
tcpdump -r arquivo.pcap > arquivo.txt
```

Não mostra nomes de domínio, apenas IPs
```
sudo tcpdump icmp -n
```

# Trafego HTTP

A comunicação HTTP é caracterizada por sua conexão TCP feita na porta 80, logo é isso que vamos capturar para podermos visualizar informações de requisição etc.
```
tcpdump -i eth0 -w captura.pcap tcp port 80
```

Exibindo a primeira linha do arquivo salvo
```
tcpdump -r captura.pcap | head -n1
```

Exibindo apenas a comunicação com a flag PUSH
```
tcpdump -r captura.pcap | grep -w P.
```

A flag -i do parâmetro grep retira o case sensitive, então independente do host estar maiúsculo ou minúsculo
```
tcpdump -r captura.pcap | grep -i host
```

capturando o trafego TCP na porta FTP e FTP data, 21 e 22, como o modo verboso ativo
```
tcpdump -i eth0 -vv -w tafego_ftp.pcap tcp port ftp or port ftp-data
```