#banco #consulta


# Resumo:
Busca na tabela que foi aberta pelo [[DBSelectArea]] o valor que foi passado como parâmetro e move a tabela do SelectArea para a respectiva linha.

Faz exatamente a mesma coisa que o DBSeek() porém de modo mais performático.

# Syntax:

[[MsSeek]](filial + dado procurado)



# Exemplo:

[[DBSelectArea]]("SA6")

  if ([[MsSeek]]([[FWxFilial]]("SA6") + cCod))
    cAgen := [[AllTrim]](A6_AGENCIA)
    cNome := [[AllTrim]](A6_NOME)
  else
    [[Alert]]("Não foi encontrado nenhum banco registrado para o código: " + cCod)
    Return
  EndIf


