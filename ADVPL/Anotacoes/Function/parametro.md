#função


# Resumo:
Variável genérica de uma função que é definida entre as () em sua declaração e passada também entre os () em sua chamada, pode ou nao ser obrigatória por poder ter ou nao um valor padrão.

Caso seja passada uma variável a uma funçao, deve-se de preferência passa-la por referência visando a otimização do uso de memória ao se utlizar o fonte que contenha a função.


# Obs:
Para passar uma variável por referência deve-se usar @ antes da propria variável.

Exemplo:

[[user Function]] Ex001()
	local nResult := 0
	local nNum1 := 2
	local nNum2 := 3

	if u_soma(nNum1, nNum2, @nResult)
		Alert("O valor da soma é: " + cValToChat(nResult) + ".")
	endif
return


Caso nResult não tivesse sido passado por referência, o mesmo não sofreria alterações pela função soma() fazendo com que o resultado fosse 0 ao invés de 5.