#array 



# Resumo:
Preenche um [[Array]] com qualquer tipo de dado


Exemplo:
local aTeste  := [[Array]](10)  -  Array de 10 posições nulas

aFill(aTeste, "GPS")

Agora em cada uma das 10 posições do Array tem o valor "GPS" algo como:
{"GPS", "GPS", "GPS", "GPS", "GPS", "GPS", "GPS", "GPS", "GPS", "GPS"}


aFill(aTeste, 10, 5)

Agora passando o parâmetro 5, informa a partir de qual elemento o preenchimento deve acontecer, logo o Array agora ficou com o valor de:
{"GPS", "GPS", "GPS", "GPS", 10, 10, 10, 10, 10, 10}


aFill(aTeste, [.T.]('.T.'), 7, 2)


Agora com este outro parâmetro adicionado neste terceiro exemplo, informa a função além de qual elemento preencher, quantos elementos deve preencher, levando em consideração o último Array, agora o seu valor seria de:
{"GPS", "GPS", "GPS", "GPS", 10, 10, [.T.]('.T.'), [.T.]('.T.'), 10, 10}