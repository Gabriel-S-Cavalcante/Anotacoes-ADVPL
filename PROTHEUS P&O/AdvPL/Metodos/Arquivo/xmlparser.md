#xml


# Resumo:
Lê um arquivo xml com base no diretório do arquivo e duas variáveis passadas com referência que retornarão Erros encontrados e Avisos sobre a leitura do arquivo



# Exemplo:
  Local cDiretorio    := [[tFileDialog]]() // Veja o arquivo para construir a funçao
  local cError           := "" 
  Local cWarning    := ""
  Local oNotaxml       
   
  oNotaxml := [[xmlparser]](MemoRead(cDiretorio), "", @cError, @cWarning)

  If cError != ""
    [[Alert]]("Erros: " + cError) 
  EndIf

  If cWarning != ""
    [[Alert]]("Avisos: " + cWarning)
  EndIf
