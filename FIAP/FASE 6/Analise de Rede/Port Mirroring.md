
Ambiente de estudos no Packet Tracer.

![[Exemplo port mirroring.png]]

# Configurando o Switch

```
Switch>enable

Switch#configure terminal

Enter  configuration  commands,  one  per  line.  End  with CNTL/Z.

Switch(config)#monitor session 1 source interface fa0/1

Switch(config)#monitor session 1 source interface fa0/2

Switch(config)#monitor  session  1  destination  interface fa0/24

Switch(config)#exit
```

[[Configuração do Switch]]

# Pacotes ICMP

O Host 1 envio uma sequencia de pacotes ICMP ao host 2, e todos foram copiados para o sniffer, em função do SPAN.

Detalhes do pacote ICMP:

![[Pacote ICMP.png]]