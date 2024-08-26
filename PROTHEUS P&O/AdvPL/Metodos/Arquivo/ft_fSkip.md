#arquivo 



# Resumo:
Geralmente utilizada no final de um laço de iteração While, essa função é responsável por pular para a próxima linha do arquivo atualmente aberto pelo [[ft_fUse]].


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