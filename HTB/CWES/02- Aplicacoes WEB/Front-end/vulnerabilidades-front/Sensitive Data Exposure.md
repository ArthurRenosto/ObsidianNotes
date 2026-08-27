A vulnerabilidade se baseia na exposicao de dados sensiveis em plain text para o usuario final. isso e geralmente encontrado no codigo HTML da pagina.

As vezes o desenvolvedor desabilita a opcao de inspecionar elemento, mas ainda podemos visualizar o codigo HTML da pagina usando um proxy como burp suite.

Verificamos o codigo HTML e JS da pagina em busca de credenciais de acesso deixadas pelos desenvolvedores, normalmalmente em comentarios.

Podemos procurar por diretorios de teste, parametros de debugging, funcionalidades ocultas etc.

Assim como existem ferramentas automatizadas para fazer isso, os desenvolvedores tambem podem usar ofuscacao de JS para impedir as ferramentas automatizadas de acharem algo.