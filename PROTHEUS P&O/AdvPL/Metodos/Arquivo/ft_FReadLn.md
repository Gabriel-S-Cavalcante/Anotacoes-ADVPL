#arquivo 


# Resumo:
Função que lê a linha atual do arquivo que foi aberta pela função [[ft_fUse]].
Para ler uma próxima linha é nessário utilizar (geralmente no fim de um while) a função [[ft_fSkip]]


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