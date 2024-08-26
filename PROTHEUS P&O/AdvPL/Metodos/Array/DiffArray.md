#array 



# Resumo:
Função que verifica se existe diferença entre 2 Arrays e retorna um booleano


# Syntaxe:

[[DiffArray]](a[[Array]]\_1, a[[Array]]\_2)

# Exemplo:

local a[[Array]]\_1 := {1, 2, 3, 4, 5}
local a[[Array]]\_2 := {1, 2, 3, 4, 5}

If [[DiffArray]](a[[Array]]\_1, a[[Array]]\_2)
	[[Alert]]("Existe diferença entre os Arrays)
Else
	[[Alert]]("Não existe diferença entre os Arrays)
EndIf