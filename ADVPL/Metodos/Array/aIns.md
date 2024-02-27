#array 


# Resumo:
Insere um elemento [Nulo](nil) no Array em determinada posição e empurra as posteriores para frente mas nao modifica o tamanho máximo do [[Array]]



Exemplo:
local aTeste  := {9, 12, 16, 20, 08, 96}

aIns(aTeste, 3)

Agora o valor de aTeste é de:
{9, 12, [[nil]], 16, 20, 08}

aIns(aTeste, 1)

Agora o valor de aTeste é de:
{[[nil]], 9, 12, [[nil]], 16, 20}

aIns(aTeste, 2)

Agora o valor de aTeste é de:
{[[nil]], [[nil]], 9, 12, [[nil]], 16}