scanner de vulnerabilidades open source
escrito em go
serve para aplicações web, APIs, redes, DNS e nuvem.

# como funciona

possui em engine : logica do programa

templates: scripts escritos em YAML que definem oq o escanner deve procurar

**Lógica do Código:**

- Define o método HTTP (ex: `GET`).
    
- Define o caminho (path) que será testado (no exemplo, ele procura pelo arquivo `readme.txt` dentro da pasta do plugin WooCommerce no WordPress).
    
- **Matchers (Validadores):** Usa RegEx (Expressões Regulares) para verificar se o arquivo existe e extrair a versão do plugin instalada.

# como usa

nuclei -u servidor.com

baixar templates
