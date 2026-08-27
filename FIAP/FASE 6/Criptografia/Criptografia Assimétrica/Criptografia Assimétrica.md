A criptografia Assimétrica ou também chamada de sistema de chave pública
é um algoritmo criptográfico que utiliza 2 chaves, uma pública e uma privada.

Embora mais seguro que o algoritmo de Criptografia Simétrica é muito mais complexo, por tanto sendo muito mais lento.

# Funcionamento da Criptografia Assimétrica para Confidencialidade

- Beto é o destinatário de uma mensagem.
- O remetente utiliza a chave pública de Beto para cifrar a mensagem.
- Apenas com a chave privada que Beto possui, ele pode decifrar a mensagem que foi cifrada com sua chave pública.

No exemplo acima a **confidencialidade** da mensagem foi garantida, porém é importante ressaltar que a chave privada NUNCA deve ser compartilhada, já a chaves públicas podem ser compartilhadas em diversos diretórios públicos na internet.

```
Qualquer mensagem cifrada com a chave pública só pode ser decriptografada com a chave privada correspondente.
```

# Funcionamento da Criptografia Assimétrica para Autenticação

- Alice cifra uma mensagem com sua chave privada, garantindo assim a autenticidade da mensagem, pois apenas Alice tem acesso a sua chave privada.
- O destinatário ou qualquer um com a chave pública pode verificar a autenticidade da mensagem, vendo que foi realmente Alice que enviou.

```
O destinário de uma mensagem cifrada com a chave privada, só podera decriptografar-la com a chave pública correspondente.
```


# Algoritmos Criptográficos Assimétricos
[[RSA]]
[[SSL e TLS]]
[[DSA]]

[[Algoritmo de Diffie-Hellman]]