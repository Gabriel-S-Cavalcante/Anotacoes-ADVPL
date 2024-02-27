#banco #insert



# Resumo:
Trava a tabela que for passada por parâmetros para permitir que seja inserido novos dados nela, necessário liberar a tabela após a inserção com o [[MsUnlock]]()



# Exemplo:


 [[RecLock]]("SA6", .T.)
   SA6->A6_FILIAL        := "01"
   SA6->A6_COD          := [[AllTrim]](cA6_COD)
   SA6->A6_AGENCIA   := [[AllTrim]](cA6_AGENC)
   SA6->A6_NUMCON  := [[AllTrim]](cA6_NUM)
   SA6->A6_NOME       := [[AllTrim]](cA6_NOME)
 [[MsUnlock]]()