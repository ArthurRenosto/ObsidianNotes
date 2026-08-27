- Ferramenta para monitoramento de redes, servidores e serviços.
- Possui interface web.
- Possui opção de configuração de alertas.

# Módulos

## Zabbix Server

- Coleta dados para monitoramento.
- Quando alguma anormalidade é detectada, alertas são emitidos.
- Mantém um histórico dos dados coletados em banco de dados.

## Zabbix Proxy

- Coleta dados e armazena localmente para encaminhar para o server posteriormente.
- Usado em DMZs, assim ajudando no isolamento da rede.

## Zabbix Agent

- Instalado nos hosts.
- Coleta de dados locais como CPU, memória, disco, processos, logs e etc.