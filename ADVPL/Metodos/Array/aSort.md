#array




# Resumo:
Ordena os itens do [[array]]



# Syntaxe:

aSorte(aVetor, nInicio, nCont, bOrdem):
Parâmetros:
  + aVetor    , [[Array]]  , Indica o [[array]] que será ordenado
  + nInicio   , Numérico , Indica o primeiro elemento que será colocado em ordem (caso não seja informado será desde a posição 1)
  + nCont     , Numérico   , Indica a quantidade de elementos que serão ordenados a partir do nInicio (caso não seja informado será considerado o [[array]] inteiro)
  + bOrdem    , [[Anotacoes/Bloco de código/Bloco de código|Bloco de código]]   , [[Anotacoes/Bloco de código/Bloco de código|Bloco de código]] que realizará a ordenação

[[Array]] convencional:
	aSort(Variável do [[Array]])

[[Array]] Multidimencional (Matrizes):
	aSorte(Variável do [[Array]], , , Variável do [[Anotacoes/Bloco de código/Bloco de código|Bloco de código]] ou [[Anotacoes/Bloco de código/Bloco de código|Bloco de código]])


# Exemplo:

User Function Array:
	 local aDadosMono := {}

    aAdd(aDadosMono, "Daniel")
	aAdd(aDadosMono, "Atilio")
	aAdd(aDadosMono, "João")
	aAdd(aDadosMono, "Maria")
	aAdd(aDadosMono, "José")

	 aSort(aDadosMono)

aDadosMono agora possui o valor de {"Atilio", "Daniel", "João", "José", "Maria"}


User Function Matriz:
	local aDadosMult := {}

    aAdd(aDadosMult, {"0001", "Daniel",   23})
    aAdd(aDadosMult, {"0002", "Atilio",   33})
    aAdd(aDadosMult, {"0003", "João",     43})
    aAdd(aDadosMult, {"0004", "Maria",    53})
    aAdd(aDadosMult, {"0005", "José",     63})
    
Ordena o Array por Nome (Array multidimensional) - Crescente usa < e Decrescente usa >
	aSort(aDadosMult, , , {|x, y| x\[2] < y\[2]})


aDadosMono agora possui o valor de: 
{
{"0002", "Atilio", 33},
{"0001", "Daniel", 23},
{"0003", "João", 43},
{"0005", "José", 63},
{"0004", "Maria", 53}
}