- Media Access Control.
- Camada 2 (Enlace)
- Todos os dispositivos com qualquer tipo de conectividade possui MAC (bluetooth, wi-fi, ethernet).
- Endereço de 48 bits que identifica a interface de rede globalmente, também chamado de MAC address.
- Idealmente é imutável, sendo definido pelo fabricante.
- Além de alguns dispositivos permitem a configuração de seu MAC, também existem softwares que realizam o chamado MAC spoofing, então surge a possibilidade de endereços iguais.

# Casos de Uso

O DHCP associa endereços IP com base no MAC, se seu dispositivo for bloqueado pelo MAC ele não receberá um IP e idealmente ficará sem acesso a comunicação. Idealmente pois dependendo de como esse bloqueio for realizado, é possível ainda setar um IP estático e realizar a comunicação com outros hosts.

Se o destino não está na mesma rede do remetente, é necessário enviar o pacote para o roteador para ele fazer o envio para outras redes. Para isso, o pacote mantém o IP de destino, e o frame ethernet leva o MAC address do roteador.
# Características

Os switches armazenam uma tabela de endereços MAC que foram vistos em cada porta, assim associando determinado MAC a determinada porta. Após isso, o switch passa a disponibilizar as informações que devem ser enviadas ao seu dispositivo, apenas para a porta que contém o seu MAC address vinculado.

As conexões sem fio, normalmente utilizam MAC address para controlar o acesso.
# Estrutura

00:18:44:11:3A:B7 -> conjunto de caracteres hexadecimal, pode ser separado por traços ou vírgulas, mas é muito incomum.