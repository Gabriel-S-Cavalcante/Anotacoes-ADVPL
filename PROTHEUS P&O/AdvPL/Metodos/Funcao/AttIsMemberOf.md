#objeto



# Resumo:
Verifica e retorna um valor booleano sobre a existência de uma propriedade em um objeto


# Exemplo:
Utilizando o objeto criado na função [[xmlparser]]

 
oCelulaXML  := oNotaxml:\_WorkBook:\_WorkSheet:\_Table:\_Row\[1]:\_Cell
lExisteValor   := [[AttIsMemberOf]](oCelulaXML, "\_Data")

Se a Celula da primeira linha o arquivo .xml exister a propriedade \_Data (Dado),
a variável lExisteValor vai ter o valor de .T. caso não exista vai ter o valor de .F. 






