#string 



# Resumo:
Retorna a parte selecionada por parametro de uma string também passada por parâmetro



[[SubStr]](String a ser consultada, Indice do inicio, quantidade de caracteres)

# Exemplo:

local cString     := "GrupoGPS"
local cSubStr1  := ""
local cSubStr2  := ""
local cSubStr3  := ""

cSubStr1 := [[SubStr]](cString, 1, 5)
cSubStr2 := [[SubStr]](cString, 6, 3)
cSubStr3 := [[SubStr]](cString, 4, 4)


cSubStr1 é igual a "Grupo"

cSubStr2 é igual a "GPS"

cSubStr3 é igual a "poGP"