#arquivo 


# Resumo:
Função que abre um arquivo para leitura em AdvPL, tem como parâmetro o caminho do arquivo e retorna o número de permanência (nHandle) caso o encontre, caso contrário retorna -1


# Exemplo:
local nHandle   := 0
local [cPath](Nota_caminho_hard-coded.md)        := "C:\\Teste\\Teste.txt" 

nHandle := [[ft_fUse]](cPath)

Caso encontre nHandle será igual ao número de permanência do arquivo.
Exemplo: nHandle = 1

Caso contrário nHandle = -1


# Obs:
O caminho do arquivo geralmente é inserido pelo usuário através do ParamBox tipo 6 [[Arquivo]].

É aconcelhavel/necessário utilizar o [[fClose]](nHandle) após o fim da utilização do arquivo, pois enquanto em execução o arquivo fica com status de "Em uso por smartclient"


# Uso:

# Exemplo:
local nHandle   := -1
local cLinha      := ""

nHandle := [[ft_fUse]](cArquivo)
if nHandle > 0
   while ! [[ft_fEOF]]()
	cLinha := [[FT_FReadLn]]()
	[[FT_FSkip]]()
   enddo
    [[FClose]](nHandle)
endif