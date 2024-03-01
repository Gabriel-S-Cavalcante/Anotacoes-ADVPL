#InputBox 


# Resumo:
[[Checkbox]] comum porém com uma áres lateral adicional para texto (Say).

  [1]-Tipo 4 - Say + Checkbox
  [2]-Descricao
  [3]-Indicador logico contendo o inicial do check
  [4]-Texto do Check
  [5]-Tamanho do Radio
  [6]-Validacao
  [7]-Flag [.T.]('.T.')/[.F.]('.F.') Parametro Obrigatirio ?
  
  [[aAdd]](aPergs, {4, "Marca todos?", [.F.]('.F.'), "Marque todos se necessário.", 90, "", [.F.]('.F.')})


# Uso:
Local aPergs         := {}
Local aResps         := {}

[[aAdd]](aPergs, {4, "Tem certeza que deseja marcar?", [.F.]('.F.'), "Marcar", 90, "", [.F.]('.F.')})

Seus parâmetros de configuração devem ser passados dentro do [[array]] aPergs.
E as respostas virão no [[array]] aResps


If [[Parambox]](aPergs, "Say + Checkbox", @aResps)
   [[Alert]]("Usuário clicou no OK.")
Else
   [[Alert]]("Operação cancelada pelo usuário.")
EndIf



![[Pasted image 20240301104605.png]] 



