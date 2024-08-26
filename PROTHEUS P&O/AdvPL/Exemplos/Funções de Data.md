#data 



\#INCLUDE "Protheus.ch"

//--------------------------------------------------------------------
// {Protheus.doc} Datas
// Exemplo de função de usuário em ADVPL
//
// @author  Gabriel Cavalcante
// @since 01/11/2023
// @version 12/superior
//
//--------------------------------------------------------------------
  

[[User Function]] Datas()
 
  Local dDataAtual  := [[Date]]()
  Local cHora       := [[Time]]()
  Local cData       := ""
  Local nDiasAcres  := 0
  Local dDataRes    := [[SToD]]("")
  Local nResp       := 0
  Local cResp       := ""

  

  cHora := [[Time]]()

  cData := [[DToC]](dDataAtual)

  dDataRes := [[CToD]]("31/12/2023")

  cData := [[DToS]](dDataAtual)

  dDataRes := [[SToD]]("20231101")

  dDataRes := [[DataValida]]([[CToD]]("31/12/2022"), .T.)

  dDataRes := [[DataValida]]([[CToD]]("31/12/2022"), .F.) 

  nResp := [[Day]](dDataAtual)

  nResp := [[Month]](dDataAtual)

  nResp := [[Year]](dDataAtual)

  cResp := [[MesExtenso]](dDataAtual)

  cResp := [[AnoMes]](dDataAtual)

  cResp := [[MesDia]](dDataAtual)

  cResp := [[Day2Str]](dDataAtual)

  cResp := [[Month2Str]](dDataAtual)

  cResp := [[Year2Str]](dDataAtual)

  

  // Adicionar ou reduzir dias à uma data

  nDiasAcres := 15

  dDataRes := dDataAtual + nDiasAcres

  dDataRes := dDataAtual - nDiasAcres

  dDataRes := [[DaySum]](dDataAtual, nDiasAcres)

  dDataRes := [[DaySub]](dDataAtual, nDiasAcres)

  

  // Adicionar ou reduzir meses de uma data

  dDataRes := [[MonthSum]](dDataAtual, 3)

  dDataRes := [[MonthSub]](dDataAtual, 3)

  

  // Adicionar ou reduzir anos de uma data

  dDataRes := [[YearSum]](dDataAtual, 3)

  dDataRes := [[YearSub]](dDataAtual, 3)

  

  // Diferença entre Dias, Meses ou Anos entre duas datas

  nRes := [[DateDiffDay]](CToD("01/02/2023"), Date())

  nRes := [[DateDiffMonth]](CToD("01/02/2023"), Date())

  nRes := [[DateDiffYear]](CToD("01/02/2020"), Date())

  

  // Retorna o número do dia da semana

  nResp := [[Dow]](dDataAtual)

  

  // Descrição do dia de semana

  cResp := [[DiaSemana]](dDataAtual)

  

  // Retorna a primeira data ou a ultima data do mes recorrente

  dDataRes := [[FirstDate]](dDataAtual)

  dDataRes := [[LastDate]](dDataAtual)

  

  // Retorna o número do último dia do mês

  nResp := [[Last_Day]](dDataAtual)

  

  // Retorna o primeiro ou último dia do ano de uma data

  dDataRes := [[FirstYDate]](dDataAtual)

  dDataRes := [[LastYDate]](dDataAtual)

  

RETURN