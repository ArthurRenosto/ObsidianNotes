	
Filosofia

| Princípios                                 | Explicação                                                                                                                                                                                                                      |
| ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Tudo é um arquivo                          | No Linux, arquivos, dispositivos, processos, tudo é representado como um arquivo, o que significa que o usuário pode interagir com um documento de texto, da mesma forma que interage com um processo                           |
| Programas pequenos e de propósito único    | Muitos programas podem são pequenos e focados em uma tarefa específica                                                                                                                                                          |
| Capacidade de encadear programas           | A possibilidade de encadear programas entre si, usando pipe( \| ) por exemplo, assim permitindo que a saída de um programa, seja a entrada de outro                                                                             |
| Evitar interfaces de usuários restritivas  | A principal interação do usuário com o sistema, ocorre no terminal, onde o usuário pode acessar recursos  e criar automações que em uma GUI não seria possível                                                                  |
| Dados de configuração em arquivos de texto | As configurações de serviços e programas ficam armazenadas em arquivos de texto, o que significa que o usuário pode acessar e modificar diretamente, como exemplo temos o /etc/passwd que gerencia todos os usuários do sistema |

Componentes

| Componentes    | Descrição                                                                                                                                                                                                                                                  |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Bootloader     | Pequeno pedaço de código que é executado para para guiar o processo de boot para o sistema operacional. Como exemplo temos o GRUB.                                                                                                                         |
| Kernel         | Gerencia Recursos como memória, CPU, dispositivos de entrada e saída, interagindo diretamente com o hardware e software.                                                                                                                                   |
| Daemons        | São os serviços que rodam em segundo plano no Linux. Eles garantem o funcionamento de tarefas como, agendamento, impressão, rede e som. Os Daemons são iniciados automaticamente após o login.                                                             |
| Shell          | O shell ou interpretador de linguagem de comando (CLI) , é a interface entre o sistema operacional e o usuário que permite enviar comandos e executar programas. Como exemplo temos o Bash, Zsh, Ksh, Tcsh/Csh e Fish.                                     |
| Graphic Server | Fornece um subsistema gráfico chamado de X ou X-server, e permite que programas com interfaces grafias sejam executados, diferente do Window Manager o Graphic Server não exibe nada na tela, apenas gerencia como e onde os programas exibem seu gráfico. |
| Window Manager | Conhecido como GUI ou Desktop Environment é o que o usuário vê e interage, temos como exemplo: GNOME, KDE, MATE, e geralmente alguns Desktop Environment incluem utilitários de sistema como navegadores;                                                  |
| Utilities      | Executam funções especificas, dês de cp, mv, top até navegadores e editores de texto                                                                                                                                                                       |

Arquitetura do Linux


| Camada         | Descrição                                                                                                                                         |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| Hardware       | Dispositivos fisicos como, RAM, SSD, CPU, etc.                                                                                                    |
| Kernel         | Núcleo do Linux, responsável por virtualizar os recursos do hardware e dando a cada processo seus próprios recursos, evitando conflito entre eles |
| Shell          | Uma interface CLI para os usuários inserirem comandos                                                                                             |
| System Utility | Utilitários de sistema que permitem o usuário copiar, colar, monitorar, configurar serviços e etc.                                                |

