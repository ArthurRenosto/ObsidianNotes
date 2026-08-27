- Transmission Control Protocol
- Camada 4 (Transporte)

# Características

- **Orientado a conexão**, necessita de, estabelecer uma conexão Antes de começar o envio dos dados. No caso do TCP por meio do 3-way handshake.
- **Ponto a Ponto (P2P)**, a comunicação sempre ocorre entre 2 dispositivos conectados.
- **Full duplex**, permite o envio simultâneo de dados entre o client e o server.
- **Controle de congestionamento**, reduz a taxa de envio quando detecta congestionamento na rede, o TCP faz essa detecção com base em ACKs recebidos e no RTT (Round Trip Travel/Tempo de Ida e Volta).
- **Confiabilidade**, garantindo a entrega de todos os pacotes na ordem correta.

# SYN (Synchronize)

- Sinalização usada para iniciar a conexão.
- Cliente envia um segmento com a flag SYN para o servidor para indicar que deseja se conectar e sincronizar os números de sequência.
- O número de sequencia que o client envia no começo da comunicação, é um identificador único para aquela tentava de conexão.

# ACK (Acknowledgment)

- Sinalização que indica a confirmação do recebimento dos dados.

# Three-Way Handshake

- Mecanismo de estabelecimento e finalização da conexão.
- Realiza a Orientação da Conexão.

## SYN

- A abertura da conexão é realizada quando o cliente encaminha o segmento com a flag SYN, e define o número de sequencia como um valor aleatório.

## SYN + ACK

- O servidor responde com um segmento SYN-ACK
- O servidor define o número de reconhecimento do como sendo, o número de sequencia do cliente + 1 (ACK = num de seq + 1), confirmando o recebimento do SYN.
- O servido escolhe um novo número de sequência aleatório.

## ACK

- O cliente responde o servidor com um segmento apenas com a flag ACK, contendo (ACK = B + 1) 