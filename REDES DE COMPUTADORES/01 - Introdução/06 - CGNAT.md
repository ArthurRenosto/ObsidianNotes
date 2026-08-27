- Carrier Grade NAT
- Técnica adotada por ISPs para utilizar um único IP válido para vários clientes.
- Vários clientes possuem o mesmo IP dentro do CGNAT, porém com portas diferentes, para diferenciação.
- Por conta do CGNAT, não podemos abrir portas em nosso roteador, tanto por conta do IP público não ser nosso e sim do ISP, quanto por conta de que isso faria com que ele conflitasse com o IP válido de outro cliente.
- Diferente do IP privado e IP público, o IP dentro do CGNAT é chamado de IP Inválido.

![[Pasted image 20260125132153.png]]

