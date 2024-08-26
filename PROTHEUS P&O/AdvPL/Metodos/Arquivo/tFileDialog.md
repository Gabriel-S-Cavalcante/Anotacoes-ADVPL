#Diretorio 



# Resumo:
Abre o explorador de arquivos para que o usuário selecione o diretório do arquivo.



# Exemplo:
  Local cArqDir  := tFileDialog("Planilha XML (*.xml) | Arquivos de texto (*.txt) | Arquivos com separação (*.csv)", "Seleção do Arquivo de candidatos.",, GetTempPath(), .F., GETF_MULTISELECT )


  cArqDir terá o valor em Texto do diretório do aquivo selecionado
  
  Planilha XML (\*.xml) - Criará a opção de selecionar apenas arquivos .xml
  Arquivos de texto (\*.txt) - Criará a opção de selecionar apenas arquivos .txt
  Arquivos com separação (\*.csv) - Criará a opção de selecionar apenas arquivos .csv






  