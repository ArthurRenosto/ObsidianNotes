- faz fuzzing
- enumeracao
- brute force

Burp Intruder pode ser usado para:
- fuzzing de paginas
- diretorios
- subdominios
- parametros
- valores de parametros
- etc
versao gratuita - 1 por segundo
tools baseadas em CLI - 10k ps
burp pro - ilimitado

# alvo

entramos no site que queremos atraves do proxy do burp(ou fazemos um GET) e vamos no historico HTTP.
double click na request que queremos e send to intruder

# positions
estamos usando o sniper attack que nos permite usar 1 payload position , o cluster bomb seriam varias, cada uma com uma wordlist

Selecionamos onde queremos os payloads, clicamos em add e adicionamos o directory
![[Pasted image 20251114000818.png]]

deixar sempre 2 linhas extras no final da request

# PAYLOADS

### Payload position and type

Payload position so temos 1
payload type:

- Simple List: tipo simples
- runtime file: carrega linha a linha como uma varredura, evita o uso exessivo da memoria do burp (melhor para wordlists muito grandes, o burp nao precisa fazer o carregamento previo delas)
- Character Substitution: Especifica uma lista de caracteres subistituiveis

![[Pasted image 20251114001247.png]]

### Payload configuration
![[Pasted image 20251114003437.png]]
### Payload Processing (processamento de Payloads)

podemos usar para adicionar regras confusas sobre uma wordlist.

por exemplo, uma regra de regex que ignore qualquer linha que comeca com .
![[Pasted image 20251114003705.png]]
![[Pasted image 20251114003742.png]]
![[Pasted image 20251114003752.png]]

### payload encoding
Ativar e desativar codificacal da URL
![[Pasted image 20251114004010.png]]

# Configuracoes

Podemos definir número de tentativas em caso de falha de rede ou pausa antes de tentar novamente

GREP - MATCH
permite sinalizar requests especificar dependendo da response
![[Pasted image 20251114004404.png]]

nesse caso demos um clear, adicionamos a regra 200 OK e desativamos o Exclude HTTP headers, ja que nos queremos o status code que fica la

# FUFF
ffuf -u http://94.237.58.116:52788/admin/FUZZ.html -w common.txt -mc 200

ffuf -u http://94.237.58.116:52788/admin/FUZZ -w common.txt -mc 200