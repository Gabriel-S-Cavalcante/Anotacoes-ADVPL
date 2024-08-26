


# Resumo:
Função de iteração que se baseia em uma variável de controle (geralmente declarada como nI) e declaração de quando finalizar o for.

E por fim pra fechar a declaração do for apenas colocar um Next (Como boas práticas em AdvPL é comum que se passe à frente do Next a variável de controle do for para sua identificação mais clara e rápida)


# Exemplo:

Vamos usar como exemplo um for que soma os números de um array

local nI           :=  0
local aNums   := {1, 2, 3, 4, 5}
local nSoma   := 0

[[For]] nI:=1 to [[len]](aNums)
	nSoma += aNums\[nI] 
Next nI


