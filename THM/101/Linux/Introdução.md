# Editores de texto

nano
vim 

# Download de arquivos

- wget faz o download de arquivos via HTTP


bash
wget https://siteparadownload.com/arquivos/arquivo.txt


# Trasferindo arquivos do pc

- scp utiliza a criptografia e autenticação do protocolo SSH para copia de arquivos e diretórios

- copiando arquivo de nossa maquina para outra

bash
scp arquivo.txt usuario@192.168.0.5:/home/usuario/destino/arquivotrasferido.txt


- copiando arquivo de outra maquina para nossa

bash
scp usuario@192.168.0.5:/home/usuario/arquivo arquivorecebido.txt


# HTTPServer

- Abrindo um servidor HTTP com python

bash
python3 -m http.server


- outra opcao é o Updog

# Processos

- programas executados em um OS gerenciados pelo kernel
- possuem um ID associado chamado de PID

- visualizando processos apartir de uma sessão

bash
ps


- vizualizando processos executados pelo sistema ou por outros usuarios.

bash
ps aux


- Verificando estatisticas em tempo real

bash
top


## Gerenciando Processos

- matando processos

kill -> mata o processo com o numero do pid
pkill -> mata o processo pelo nome
SIGTERM -> mata o processo mas permite que ele faça tarefas de limpeza antes
SIGKILL -> mata o processo mas nao faz nem uma limpeza
SIGSTOP -> para/suspende o processo

## Começo dos processos

- o OS usa namespaces para dividir os recursos do computador para os processos
- Os namespaces segmentam os processos um dos outros, apenas os processos do mesmo namespace iram se ver
- o processo com pid 0 é o systemd iniciado quando o sistema inicializa, qualquer processo iniciado na sequencia é filho do systemd e controlado por ele

