#outputBox 



# Resumo:
Cria uma barra de processamento com base no item atual a ser processado de uma lista e o número total de itens na lista


# Uso:
Processa({| | Função }, "Título" )



# Exemplo:

User Function Exemplo1()
  Local cResult   := ''  // Variável que receberá o retorno da função Exemplo2

  Processa({| | cResult := Exemplo2()}, "Contando tipos de itens")

  [[FWAlertInfo]](cResult, "Resultado do Exemplo")

Return Nil



Static Function Exemplo2()
  Local aDados     := {1, "Hello", 2, 3, "World", 4, 5, 6, "GPS",7 ,8 ,9, "AdvPL"}
  Local cResult     := ''
  Local nTotal       := [[Len]](aRetorno)
  Local nAtual      := 0
  Local nChars     := 0
  Local nNums     := 0
  Local nX            := 0

  ProcRegua(nTotal)

  For  nX:=1 to [[Len]](aDados)
    If       [[ValType]](aDados\[nX]) == "C"
		nChars++
    ElseIf [[ValType]](aDados\[nX]) == "C"
	    nNums++
    EndIf
	IncProc("Separando tipos: " + cValToChar(nX) + " de " + cValToChar(nTotal) + "...")
  Next nX

  cResult  := "Quantidade de tipos de dados"         +CRLF+;
           "Caracteres:  " + cValToChar(nChars)    +CRLF+;
           "Numeros:    " + cValToChar(nNums)

Return cResult