#InputBox 


# Resumo:
Input do tipo de caixa de seleção onde é passada por meio de um [[array]].
Seus parâmetros de uso são:

[1]-Tipo 2 - Combo
[2]-Descricao
[3]-Numerico contendo a opcao inicial do combo  
[4]-Array contendo as opceos do combo
[5]-Tamanho do combo
[6]-Validacao
[7]-Flag [.T.]('.T.')/[.F.]('.F.') Parametro obrigaório?

[[aAdd]](aPergs, {2, "Escolha uma opção", "1-Ruim", aOpcoes, 50, "", [.F.]('.F.')})


# Uso:
Local aPergs         := {}
Local aResps         := {}
Local aOpcoes      := {"1-Ruim", "2-Regular", "3-Bom", "4-Ótimo"}

Suas opções de escolha devem estar dentro de um [[array]] como o aOpcoes.
Seus parâmetros de configuração devem ser passados dentro do [[array]] aPergs.
E as respostas virão no [[array]] aResps


[[aAdd]](aPergs, {2, "Escolha uma opção", "1-Ruim", aOpcoes, 50, "", [.F.]('.F.')})

If [[Parambox]](aPergs, "Meu Input Box", @aResps)
   [[Alert]]("Usuário clicou no OK.")
Else
   [[Alert]]("Operação cancelada pelo usuário.")
EndIf


![[Pasted image 20240216103312.png]]


