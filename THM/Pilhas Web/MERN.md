- MERN(MongoDB, Express.js, React, Node.js)
- Utilizada em grande parte dos SaaS e APIs.
# Identidade
- Escolha padrão para aplicações somente JS.
- No ubuntu a implementação padrão é Node.js do NodeSource PPA, Express ouvindo na porta 3000 ou 5000.
- MongoDB na porta 27017.
- Um reverse proxy (geralmente nginx) fica na frente em produção, porém em ambientes mal configurados o express é exposto diretamente.
# Fingerprinting
## Headers

![[Pasted image 20261011131026.png]]

- `X-Powered-By: Express` -> O Express envia esse header em todas as responses por padrão. O desenvolvedor pode explicitamente desativa-lo ou adicionar um helmet middleware.
- `Set-cookie: connect.sid=` -> Este cookie é utilizado pelo middleware express-session com a opção `saveUninitialized` definida como true. Porém se ela estiver definida como false o cookie não aparece em requests não autenticadas.
## Endpoint Inexistente 

![[Pasted image 20261012140357.png]]

- `Cannot GET /nonexistent` -> Uma aplicação Express com configurações padrão retorna em plain text um endpoint inexistente.
- Distinto de Django(exibe um erro HTML), Apache(exibe erros 403 ou 404) e Next.js(exibe uma pagina de erro HTML estilizada).

# Enumeração da superfície API

- Descobrir quais rotas existem, quais métodos HTTP aceitam, quais dados recebem e quais permissões exigem.
- As aplicações MERN geralmente possuem APIs JSON para atualização de perfil, preferências, configurações de usuários e etc.

![[Pasted image 20261012142307.png]]

- Podemos salvar nosso cookie de sessão e tentar utilizar uma rota de update de usuarios.
- É possível perceber que o endpoit aceita chaves JSON e mesclas no objeto do usuário sem filtragem.
# Prototype Pollution
## Prototype 

- Um prototype(protótipo) é um objeto que outro objeto pode consultar para encontrar propriedades e métodos que não possui diretamente.

```js
const animal = {
    respirar: true
};

const cachorro = Object.create(animal);

cachorro.nome = "Rex";

console.log(cachorro.nome);      // Rex
console.log(cachorro.respirar);  // true
```

- Quando o JavaScript procura a propriedade `respirar` em cachorro ele não encontra, então procura no protótipo `animal`e encontra.
- Essa relação é chamada de prototype chain.
### Object.prototype

- É um protótipo padrão para muitos objetos.

## Merge Function

- Uma função que recebe dois ou mais objetos e combina suas propriedades em um único objeto.

```js
const user = {
    nome: "Balio",
    tema: "claro"
};

const updates = {
    tema: "escuro",
    idioma: "pt-BR"
};

Object.assign(user, updates);

console.log(user);
```

- Utilizando a função merge(mesclagem) `Object.assign()`.

```js
{
    nome: "Balio",
    tema: "escuro",
    idioma: "pt-BR"
}
```

# Explorando 