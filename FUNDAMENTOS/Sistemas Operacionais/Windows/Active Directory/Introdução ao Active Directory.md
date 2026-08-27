O Active Directory(AD) é um serviço de diretórios para redes windows, ele consiste em uma estrutura hierárquica para permitir o gerenciamento de recursos como usuários, computadores, grupos, dispositivos de rede, compartilhamento de arquivos, politicas de segurança, servidores, workspaces e trusts. Além de gerenciamento ele e fornece funções de Autorização e autenticação.

Dentro do AD temos o AD DS (Active Directory Domain Service) que permite o armazenamento de dados em diretórios para deixa-los disponíveis a usuários padrão e administradores. Ele também armazena informações como nomes de usuários, senhas e as permissões para que usuários autorizados acessem informações.

As falhas e configurações incorretas(misconfigurations) do AD muitas vezes podem ser usadas para obter acesso interno, movimentação lateral e vertical e obter acesso não autorizado a um recurso protegido, como, banco de dados, compartilhamento de arquivos, códigos fonte e etc.

O AD é essencialmente, um grande banco de dados acessível a todos os usuários dentro do domínio, independente do seu nível de privilegio, ou seja, mesmo que sua conta tenha permissoes basicas, ela ainda pode ser usada para enumerar serviços como:

|                                  |                                     |
| -------------------------------- | ----------------------------------- |
| Computadores de Domínios         | Usuários de Domínios                |
| Informações do Grupo de Domínios | Unidades Organizacionais (OUs)      |
| Política de Domínio Padrão       | Níveis de domínio funcional         |
| Política de Senha                | Objetos de Política de Grupo (GPOs) |
| Confianças de Domínio            | Listas de Controle de Acesso (ACLs) |
|                                  |                                     |
| Domain Computers                 | Domain Users                        |
| Domain Group Information         | Organizational Units (OUs)          |
| Default Domain Policy            | Functional Domain Levels            |
| Password Policy                  | Group Policy Objects (GPOs)         |
| Domain Trusts                    | Access Control Lists (ACLs)         |