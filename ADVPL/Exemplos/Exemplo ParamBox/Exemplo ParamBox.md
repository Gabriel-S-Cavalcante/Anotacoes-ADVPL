#InputBox 

 Local aPergs         := {}
 Local aResps         := {}
 Local aOpcoes      := {"1-Ruim", "2-Regular", "3-Bom", "4-Ótimo"}
Input tipo 1 - MsGet
------------------------------------
Input do tipo [[MsGet]] pode ter 3 tipos, tipo caracter, tipo numérico e tipo data.

Input tipo 2 - Combo Box
---------------------------------------------
Input do tipo [[Combo Box]], um input do tipo de caixa de seleção entre opções. 

Input tipo 3 - Radio
-----------------------------------
Input do tipo Radio.
  [1]-Tipo 3 - Rádio
  [2]-Descricao
  [3]-Numerico contendo a opcao inicial do Radio
  [4]-Array contendo as opções inciais do Radio
  [5]-Tamanho do Radio
  [6]-Validacao
  [7]-Flag [.T.]('.T.')/[.F.]('.F.') Parametro Obrigatirio ?
  [[aAdd]](aPergs, {3, "Mostrar deletados", 1, {"Sim", "Não"}, 50, "", [.F.]('.F.')})

  [1]-Tipo 4 - Say + Checkbox
  [2]-Descricao
  [3]-Indicador logico contendo o inicial do check
  [4]-Texto do Check
  [5]-Tamanho do Radio
  [6]-Validacao
  [7]-Flag [.T.]('.T.')/[.F.]('.F.') Parametro Obrigatirio ?
  [[aAdd]](aPergs, {4, "Marca todos?", [.F.]('.F.'), "Marque todos se necessário.", 90, "", [.F.]('.F.')})

  [1]-Tipo 5 - Somente Checkbox
  [2]-Descricao
  [3]-Indicador logico contendo o inicial do check
  [4]-Texto do Check
  [5]-Tamanho do Radio
  [6]-Validacao
  [7]-Flag [.T.]('.T.')/[.F.]('.F.') Parametro Obrigatirio ?
  [[aAdd]](aPergs, {5, "Marca todos?", [.F.]('.F.'), 50, "", [.F.]('.F.')})

  [1]-Tipo 6 - Arquivo
  [2]-Descricao
  [3]-String contendo 0 inicializador do campo
  [4]-String contendo a Picture do campo
  [5]-String contendo a validacao
  [6]-String contendo a validacao when
  [7]-Tamanho do MsGet
  [8]-Flag [.T.]('.T.')/[.F.]('.F.') Parametro Obrigatirio ?
  [9]-Texto contendo os tipos de arquivo, exemplo: "Arquivos .CSV |* .CSV"
  [10]-Diretorio inicial do cGetFIle
  [11]-Número relativo a visualização, podendo ser por diretório ou por arquivo (0,1,2,4,8,16,32,64,128)
  [[aAdd]](aPergs, {6, "Informe o arquivo:", "", "", "", "", 80, [.F.]('.F.'), "Arquivo .CSV |* .CSV", "", GETF_LOCALHARD+GETF_NETWORKDRIVE})

  [1]-Tipo 7 - Monstagem de expressao de filtro
  [2]-Descricao
  [3]-Alias da tabela
  [4]-Filtro inicial
  [[aAdd]](aPergs, {7, "Monte o filtro", "SXS", "X5_FILIAL\==xFilial('SXS')"})

  [1]-Tipo 8 - MsGet password
  [2]-Descricao
  [3]-String contendo 0 inicializador do campo
  [4]-String contendo a Picture do campo
  [5]-String contendo a validacao
  [6]-Consulta F3
  [7]-String contendo a validacao when
  [8]-Tamanho do MsGet
  [9]-Flag [.T.]('.T.')/[.F.]('.F.') Parametro Obrigatirio ?
  [[aAdd]](aPergs, {8, "Digite a senha", [[Space]](15), "", "", "", "", 80, [.F.]('.F.')})

  [1]-Tipo 9 -> Somente uma mensagem, formao de um titulo
  [2]-Texto descritivo 
  [3]-Largura do Texto
  [4]-Altura do Texto
  [5]-Valor lógico sendo: [.T.]('.T.') => fonte tipo VERDANA e [.F.]('.F.') => fonte tipo ARIAL
  [[aAdd]](aPergs, {9, "Texto aleatório, apenas demonstrativo", 150, 7, [.T.]('.T.')})

  [1]-Tipo 10 -> Range de busca
  [2]-Titulo
  [3]-Inicializador padrao
  [4]-Consulta F3
  [5]-Tamanho do GET
  [6]-Tipo de Dado, Somente (C=Caractere e D=Data)
  [7]-Tamanho do espaço 
  [8]-Condição When
  [[aAdd]](aPergs, {10, "Cliente", [[Space]](6), "SA1", 40, "C", 6, "[.T.]('.T.')"})

  [1]-Tipo 11 -> MultiGet (Memo)
  [2]-Descrição
  [3]-Inicializador padrão
  [4]-Validação
  [5]-When
  [6]-Campo com preenchimento obriatório [.T.]('.T.')=Sim [.F.]('.F.')=Não (Incluir validação na função ParamOK)
  [[aAdd]](aPergs, {11, "Informe o motivo", "", "[.T.]('.T.')", "[.T.]('.T.')", [.T.]('.T.')})

  If [[Parambox]](aPergs, "Meu Input Box", @aResps)
    [[Alert]]("Usuário clicou no OK.")
  Else
    [[Alert]]("Operação cancelada pelo usuário.")
  EndIf

Return
