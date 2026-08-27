A criptografia garante a **confidencialidade** por meio de cifragem de mensagens, também podendo ser aplicada para garantir a **integridade** de uma mensagem.

- **Criptografar/Encriptar** é o processo onde submetemos um texto puro (clear text) a um algoritmo de criptografia, que codifica a mensagem, deixando-a incompreensível.

- **Decriptografar/Desencriptar** é a reversão do processo criptográfico, restaurando a legibilidade da mensagem.

Exemplos práticos da aplicação da criptografia nos dias de hoje, é a substituição do FTP, TELNET e POP3 que são protocolos que trafegavam os dados em texto puro, para SFTP, SSH, e POP3S que utilizam de algoritmos criptográficos para garantir a confidencialidade da mensagem.

# Ataques relacionados a Criptografia

Em protocolos onde a comunicação acontece em texto puro, um atacante pode realizar o sniffing, colocando sua interface de rede em modo promíscuo (modo de captura e análise de pacotes), capturando os pacotes que trafegam por aquela rede.

![[Exemplo Sniffing.png]]

Posteriormente o ataque pode evoluir para um Man-In-The-Middle (MITM), onde o atacante vira um intermediário invisível entre os hosts, não apenas podendo interceptar pacotes, mas sim podendo fazer adições e modificações de pacotes. Em um cenário ainda mais critico, o atacante pode derrubar um dos host com um ataque DDOS e tomar completamente seu lugar na rede.

![[Exemplo MITM.png]]

# Overhead

É importante intender quais algoritmos criptográficos serão eficientes dentro do seu ambiente computacional, no quesito processamento do sistema e afins, com o objetivo de evitar overhead (desperdício), decorrente dos processos de criptografia e decriptografia.

# Software e Hardware

Os sistemas criptográficos podem ser implementados de duas maneiras.

- Software
	- Geralmente a opção mais barata.
	- Mais lenta em comparação ao hardware.
	- Demanda mais recursos computacionais.

- Hardware
	- Geralmente mais caro.
	- Mais rápido e com menos overhead.
	- Feita através de ASICs (Application Specific Integrated Circuit).
	- Circuito independente da GPU, tratando o processo criptográfico de forma autônoma.

# Sistemas Criptográficos

Para que um algoritmo criptográfico seja considerado seguro, deve cumprir 2 requisitos. 

- A descoberta da chave criptográfica utilizada deve ser praticamente impossível.
- A descoberta decriptografia da cifra sem a chave também deve ser praticamente impossível.

Para isso temos 2 tipos de sistemas baseado em chaves, o sistema de chave privada (ou chave secreta), também chamado de [[Criptografia Simétrica]] e o sistema de chave pública, também chamado de [[Criptografia Assimétrica]].

# Sistemas Hash

Adicionalmente temos os algoritmos baseados em message digest, também chamados de função hash, a função hash não tem como objetivo a confiabilidade e cifra da mensagem, mas sim sua integridade.

Para que elas sejam consideradas seguras, devem apresentar 2 propriedades:

- Baixo nível de colisão, o que significa que a probabilidade de 2 entradas gerarem o mesmo hash, deve ser praticamente nula.
- Garantir que será praticamente impossível reconstruir a mensagem de entrada somente com o hash de saída.

A assinatura digital obtida por meio do uso da criptografia assimétrica e simétrica, infelizmente não pode ser utilizada de forma isolada, assim  sendo necessário o emprego de um mecanismo de [[Algoritmos de Hashing]]