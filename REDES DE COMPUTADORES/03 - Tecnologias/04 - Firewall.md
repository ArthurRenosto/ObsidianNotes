- Tem como objetivo, aplicar políticas de segurança. 
- Dispositivo de uma rede de computadores na forma de um software ou hardware, a combinação de de ambos é chamada de appliance.
- O firewall de hardware possui um OS especializado para rodar o software de firewall, isso faz com que a eficácia seja maior. 
- NGFW (Next-Generation Firewall), possui tecnologias de IA, deep learning, sandbox e etc...

![[Pasted image 20260126200547.png]]


# Tipos de Firewall

- Filtros de Pacote
- Proxy Firewall
- IDS
- IPS

# UTM (Unified Threat Manager/Gerenciador Unificado de Ameaças)

- Termo que se refere a uma solução de segurança que em um único dispositivo, oferece várias soluções, como: antivirus, antispyware, antispam, firewall de rede, NAT, VPN e etc.

# Mecanismos de Filtragem

## Stateless (Sem estado)

- Avalia cada pacote de maneira individual.
- Não possui conhecimento da conexão como um todo.
- Todos os pacotes são avaliados pelo firewall, independente de ser uma conexão nova ou já existente.

## Stateful (Com estado)

- Mantém uma tabela de estados.
- Conhece a conhece a conexão com um todo, sabe quais conexões estão estabelecidas, novas ou relacionadas.
- Só avalia totalmente o primeiro pacote da conexão, os demais pacotes são liberados por fazerem parte de uma conexão válida.