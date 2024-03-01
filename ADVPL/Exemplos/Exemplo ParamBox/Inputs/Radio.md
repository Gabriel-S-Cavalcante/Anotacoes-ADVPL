#InputBox 


# Resumo:
Input do tipo Radio: Input box onde algumas opções aparecem em sequência e o usuário apenas pode escolher uma das opções 

  [1]-Tipo 3 - Rádio
  [2]-Descricao
  [3]-Numerico contendo a opcao inicial do Radio
  [4]-Array contendo as opções inciais do Radio
  [5]-Tamanho do Radio
  [6]-Validacao
  [7]-Flag [.T.]('.T.')/[.F.]('.F.') Parametro Obrigatirio ?


  [[aAdd]](aPergs, {3, "Mostrar deletados", 1, {"Sim", "Não"}, 50, "", [.F.]('.F.')})


# Uso:
 Local aPergs         := {}
 Local aResps         := {}

As opções que apareceção no Rádio devem estar dentro de um [[array]].
Seus parâmetros de configuração devem ser passados dentro do [[array]] aPergs.
E as respostas virão no [[array]] aResps

[[aAdd]](aPergs, {3, "Mostrar deletados", 1, {"Sim", "Não"}, 50, "", [.F.]('.F.')})


  If [[Parambox]](aPergs, "Rádio", @aResps)
    [[Alert]]("Usuário clicou no OK.")
  Else
    [[Alert]]("Operação cancelada pelo usuário.")
  EndIf


![[Pasted image 20240301101450.png]]   






