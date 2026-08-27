- Utilizado em estruturas complexas

# Funcionamento
## (1) Fuzzing Inicial
- Começa no diretório root (/)
- Envia as request
- Analisa o status code

## (2) Expansão
- Pega o diretório válido
- Inicia um fuzzing em cima dele

## (3) Repetição
- O processo se repete para cada diretório válido
- Continua até o limite de profundidade definido

# Sobrecarga
- Em grandes aplicações web o fuzzing recursivo pode sobrecarregar o servidor
- Usar flags para definir limites

# Utilizando FFUF
[[03 - Fuzzing de Diretórios e Arquivos]]