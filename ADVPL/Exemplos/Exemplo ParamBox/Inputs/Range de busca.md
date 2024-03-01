#InputBox 
#necessário-atualizar 

# Resumo:
Função que retorna o range de busca inserido pelo usuário

[1]-Tipo 10 -> Range de busca
[2]-Titulo
[3]-Inicializador padrao
[4]-Consulta F3
[5]-Tamanho do GET
[6]-Tipo de Dado, Somente (C=Caractere e D=Data)
[7]-Tamanho do espaço 
[8]-Condição When
[[aAdd]](aPergs, {10, "Bancos", [[Space]](12), "SA6", 40, "C", 12, "[.T.]('.T.')"})


# Uso:
Local aPergs         := {}
Local aResps         := {}

[[aAdd]](aPergs, {10, "Bancos", [[Space]](3), "SA6", 40, "C", 3, "[.T.]('.T.')"})

If [[Parambox]](aPergs, "Range de busca", @aResps)
   [[Alert]]("Usuário clicou no OK.")
Else
   [[Alert]]("Operação cancelada pelo usuário.")
EndIf

Returno no aResps\[1]  é = "004..197;"



![[Pasted image 20240301120908.png]] 