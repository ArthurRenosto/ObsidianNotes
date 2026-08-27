- Cross Site Request Forgery
- Camada 7 (Aplicação)
- Severidade Alta
- Engenharia Social | Falta de Parametrização
# Descrição

O CSRF é uma vulnerabilidade que foça a vítima a executar ações em uma aplicação que ela esteja logada.

Usando engenharia social o atacante pode encaminhar um link que quando a vítima clickar, ela vai executar uma ação no site utilizando seu cookie/token de autenticação, e o site vai achar que é uma ação legitima.

# Objetivo

O CSRF tem como objetivo ações que mudem o estado do servidor, como:
- Alteração do próprio endereço de e-mail
- Alteração da própria senha
- Efetuar transações

# CSRF Storage

Armazenar um script na aplicação por meio de uma tag IMG ou IFRAME em um campo que aceita HTML 
