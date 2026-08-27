# Classes

- Classes são categorias de IP segmentadas por tamanho, ou seja, por sua capacidade máxima de IPs.
- Dentro de cada classe temos o CIDR (Classless Inter-Domain Routing).

## Classe C

- Possui o /24, muito utilizado em redes domesticas
- O /24 detém 254 IPs para uso, visto que o primeiro (Identifica a própria rede) e o ultimo (Broadcast) são reservados.

![[Pasted image 20260124232912.png]]

## Classe B

![[Pasted image 20260125111605.png]]
## Classe A

![[Pasted image 20260125111624.png]]

# Sub-redes

- São utilizadas para segmentar as redes e evitar o desperdício de IP
- Seria possível pegar uma rede doméstica /24 e transforma-la em /25, tendo assim, 2 redes com 128 IPs cada.
# IPs Reservados

![[Pasted image 20260125131748.png]]