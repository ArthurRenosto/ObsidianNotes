![[Pasted image 20251231033047.png]]
![[Pasted image 20251231033212.png]]SQLI Band - Mais comum, usa a resposta da aplicacao web pra injection

SQLI error based - Forçar banco de dados a gerar mensagens de erro
' OR 1=1--

SQLI Union Based - Explora o union para retornar mais dados
' UNION SELECT username, password FROM users--

Blind SQL - Enviado de consultas que retorna verdadeiro/Falso, mudanças sutis na resposta fazer aplicativo (conteúdo da página, Categoria: Códigos de status, redirecionamentos
' AND 1=1-- → Page loads normally (True condition)
' AND 1=2-- → Page content changes (False condition)

Time-Based Blind SQLI - nao tem diferença nas respostas, O atacante injeta consultas que fazem com que o banco de dados atrase sua resposta, Se a resposta for atrasada, a condição é verdadeira; caso contrário, é falsa.
