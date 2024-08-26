#InputBox 


# Resumo:
MsGet do tipo password onde a senha é trocada no input por \****

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


# Uso:
Local aPergs         := {}
Local aResps         := {}

[[aAdd]](aPergs, {8, "Digite a senha", [[Space]](15), "", "", "", "", 80, [.F.]('.F.')})


  If [[Parambox]](aPergs, "MsGet password", @aResps)
    [[Alert]]("Usuário clicou no OK.")
  Else
    [[Alert]]("Operação cancelada pelo usuário.")
  EndIf


![[Pasted image 20240301113657.png]] 




