#InputBox 


# Resumo:
Campo de [[MsGet]] do tipo Caractere onde é possível resgatar textos maiores e com quebrade linha.

[1]-Tipo 11 -> MultiGet (Memo)
[2]-Descrição
[3]-Inicializador padrão
[4]-Validação
[5]-When
[6]-Campo com preenchimento obriatório [.T.]('.T.')=Sim [.F.]('.F.')=Não (Incluir validação na função ParamOK)
[[aAdd]](aPergs, {11, "Informe o motivo", "", "[.T.]('.T.')", "[.T.]('.T.')", [.T.]('.T.')})

# Uso:
Local aPergs         := {}
Local aResps         := {}

Seus parâmetros devem ser passados dentro do [[array]] aPergs
E as respostas virão no [[array]] aResps

[[aAdd]](aPergs, {11, "Informe o motivo", "", "[.T.]('.T.')", "[.T.]('.T.')", [.T.]('.T.')})

  If [[Parambox]](aPergs, "MultiGet (Memo)", @aResps)
    [[Alert]]("Usuário clicou no OK.")
  Else
    [[Alert]]("Operação cancelada pelo usuário.")
  EndIf


![[Pasted image 20240301121920.png]]  


