#InputBox 


# Resumo:
Tipo mensagem, apenas uma descrição na tela em Title case


[1]-Tipo 9 -> Somente uma mensagem, formato de um titulo
[2]-Texto descritivo 
[3]-Largura do Texto
[4]-Altura do Texto
[5]-Valor lógico sendo: [.T.]('.T.') => fonte tipo VERDANA e [.F.]('.F.') => fonte tipo ARIAL

[[aAdd]](aPergs, {9, "Texto aleatório, apenas demonstrativo", 150, 7, [.T.]('.T.')})


# Uso:
Local aPergs         := {}
Local aResps         := {}

[[aAdd]](aPergs, {9, "Texto aleatório, apenas demonstrativo", 150, 7, [.T.]('.T.')})

If [[Parambox]](aPergs, "Somente uma mensagem, formato de um titulo", @aResps)
   [[Alert]]("Usuário clicou no OK.")
Else
   [[Alert]]("Operação cancelada pelo usuário.")
EndIf



![[Pasted image 20240301114455.png]] 










