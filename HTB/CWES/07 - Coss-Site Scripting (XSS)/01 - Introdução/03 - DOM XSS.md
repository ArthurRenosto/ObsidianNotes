# Descrição

O DOM XSS não possui interação alguma com o banco de dados, e ocorre quando o payload JS é executado através do DOM.

# Source & Sink

- **Source:** Objeto JS que recebe a entrada do usuário (parâmetros de entrada, parâmetros na URL, etc)
- **Sink:** Função que grava a entrada do usuário no DOM (document.write(), DOM.innerHTML, DOM.outerHTML, add(), after(), append())

Caso o Sink escreva a entrada sem qualquer validação, a página esta vulnerável a XSS.

```javascript
var pos = document.URL.indexOf("task=");
var task = document.URL.substring(pos + 5, document.URL.length);
```

```javascript
document.getElementById("todo").innerHTML = "<b>Next Task:</b> " + decodeURIComponent(task);
```
# Identificando

```html
<img src="" onerror=alert(window.origin)>
```

Criamos um objeto, que contem um onerror para quando a imagem não é encontrada, então fornecemos um link vazio para ativarmos o onerror.

O payload é passado na URL, logo encaminhamos a mesma para a vítima.
![[Pasted image 20260118031421.png]]