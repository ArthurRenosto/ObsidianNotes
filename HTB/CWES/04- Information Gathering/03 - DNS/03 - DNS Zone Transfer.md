- Cópia de todos os registros DNS de uma zona
- Mais eficiente que o Brute Force
- Menos invasivo
 # Funcionamento

![[Pasted image 20251215163945.png]]

## (1) Zone Transfer Request (AXFR)
- Servidor DNS secundário envia solicitação de transferência para o servidor primário
- Usa o tipo AXFR (Transferência completa)

## (2) SOA Record Transfer
- Servidor primário encaminha se registro SOA

## (3) DNS Records Transmission
- Servidor primário encaminha todos os registros

## (4) Zone Transfer Complete
- Servidor primário encaminha mensagem referente ao fim do encaminhamento dos arquivos

## (5) Acknowledgement (ACK)
- Servidor secundário encaminha mensagem de confirmação referente ao recebimento os aquivos
# Explorando

```shell-session
dig axfr @ns1.jorge.com jorge.com
```

**axfr**  -> transferência de zona completa
**\@ns1.jorge.com2** ->  ip do servidor DNS
**jorge.com** -> domínio (zona dns) a ser transferido
