  Cross-Site Scripting

O xss consiste em injetar codigo JS no lado do cliente.

# TIPOS DE XSS


| Tipo          | descicao                                                                                         |
| ------------- | ------------------------------------------------------------------------------------------------ |
| Reflected XSS | Quando injetamos codigo JS na pagina e ele e interpretado pelo navegador e executado             |
| Stored XSS    | Quando o codigo e armazenado no banco de dados e executado quando requerido                      |
| DOM XSS       | Quando a entrada o usuario e exibida no navegador e gravada no HTML da pagina como um objeto DOM |
```javascript
#"><img src=/ onerror=alert(document.cookie)>
```

este payload acessa o objeto document do HTML e pega o valor document.cookiem quando o navegador interpreta nossa entrada ela passa a fazer parte do DOM e o JS e exibido como um alert