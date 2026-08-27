# Capturando Respostas HTTP
proxy settings -> response interception
![[Pasted image 20251111180834.png]]

# Exibindo campos ocultos
![[Pasted image 20251111181547.png]]

# Modificacao HTTP baseada em regras 

Proxy > Proxy settings > HTTP match and replace rules > Add
![[Pasted image 20251111202655.png]]
Match: ^User-Agent.*& -> Procura a linha do User Agent para subistituir
Replace: subi 

# Modificando Response

Proxy > Options > Match and Replace
![[Pasted image 20251112182540.png]]

# Reenviando Requests

proxy > http history > right click na request > send to repeter
![[Pasted image 20251112184749.png]]

# Codificando
codificando em URL
![[Pasted image 20251112220458.png]]

![[Pasted image 20251112221952.png]]

# Configurando Proxychains

baixamos o proxychains
```
sudo pacman -S proxychains-ng
```

editamos o arquivo de configuracao do proxy chains
```
micro /etc/proxychains.conf
```

comentamos a ultima linha e adicionamos nosso proxy

```
#socks4 	127.0.0.1 9050
http 127.0.0.1 8080
```

usamos o proxychains em alguma ferramenta cli para interceptar seu trafego
![[Pasted image 20251113224233.png]]

usamos o -q para suprimir os alerts de conexao

## Proxy no metasploit

usamos o proxy no metasploit
![[Pasted image 20251113225034.png]]
