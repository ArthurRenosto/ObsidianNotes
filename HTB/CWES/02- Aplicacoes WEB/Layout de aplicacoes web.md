
| Categoria                                                            | Descricao                                                                                                                                                                                                                                                                                                     |
| -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Web Application Infrastructure(Infraestrutura de aplicativos da Web) | Base fisica e logica, como banco de dados(MySQL), Servidores(Apache), servidor para front-end e APIs, Integracoes com DNS, SSL, WAFs                                                                                                                                                                          |
| Web Application Components (Componentes de aplicativos web)          | As partes que compoe a aplicacao web em si, o que o usuario ve e o que o sistema executa internamente:<br>UX/UI components: botoes, formularios, layouts<br>Client components: codigo que roda no navegador, HTML, CSS, JavaScript<br>Server components: APIs, autenticacao, comunicacao com o banco de dados |
| Web Application Architecture(Arquitetura de aplicativos da Web)      | Define como todos os componentes interagem entre si<br>Cliente se comunica ao servidor(HTTP, REST)<br>Como o servidor se conecta ao banco de dados                                                                                                                                                            |

# Infraestrutura de Aplicacoes Web

As diferentes configuracoe de infraestrutura das aplicacoes web sao chamadas de models. Os mais comuns podem ser agrupados de 4 tipos:

### Client-Server

Usado na maioria das aplicacoes web, o servidor hospeda a aplicacao, e distribui para quais quer clientes que solicitar
![[Pasted image 20251030003701.png]]

Neste modelo a aplicacao web possui o back-end do lado do servidor, e o frontend do lado do cliente sendo renderizado pelo browser

Cliente acessa uma pagina -> navega pela mesma -> clicka para trocar de pagina -> browser faz uma requisicao GET para o servidor -> servidor processa e responde
### One Servidor

Toda a aplicacao web ou ate mesmo mais aplicacoes web, seus componentes e banco de dados estao hospedados em um unico servidor
![[Pasted image 20251030004622.png]]
Uma vez que qualquer uma das aplicacoes web hospedadas esta vulneravel, todas as outras estao comprometidas

se o servidor web cair, todas caem

### Vários Servidores - Um Banco de Dados

O banco de dados e isolado em um servidor separado e todos os outros servidores que hospedam aplicacoes web, acessam ele
![[Pasted image 20251030005510.png]]

podem utilizar os mesmos dados, caso necessario

Vários Servidores - Vários Bancos de Dados

Os dados de cada aplicativo web, sao hospedados de forma separada em seu banco de dados especifico,

### componentes de aplicacoes web

- Client
	- front-end

- Server
	- Web server: Apache, Nginx
	- back-end: Python, node
	- banco de dados: MySQL, PostgreSQL

- Services(microservicos)
	- Integracoes com servicos externos: APIs de pagamento

- Function (ServerLess)

### Arquitetura de aplicacoes web


| Camada             | Descricao                                                                                                                 |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------- |
| Presentation Layer | Front-end, acessador pelo navegador do cliente, e sao retornadors em forma de HTML, CSS e Javascript                      |
| Application Layer  | Garante que as solicitacoes do cliente sejam corretamente processadas, verifica coisas como, autorizacao, privilegios etc |
| Data Layer         | trabalha com a camada de aplicacao para armazenar os dados na db                                                          |
![[Pasted image 20251031153831.png]]

### microservicos

componentes independentes de aplicativos web, geralemente programados apenas para uma tarefa.

Ao inves de ter uma API que faz tudo, sao divididos em servicos como: inscricao, pagamento, pesquisa etc

os microservicos podem ser escitos em diferentes linguagens e ainda sim interagir entre si

### serverless

Provedores de nuvem como AWS, GCP e azure oferecem servidores para empresas construirem aplicativos web executados em conteiners (docker), isso da liberdade para a empresa executar aplicativos web sem se preucupar com a infraestrutura

### Arquitetura de seguranca

Ao realizar pentests, e importante entender arquitetura de seguranca pois algumas vezes a falha pode nao ser de programacao, mas sim um erro de design em sua arquitetura

Por exemplo, um aplicativo web individual pode ter toda a sua funcionalidade principal segura implementada. No entanto, devido à falta de medidas de controle de acesso adequadas em seu projeto, ou seja, o uso do [Controle](https://en.wikipedia.org/wiki/Role-based_access_control) de [Acesso Baseado](https://en.wikipedia.org/wiki/Role-based_access_control) em [Funções (RBAC),](https://en.wikipedia.org/wiki/Role-based_access_control) os usuários podem acessar alguns recursos de administração que não se destinam a serem diretamente acessíveis a eles ou até mesmo acessar as informações privadas de outros usuários sem ter os privilégios para fazê-lo. Para corrigir esse tipo de problema, uma mudança significativa de design precisaria ser implementada, o que provavelmente seria caro e demorado.

Outro exemplo seria se não conseguirmos encontrar o banco de dados depois de explorar uma vulnerabilidade e ganhar controle sobre o servidor de back-end, o que pode significar que o banco de dados está hospedado em um servidor separado. Podemos encontrar apenas parte dos dados do banco de dados, o que pode significar que existem vários bancos de dados em uso. É por isso que a segurança deve ser considerada em cada fase do desenvolvimento de aplicações web, e os testes de penetração devem ser realizados ao longo do ciclo de vida de desenvolvimento de aplicações web.