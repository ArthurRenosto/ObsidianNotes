 Hypertext Transfer Protocol
Hypertext Transfer Protocol Secure

# Diferenças

**HTTPS**
- Usa TLS/SSL, as informações entre cliente e servidor vão totalmente criptografadas

**HTTP**
- As informações vão em texto puro, ou seja, podem estar sujeitas a MITM

# Requests

```
http://user@password@sitegamer.com:80/dashbord.php?login.php=true#status
```


| Componente        | Exemplo                   | Descrição                                                                                                                                           |
| ----------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| Scheme(Protocolo) | http://, https://, ftp:// | Protocolo usado na comunicação                                                                                                                      |
| User Information  | admin@jorge123            | Usuário e senha, utilizado apenas em autenticações feitas via http, não muito utilizado hoje em dia                                                 |
| Host              | bancodobrasil.com         | Host que o DNS transforma em IP para poder acessar                                                                                                  |
| Port              | :80                       | Porta da comunicação, se não for especificada, é utilizado a porta padrão do serviço                                                                |
| Path              | /saldodaconta             | Acessando algum diretório ou arquivo da aplicação                                                                                                   |
| Query String      | ?login=true               | Inicio indicado pelo ?, os pares de chave e valor são passados na URL para buscar dados, autenticar etc, podem ser passados vários parâmetros com & |
| Fragment          | \#status                  | Visto apenas pelo navegador, usado para ir até seções do código HTML                                                                                |

# Fluxo

![[Pasted image 20251010224651.png]]

Antes de fazer a requisição ao servidor DNS, o navegador procura em /etc/hosts para ver se o domínio já foi acessado antes

