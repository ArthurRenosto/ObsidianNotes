O DES (Data Encryption Standart ou Padrão de encriptação de Informações) é uma cifra de bloco, ou seja, um bloco de entrada de 64 bits em texto plano é tratado afim de produzir outro bloco de 64 bits, porém desta vez, cifrado. Entretanto, como a chave criptográfica do DES é comprimida, ela tem o tamanho de 56 bits, se tornando insegura para os padrões atuais.

No 3DES (Triple  Data  Encryption  Standard ou padrão  de criptografia de dados triplo) o algoritmo DES é aplicado 3 vezes com 3 chaves distintas de 56 bits, tendo assim, o comprimento final de 168 bits. No 3DES a mensagem é cifrada pela chave K1, o resultado é cifrado pela chave K2, e sequencialmente, cifrado pela chave K3

![[Exemplo 3DES.png]]

Também é possível ao invés de se utilizar 3 chaves, utilizar apenas 2, assim a mensagem é cifrada pela chave K1, em sequencia pela chave K2 e novamente pela chave K1, tendo assim uma chave com tamanho de 112 bits.

