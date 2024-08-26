#banco 


# Resumo: 
Função que retorna a area atual de uma tabela ou posição da tabela.

# Exemplo:
Caso a user function criada seja chamada no meio da execução de uma outra função, o [[GetArea]] junto ao [[RestArea]] garantem que os procedimentos não quebrem a lógica da  User Function que a chamou

# Uso:

User Function Exemplo()
  local aArea   := [[GetArea]]()
  local aSA1    := SA1->([[GetArea]]())

  <<Restante do código e da lógica da função exemplo>>

  [[RestArea]](aSA1)
  [[RestArea]](aArea)
Return nil