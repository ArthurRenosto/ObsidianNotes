Existem casos onde a entrada do usuario e validada pelo front-end, e por isso deve-se ter uma boa sanitizacao dos dados.

O HTML injection ocorre quando alguma entrada do usuario nao e filtrada e ele consegue inserir codigo HTML, diferente do XSS onde se insere codigo javascript.

Esse codigo HTML pode ser exibido apos ser recuperado de algum comentario no banco de dados, ou exibido diretamente no front-end

# Impacto

O HTML injection pode permitir que modifiquemos alguma pagina de modo que quando encaminharmos o link para alguma vitima, esse link pode conter codigo html alterado, oq poderia ser usado para um formulario de login malicioso por exemplo.

Outro exemplo seria o deface na pagina, onde nos inserimos codigo html na pagina e ele e refletido mudando o front-end.

# Exemplo

![[Pasted image 20251103003056.png]]

inserimos um codigo HTML para vermos se a aplicacao reflete

![[Pasted image 20251103003235.png]]
 a aplicacao exibiu no lugar do nome
 ![[Pasted image 20251103003259.png]]

quando inspecionamos o codigo da pagina, percebemos que nao a nem uma validacao

![[Pasted image 20251103003332.png]]

