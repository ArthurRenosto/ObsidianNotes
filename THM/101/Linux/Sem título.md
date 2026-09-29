# SSH

- Secure Shell (SSH), usado para se conectar remotamente a uma maquina.
- Interage com ela via CLI.
- Dados sao criptografados na comunicação.

ssh user@ip

# FLAGS & SWITCHES

- podemos usar flags para que nossos comandos tenham mais informações ou comportamentos diferentes

--help -> abreviação do manual
man -> documentação da ferramenta

*ADICIONAR TABELA*

# Permissões

su -l user2 -> nos permite cai no diretorio home do usuario

r - read
w - write
x - execute

```bash
rwxrwxrwx
```

primeiros 3 - propietario
proximos 3 - grupo
ultimos 3 - outros

r = 4
w = 2
x = 1

proprietario - 4 + 2 + 1 = 7
grupo - 4 + 2 + 1 = 7
outros - 4 + 2 + 1 = 7

* TABELA *

chmod 750 arquivo.txt

# DIRETORIOS COMUNS

/etc -> armazena arquivos usados pelo OS, como  o arquivo sudoers, passwd e shadow

/var -> armazena dados variaveis, que estao sendo usados por aplicativos em execução, ou logs em /var/logs também sao armazenados em /var/logs arquivos nao associados a um usuario especifico

/root -> diretorio home do usuario root

/tmp -> amazena dados que sao acessados uma ou duas vezes, quando o computador é reiniciado essa pasta é limpa, por padrão qualquer usuario pode escrever nessa pasta, servindo para armazenas scripts.