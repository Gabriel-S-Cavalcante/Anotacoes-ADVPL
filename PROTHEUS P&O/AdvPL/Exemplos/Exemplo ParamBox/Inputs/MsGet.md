#InputBox 


# Resumo:
Input do tipo get convencional podendo ter 3 tipo, tipo caracter, tipo numérico e tipo data.
Seus parâmetros de uso são:

[1]-Tipo 1 - MsGet
[2]-Descrição
[3]-String contendo o inicializador do campo
[4]-String contendo a Picture do campo
[5]-String contendo a validacao
[6]-Consulta F3
[7]-String contendo a validacao when
[8]-Tamanho do MsGet
[9]-Flag [.T.]('.T.')/[.F.]('.F.') Parametro obrigatório?

Tipo caracter
[[aAdd]](aPergs, {1, "Produto", [[Space]](15), "@!", "ExistCpo('SB1', mv_part01)", "SB1", "", 0, [.T.]('.T.')})

Tipo numérico
[[aAdd]](aPergs, {1, "Valor", 0, "@E 9.999,99", "mv_par02>0", "", "", 20, [.F.]('.F.')})

Tipo data
[[aAdd]](aPergs, {1, "Data", [[SToD]](""), "", "", "", "", 50, [.T.]('.T.')})


# Uso:
Local aPergs         := {}
Local aResps         := {}

Seus parâmetros devem ser passados dentro do [[array]] aPergs
E as respostas virão no [[array]] aResps

[[aAdd]](aPergs, {1, "Produto", [[Space]](15), "@!", "ExistCpo('SB1', mv_part01)", "SB1", "", 0, [.T.]('.T.')})
[[aAdd]](aPergs, {1, "Valor", 0, "@E 9.999,99", "mv_par02>0", "", "", 20, [.F.]('.F.')})
[[aAdd]](aPergs, {1, "Data", [[SToD]](""), "", "", "", "", 50, [.T.]('.T.')})

If [[Parambox]](aPergs, "Meu Input Box", @aResps)
   [[Alert]]("Usuário clicou no OK.")
Else
   [[Alert]]("Operação cancelada pelo usuário.")
EndIf


![[Pasted image 20240216101707.png]]





