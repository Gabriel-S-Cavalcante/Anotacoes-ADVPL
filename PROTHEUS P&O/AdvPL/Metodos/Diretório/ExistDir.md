#Diretorio


# Resumo:
Função que verifica se o diretório passado por parâmetro para a função existe, caso exista, retorna True caso não exista retorna False


# Exemplo:

local [cCaminho](Nota_caminho_hard-coded.md)  := "C:\\Protheus\\AdvPL\\"
local nCaminho  := -1

if ! [[ExistDir]](cCaminho)
	nCaminho := [[MakeDir]](cCaminho)
	if nCaminho != 0
		[[Alert]]("Não foi possível criar o diretório.")
	endif
endif