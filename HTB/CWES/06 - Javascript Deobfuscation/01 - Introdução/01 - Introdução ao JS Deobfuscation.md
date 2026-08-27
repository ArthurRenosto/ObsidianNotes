- Análise de código
- Engenharia reversa

# HTML

- Ctrl + U
- Desenvolvedores podem deixar vazar informações em comentários HTML
# CSS

- Pode ser definido internamente no código HTML ou externamente em um arquivo .css e apenas referenciado dentro do HTML


    <style>
        *,
        html {
            margin: 0;
            padding: 0;
            border: 0;
        }
        ...SNIP...
        h1 {
            font-size: 144px;
        }
        p {
            font-size: 64px;
        }
    </style>

No código cima temos um exemplo do CSS definido internamente 
<head>
    <link rel="stylesheet" href="style.css">
</head>

No código a cima temos um exemplo de CSS definido externamente e sendo referenciado no código

# Javascript
- Pode ser definido internamente ou externamente em um arquivo .js e referenciado dentro do HTML

<script src="secret.js"></script>

No código a cima vemos um exemplo do JS sendo usado externamente e apenas referenciado no HTML

Podemos clickar no secret.js para sermos direcionados para o código JS ofuscado

```javascript
eval(function (p, a, c, k, e, d) { e = function (c) { '...SNIP... |true|function'.split('|'), 0, {}))
```
