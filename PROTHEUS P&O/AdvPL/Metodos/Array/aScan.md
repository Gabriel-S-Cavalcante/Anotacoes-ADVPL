#array




# Resumo:
Retorna a posição no [[Array]] do valorBuscado


# Uso:
aScan(Array, valorBuscado)



# Exemplo:

local aArray   := {"Gabriel", "Fábio", "Rodrigo"}
local cBusca   := "Gabriel"
local nPosi     := 0

nPosi := aScan(aArray, cBusca)

Tendo como busca o nome "Gabriel" o valor atual de nPosi é 1.


# Obs:
Diferente de outras linguagens a indexação em ADVPL começa a contar a partir do número 1 ao invés do 0.