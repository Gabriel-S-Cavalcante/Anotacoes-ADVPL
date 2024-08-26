#arquivo


# Resumo:
Função que fecha o arquivo que foi aberto pela função [[ft_fUse]] para que seja liberado após utilização do fonte

Seu parâmetro é o próprio nHandle retornado pela função ft_fUse



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