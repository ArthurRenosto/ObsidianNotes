A assinatura da criptografia assimétrica não pode ser usada de forma isolada, é necessário empregar o mecanismo de Hashing para uso adequado da assinatura digital.

Na prática é inviável utilizar puramente algoritmos assimétricos para assinaturas digitais, principalmente quando se deseja assinar um grandes mensagens, pois podem levar minutos ou até mesmo horas para serem cifradas com a chave privada de alguém. Em vez disso é empregada uma função hashing, que gera um valor pequeno, de tamanho fixo, derivado da mensagem  que  se  pretende  assinar,  de  qualquer  tamanho, para oferecer  agilidade nas assinaturas digitais, além de integridade confiável

A função Hash serve para garantir a Integridade do conteúdo da mensagem, assim, uma vez o hash de uma mensagem ser gerado por qualquer algoritmo de hashing, qualquer modificação em seu conteúdo resultara em uma mensagem totalmente diferente da original

# Características da função Hash

- **Unidirecionalidade** A partir do valor de uma hash, deve ser computacionalmente inviável recuperar a mensagem original
- **Compressão**  Independente do tamanho da mensagem em clear text, o hash sempre terá um tamanho fixo, geralmente o hash tem sempre um tamanho menor.
- **Facilidade de cálculo** Independente da mensagem deve ser rápido e eficiente de calcular o hash
- **Difusão** uma pequena mudança na mensagem inicial, deve causar uma grande mudança no hash
- **Resistência a colisões** Deve ser impossível duas mensagens diferentes chegarem no mesmo hash

# Algoritmos de Hashing

Exemplos de algoritmos de cálculo de hash: md4, md5, sha1, sha256, sha512

![[Tabela Hashes.png]]

# Cracking de Hash

[[Identificando Hashes]]
Há   vários sites na  Internet  especializados  em  “crackear” hashespara recuperação         das         respectivas         senhas, como         o         HashKiller(https://hashkiller.io/listmanager) dentre outros, bem como, softwares com a mesma finalidade, a exemplo do HashCat e John the Ripper.

# Tipos de Cifras

[[Transposição]]
[[Base 64]]
