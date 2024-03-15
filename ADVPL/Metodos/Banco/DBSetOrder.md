#banco 


# Resumo:
Ordena a tabela aberta no fonte de acordo com o índice passado por parâmetro:

# Uso:

[[DBSetOrder]](índice)

Para descobrir o índice mais adequado é recomendado usar a query no banco 

SELECT
	*
FROM [[SIX]]990
WHERE INDICE = 'TABELA'



# Exemplo:
SELECT
	*
FROM [[SIX]]990
WHERE INDICE = 'SA1'

![[Pasted image 20240307110304.png]]

SA1->([[DBSetOrder]](1)) 
Seguindo a tabela [[SIX]] o INDICE 1 irá ordernar a Tabela por código e loja.