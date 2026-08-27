Os RCs (Rivest Ciphersou ou cifras ricas) são uma sucessão de diversos outros algoritmos e possibilita maior flexibilidade e segurança do que o é o sucessor do DES Simples.

# RC2

O RC2 cifra por blocos, com entradas até 64 bits, porém, diferente do DES e 3DES ele pode gerar chaves criptográficas de até 2048 bits, mas o tamanho usual para chaves criptográficas é de 128 bits, e ainda pode ser considerado adequado.

Em implementações de criptografia via software, o RC2 é aproximadamente **duas vezes mais rápido** que o DES.

# RC4

O RC4 é uma cifra por fluxo, oque significa que a mensagem em clear text é cifrada de forma continua (bit a bit, byte a byte ou outras formas de unidade de dados) com ajuda de uma chave inserida por um gerador pseudoaleatório. Como RC2, o RC4 pode gerar chaves de tamanho variável, com valor máximo de ate 2048 bits (mas tipicamente sendo de 128 bits).

Em implementações de criptografia via software, o RC4 é aproximadamente **dez vezes mais rápido** que o DES e 3DES.

# RC5

É uma cifra por blocos, é conhecido por sua flexibilidade e possibilidade de parametrização. No RC5 os blocos de entrada podem ter qualquer tamanho predeterminado (32m 64, 128 bits), é possível definir também o tamanho da chave (0-255 bytes) e o numero de interações do algoritmo (0-255).

