# Gobuster

| Flag                  | Descrição                         |
| --------------------- | --------------------------------- |
| -s 200, 301,          | apenas esses status code          |
| -b 404                | remove esses status code          |
| --exclude-length 0,15 | remove respostas de 0 ou 15 bytes |
# FFUF


| Flag            | Descrição                                                               |
| --------------- | ----------------------------------------------------------------------- |
| -mc 200,300,301 | Apenas respostas com status code especificado                           |
| -fc 404         | Remove respostas com status code especificado                           |
| -fs 0-1023      | Remove respostas com tamanho de bytes  entre o especificado             |
| -ms 3456        | Apenas respostas com tamanho de bytes especificado                      |
| -fw 219         | Remove respostas com determinada quantidade de palavras                 |
| -mw 5-10        | Apenas respostas com quantidade especifica de palavras                  |
| -fl 10          | Remove respostas com numero especificado de linhas no corpo da resposta |
| -ml 20          | Apenas respostas com numero especificado de linhas no corpo da resposta |
| -mt > 500       | Apenas respostas com determinada condição de tempo para o primeiro byte |
