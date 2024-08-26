#BlocoDeCodigo 



\#INCLUDE "Protheus.ch"

//--------------------------------------------------------------------
// {Protheus.doc} BlocoCod         
// Estudo bloco de código        
//                                               
// @author  Gabriel Cavalcante 
// @since 01/11/2023              
// @version 12/superior
//
//--------------------------------------------------------------------

[[User Function]] BlocoCod()

  Local cTeste    := "Teste de bloco1"
  Local nNum1     := 10
  Local nNum2     := 30
  Local nResult   := 0
  Local aNumeros  := {4,3}
  Local bBloco1   := {|| cTeste}
  Local bBloco2   := {|| nNum1 + nNum2}
  Local bBloco3   := {|cMsg| [[Alert]](cMsg)}
  Local bBloco4   := {|x,y| [[Alert]](cValToChar(x+y)), [[Alert]](cValToChar(x\*y)), [[Alert]](cValToChar(x/y))}
  Local bBloco5   := {|x,y| x < y}

Mostra na tela o resultado do bBloco1
  [[Alert]](Eval(bBloco1)) 
  
Armazena na variável o resultado gerado pela função bBloco2
  nResult := [[Eval]](bBloco2)

Executa os blocos de código passando os parâmetros
  [[Eval]](bBloco3, "Olá mundo!")
  [[Eval]](bBloco3, "Mensagem 2!")
  [[Eval]](bBloco4, 12,3)

Executa a função Teste3, passando um bloco de código que chama a função Teste2
  U_Teste3({|| U_Teste2()})

Executa a função Ordena passando o array e o bloco de código
  Ordena(aNumeros, bBloco5)

Return



[[User Function]] Teste2()

  [[Alert]]("Executando User Function TESTE2")

Return

[[User Function]] Teste3(bBLoco)

  [[Eval]](bBloco)

Return

[[Static Function]] Ordena(aNumeros, bBloco)

  Local nAux := 0


  If ! [[Eval]](bBloco, aNumeros\[1], aNumeros\[2])
    nAux := aNumeros\[1]
    aNumeros\[1] := aNumeros\[2]
    aNumeros\[2] := nAux
  EndIf

Return
