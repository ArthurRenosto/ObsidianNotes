Tem como objetivo garantir que dos interlocutores possam trocar de maneira segura, a chave simétrica que será utilizada para cifragem das mensagens trocadas

![[Exemplo Diffie-Hellman.png]]

- Bob recebe uma cópia da chave pública de Alice, e combina com sua chave privada, gerando assim a chave compartilhada.
- A Mesma coisa acontece com Alice, gerando exatamente a mesma chave compartilhada

O algoritmo de Diffie-Hellman não cifra a mensagem, ele apenas serve para que ambos cheguem na mesma chave compartilhada, sem enviar a chave toda pela rede, apenas a parte pública. Posteriormente essa chave é passada para o algoritmo de criptografia (DES, AES) junto com texto a ser cifrado, e para a decifração, é passado a cifra e a chave.