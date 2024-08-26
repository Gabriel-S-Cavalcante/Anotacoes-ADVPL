#banco 



# Resumo:
Função geralmente usada como condição de uma while pois retorna um booleano caso o registro atual da tabela aberta no fonte seja o final da tabela (após a última linha) ou seja, caso a tabela ainda esteja em um índice que exista registro, retorna .T. caso a tabela tenha acabado retorna .F.


# Exemplo:

 cAliasTop := [[MPSysOpenQuery]](cQuery)

  while ! (cAliasTop)->([[EOF]]())
    If (cAliasTop)->A1_LC >= (cAliasTop)->C6_VALOR
	    [[Alert]]("Liberação de venda aprovada! Saldo suficiente!")
    EndIf

 .    (cAliasTop)->([[DBSkip]]())
  EndDo