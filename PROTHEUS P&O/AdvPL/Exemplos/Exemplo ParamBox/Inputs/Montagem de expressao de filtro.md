#InputBox 


# Resumo:
Abre uma tela para montar e editar filtro


[1]-Tipo 7 - Montagem de expressao de filtro
[2]-Descricao
[3]-Alias da tabela
[4]-Filtro inicial

[[aAdd]](aPergs, {7, "Monte o filtro", "SXS", "X5_FILIAL\==xFilial('SXS')"}) 

# Uso:
Local aPergs         := {}
Local aResps         := {}

[[aAdd]](aPergs, {7, "Monte o filtro", "SA6", "A6_FILIAL\==xFilial('SA6')"}) 

If [[Parambox]](aPergs, "Monstagem de expressao de filtro", @aResps)
   [[Alert]]("Usuário clicou no OK.")
Else
   [[Alert]]("Operação cancelada pelo usuário.")
EndIf


![[Pasted image 20240301113252.png]] 















