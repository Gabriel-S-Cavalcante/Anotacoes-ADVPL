#banco 



# Resumo:
Função que pula linha da tabela aberta no fonte

# Exemplo:
Como exemplo, para iterar uma tabela que foi retornada por uma Query, precisamos utilizar o While e para seguir para a próxima linha devedor utilizar o [[DBSkip]]() no final.

 cAliasTop := [[MPSysOpenQuery]](cQuery)

  while ! (cAliasTop)->([[EOF]]())
    If (cAliasTop)->A1_LC >= (cAliasTop)->C6_VALOR
	    [[Alert]]("Liberação de venda aprovada! Saldo suficiente!")
    EndIf

 .    (cAliasTop)->([[DBSkip]]())
  EndDo