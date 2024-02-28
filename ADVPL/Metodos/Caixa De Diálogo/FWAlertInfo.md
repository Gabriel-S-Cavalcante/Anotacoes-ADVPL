#outputBox 



# Resumo:
Cria uma caixa de texto na tela do Usuário com o símbolo de Informação "!"

# Uso
FWAlertInfo(Texto ou variável com valor de texto, texto ou variável com o valor do título)


# Exemplo:


local cMsg    := ""
local cTitulo  := ""

cTitulo := "Dados Cadastrados:" + [[CRLF]]
cMsg   := "Nome: Fulano" + [[CRLF]]
cMsg  += "Cargo: xxxxx" + [[CRLF]]
cMsg  += "Nascimento: xx/xx/xxxx" + [[CRLF]]


FWAlertInfo(cMsg, cTitulo)

ou

FWAlertInfo("informações em String", "Dados Cadastrados:")



![[Pasted image 20240215115522.png]]