#arquivo 


# Resumo:
Escreve o conteúdo de um arquivo com base no valor nHandle do arquivo e o conteúdo a ser adicionado, ambos passados por parâmetro


# Exemplo:
local cDir            := "C:\\Teste\\Teste.txt"
local nHandle     := -1
local cConteudo := "Hello, World! I love AdvPL!"

nHandle := [[fCreate]](cDir)
[[fWrite]](nHandle, cConteudo)
[[fClose]](nHandler)