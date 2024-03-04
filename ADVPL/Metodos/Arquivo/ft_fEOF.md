#arquivo 



# Resumo:
EOF de End Of File, retorna um booleano que identifica se chegou ou não ao fim do arquivo aberto pelo [[ft_fUse]], geralmente usado como condiçao de um While junto a negação ( ! ) e a função [[ft_fSkip]] para iterar todas as linhas do arquivo aberto.


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