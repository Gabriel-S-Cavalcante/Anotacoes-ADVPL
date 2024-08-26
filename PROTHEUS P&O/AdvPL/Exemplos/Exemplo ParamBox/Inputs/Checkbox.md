#InputBox 


# Resumo:
Area com um checkbox convencional dando a opção de marcar ou não.

  [1]-Tipo 5 - Somente Checkbox
  [2]-Descricao
  [3]-Indicador logico contendo o inicial do check
  [4]-Texto do Check
  [5]-Tamanho do Radio
  [6]-Validacao
  [7]-Flag [.T.]('.T.')/[.F.]('.F.') Parametro Obrigatirio ?
  
  [[aAdd]](aPergs, {5, "Marca todos?", [.F.]('.F.'), 50, "", [.F.]('.F.')})


# Uso:
Local aPergs         := {}
Local aResps         := {}

[[aAdd]](aPergs, {5, "Salvar dados", [.F.]('.F.'), 50, "", [.F.]('.F.')})

Seus parâmetros de configuração devem ser passados dentro do [[array]] aPergs.
E as respostas virão no [[array]] aResps


If [[Parambox]](aPergs, "Somente Checkbox", @aResps)
  [[Alert]]("Usuário clicou no OK.")
Else
  [[Alert]]("Operação cancelada pelo usuário.")
EndIf


![[Pasted image 20240301105304.png]] 
