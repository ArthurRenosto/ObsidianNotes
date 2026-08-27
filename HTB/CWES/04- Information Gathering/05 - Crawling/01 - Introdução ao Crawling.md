- Crawling também é chamado de spidering
- Bots que navegam entre paginas e seus links para descobrir e indexar
# Funcionamento

## (1) Seed URL
- A pagina inicial para rastreamento

## (2) Scan
- Varre a pagina extraindo seus links

## (3) Repeat
- Adiciona os links a uma fila e repete o processo

```txt
Homepage
├── link1
├── link2
└── link3

link1 Page
├── Homepage
├── link2
├── link4
└── link5
```

# Breadth-First Crawling (Amplitude Primeiro)

- Prioriza explorar a largura de um site antes de aprofundar
- Começa rastreando todos os links na seed page
- Passa para os links nessas páginas e assim por diante

![[Pasted image 20251216220603.png]]

# Depth-First (Profundiade Primeiro) 

- Prioriza a profundidade antes da amplitude.
- Segue um único caminho de links, tanto quanto possível
- Volta atrás e explorar outros caminhos

![[Pasted image 20251216220658.png]]