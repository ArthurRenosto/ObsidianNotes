
| Help         |                                      |
| ------------ | ------------------------------------ |
| man          | Manual da ferramenta                 |
| --help ou -h | Ajuda rápida no propio terminal      |
| apropos      | Busca por palavras chave no terminal |


| Users    | Descrição                                                                                                               |
| -------- | ----------------------------------------------------------------------------------------------------------------------- |
| whoami   | usuário atual                                                                                                           |
| [[id]]   | lista as permissões que o usuário possui, juntamente com seu GID/UID(numeros), os GID podem variar dependendo da distro |
| hostname | nome do host ou nome da maquina                                                                                         |
| uname    | informações sobre OS, Kernel e hardware                                                                                 |
| ip       | mostrar e manipular, roteamento, dispositivos de rede, interfaces                                                       |
| netstat  | status da tede                                                                                                          |
| ss       | sockets                                                                                                                 |
| ps       | status do processo                                                                                                      |
| who      | quem esta conectado                                                                                                     |
| env      | informações do ambiente                                                                                                 |
| lsblk    |                                                                                                                         |
| lsubsb   |                                                                                                                         |
| lsof     |                                                                                                                         |
| lspci    |                                                                                                                         |


```
uname -a

Linux balio 6.12.48+deb13-amd64 #1 SMP PREEMPT_DYNAMIC Debian 6.12.48-1 (2025-09-20) x86_64 GNU/Linux
```

Nome do Kernel: Linux
Nome do Host: balio
Kernel Version: 6.12.43+deb13-amd64
Kernel Release: Debian 6.12.48-1 
Nome do Hardware/Arquitetura: x86_64
Tipo do OS: GNU/Linux

cd -           -> ultimo diretorio que vc estava

inode -> funciona como um CPF do arquivo, ele  armazena : permissoes de acesso, tipo do arquivo, UDI, GDI, tamanho do arquivo, Timestamps, 

which nmap -> mostra o caminho do executavel

find /home/balio -name Desktop -> procura por desktop no diretorio especificado

find /home/balio -type f -name *.conf -user root -size +20k -newermt 2020-03-03 -exec ls -al {} \; 2>/dev/null

|   |   |
|---|---|
|`-type f`|Por este meio, definimos o tipo do objeto pesquisado. Neste caso, '`f`' significa '`file`".|
|`-name *.conf`|Com '`-name`"Indicamos o nome do arquivo que estamos procurando. O asterisco (`*`) significa "todos" arquivos com o '`.conf`' extensão.|
|`-user root`|Esta opção filtra todos os arquivos cujo proprietário é o usuário root.|
|`-size +20k`|Podemos então filtrar todos os arquivos localizados e especificar que queremos apenas ver os arquivos que são maiores que 20 KiB.|
|`-newermt 2020-03-03`|Com esta opção, marcamos a data. Somente arquivos mais recentes do que a data especificada serão apresentados.|
|`-exec ls -al {} \;`|Esta opção executa o comando especificado, usando os colchetes encaracolados como espaços reservados para cada resultado. A barra invertida escapa do próximo caractere de ser interpretado pelo shell porque, caso contrário, o ponto e vírgula encerraria o comando e não alcançaria o redirecionamento.|
|`2>/dev/null`|Isto é uma `STDERR`redirecionamento para o '`null device`", a que vamos voltar na próxima seção. Esse redirecionamento garante que nenhum erro seja exibido no terminal. Este redirecionamento deve `not`ser uma opção do comando 'encontrar'.|
