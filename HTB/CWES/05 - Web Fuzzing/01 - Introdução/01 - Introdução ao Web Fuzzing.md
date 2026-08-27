- Testes automatizados com entradas inesperadas

# Fuzzing != Brute Force

## Fuzzing
- Entradas inesperadas
- Utilizam listas de payloads que incluem dados mal formados, caráteres aleatórios ou inválidos e etc
- O objetivo é ver como a aplicação reage

## Brute Force
- Abordagem direcionada
- Utilizam wordlists com valores padronizados
- Objetivo é explorar muitas possibilidades de um valor especifico

# Casos de uso

## Vulnerabilidades Ocultas
- Pode descobrir vulnerabilidades que scanners não detectam

## Validação de Inputs
- Identificar falhas nas validações, permitindo XSS e SQLIs

## Information Gathering
- Descoberta de diretórios e subdomínios

# Ferramentas

## FUFF
- Enumeração de diretórios e arquivos
- Descoberta de parâmetros
- Brute Force

## Gobuster
- Descoberta de conteúdo
- Enumeração DNS
- Detecção de WordPress

## FeroxBuster
- Scan Recursivo
- Descoberta de conteúdo não vinculado
- Scans de alta performace

## wfuzz/wenum
- Enumeração de diretórios e arquivos
- Descoberta de parâmetros
- Brute Force