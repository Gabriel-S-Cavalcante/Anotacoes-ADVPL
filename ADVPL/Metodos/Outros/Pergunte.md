#InputBox 



# Resumo:
Cria uma telinha de perguntas com base na tabela do arquivo [[SX1]] 

# Sintaxe:
Pergunte(
	"NomeDaTabelaSX1",
	 Variável booleana que define se as perguntas irão ou não aparecer para o usuário,
	 Cabeçalho da tela de perguntas
	 )

# Exemplo:
  if Pergunte("XGabriel", .T., "Minhas perguntas")
    [[Alert]]("Achou as perguntas e vai preencher as variáveis públicas MV_PARXX")
  Else
    [[Alert]]("NÃo localizou as perguntas no arquivo SX1 ou usuário clicou em cancelar")
  EndIf

