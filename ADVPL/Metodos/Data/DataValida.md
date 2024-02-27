#data 



# Resumo:
Retorna uma data sem considerar final de semana e feriado.


# Explicação:
Função que retorna uma data válida, a partir de uma data qualquer informada

Sintaxe: DataValida(dData, lTipo)

Onde:  
dData: Data que deseja validar  
lTipo: Se .T. posterga a data recebida para o próximo dia útil, se .F. retrocede a data recebida para o dia útil anterior.

# Exemplo:

Reclock("SF6", .F.)
SF6->F6_DTVENC  := DataValida(dDataBase,.T.)
SF6->F6_DTPAGTO := DataValida(dDataBase,.T.)
IF SE2->(DbSeek(xFilial("SE2") + SF6->F6_NUMERO))
	IF SA2->(DbSeek(xFilial("SA2") + SE2->E2_FORNECE + SE2->E2_LOJA))
		SF6->F6_BANCO 	:= SA2->A2_BANCO
		SF6->F6_AGENCIA := SA2->A2_AGENCIA
	ENDIF
ENDIF
SF6->(MsUnlock())



[Site fonte](https://www.blogadvpl.com/glossario/datavalida/#page-content)


