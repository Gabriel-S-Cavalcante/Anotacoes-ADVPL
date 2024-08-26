#banco #query 

# Resumo: 
executa uma query no Banco de Dados e retorna o cAlias da tabela resultante



  
# Exemplo:
cQuery   := "SELECT A6_AGENCIA, A6_NOME FROM "+[[RetSqlName]]("SA6")+" "
cQuery += "WHERE D_E_L_E_T_ = ' ' AND A6_COD='"+cCodigo+"'"

cAlias := [[MPSysOpenQuery]](cQuery) 

cNome    := [[allTrim]]((cAlias) -> A6_NOME) 
cAgengia := [[allTrim]]((cAlias) -> A6_AGENCIA)

