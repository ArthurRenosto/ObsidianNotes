# front end

Inclui o HTML CSS e JS interpretado pelo nosso navegador

- Conceito visual de web design
- User interface(UI)design
- User experience(UX)desing

# back-end

Componentes do backend

| Componente             | descricao                                                                                                                                                          |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Back-end Servers       | Hardware e sistema operacional que executa os componentes, geralmente sao Linux ou containers, mas podem ser windows                                               |
| Web Servers            | Lidam com solicitacoes HTTP, como Apache NGINX e ISS                                                                                                               |
| Databases              | Sao os bancos de dados(DBs), servem para armzenar e recuperar dados, podem ser relacionais(MySQL, MSSQL, Oracle, PostgreSQL), ou nao relacionais(NoSQL e MongoDB)\ |
| Development Frameowrks | Sao frameworks de desenvolvimento usados para aplicacoes web, como Laravel(PHP), ASP.NET(C#), Spting(Java), Django(Python) e Express(NodeJS Javascript)            |
![[Pasted image 20251031181908.png]]

Tambem e possivel isolar os componentes da aplicacao web em diferentes servidor ou conteiners, para mitigar o impacto de vulnerabilidades, bancos de dados, back end de aplicacoes etc.

trabalhos realizados pelo back-end

- Desenvolver a lógica principal e serviços do back-end da aplicação web
- Desenvolver o código principal e funcionalidades da aplicação web
- Desenvolver e manter o banco de dados back-end
- Desenvolver e implementar bibliotecas para serem usadas pela aplicação web
- Implementar necessidades técnicas/de negócios para a aplicação web
- Implemente as principais APIs para comunicações de componentes front-end
- Integrar servidores remotos e serviços em nuvem no aplicativo web
# Protegendo front/back end

20 erros mais comuns de se encontrar em aplicacoes web

1- Permitir a insersao de dados invalidos no banco de dados
2- concentrando-se na aplicacao como um todo
3- estabelecer metodos de seguranca desenvolvidos pessoalmente(vozes na cabeca)
4- tratando a seguranca como ultimo passo
5- armazenamento de senhas em plain text
6- Senhas fracas
7- Armazenamento de dados nao criptografados
8- Depender do client-side
9- ser muito otimista(ng vai atacar saporra kkk)
10- variaveis atraves da URL
11- confiar em codigo third party
12-  credenciais no cod
13- entrada de SQL nao verificada
14- inclusao de arquivos remotos
15- tratamento de dados inseguro
16- deixar de criptografas as parada de um jeito descente
17- ignorar a camada 8
19- olha bem a bomba que o user ta fazendo
20- configurar o waf que nem o cu

https://owasp.org/www-project-top-ten/

![[Pasted image 20251031204657.png]]

