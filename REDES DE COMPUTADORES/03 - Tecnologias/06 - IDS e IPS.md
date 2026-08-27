- Intrusion Detection System
- Intrusion Prevention System

# IDS

- Coleta informações de diversos ataques para fazer uma melhor defesa da infraestrutura, assim identificando pontos a serem melhorados.
- Não possui nem um tipo de ação ou alerta, é totalmente passivo.

## NIDS

- Network Intrusion Detection System.
- Monitora tráfego de rede em tempo real.
- Conecta-se a um switch que possui uma porta espelhada, assim todo o trafego que passa por ele, é espelhado na porta do NIDS para recebimento das informações.

![[Pasted image 20260126222217.png]]

## HIDS

- Host Intrusion Detection System
- Sistema instalado em um Host que monitora invasões analisando as chamadas de sistema, logs, modificações de arquivos, status e etc...
- Coleta as informações e salva em um log, para posteriormente ser encaminhada para a CCM (Centralized Control Module) 

![[Pasted image 20260126223409.png]]

# IPS

- Intrusion Detection System
- É ativo, e realiza ações automatizadas como enviar alertas, dar drop em pacotes maliciosos, bloquear trafego e etc...
- Possível configuração de triggers.