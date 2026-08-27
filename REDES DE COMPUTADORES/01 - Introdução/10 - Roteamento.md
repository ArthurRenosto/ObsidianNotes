- Mecanismo para entrega de pacotes.
- Permite que o roteador analise os possíveis caminhos e determine qual o caminho de preferencia para envio dos pacotes.

# Estático

- Utiliza rotas definidas estaticamente na tabela de roteamento pelo administrador.
- Caso ocorra mudança na infraestrutura é necessário a alteração nas tabelas de roteamento.
# Dinâmico

- A tabela de rotas é preenchida com protocolos de roteamento, que são algoritmos arquitetados para trocarem informações de rotas conhecidas entre roteadores.
- Qualquer alteração na topologia é propagada pela rede, assim todos os roteadores podem atualizar suas tabelas.
# Default

- Conhecidas como "rotas de último recurso"
- Normalmente para redes que não estão na tabela de roteamento, o pacote enviado é descartado, pois o roteador não possui conhecimento da rota
- Utilizando a rota default, o roteador envia o pacote para outro roteador que conheça quele destino.