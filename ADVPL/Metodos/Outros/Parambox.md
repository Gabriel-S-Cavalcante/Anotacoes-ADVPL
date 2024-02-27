#InputBox


# Resumo:
Cria uma tela de perguntas com InputBox passadas por [[parametro]].


# Uso:
O método ParamBox pede 2 [Arrays](Array) obrigatórios, sendo o primeiro o que leva as configurações dos inputbox da tela de perguntas e o segundo que retornará com as respostas do usuário.

Parambox(
		Variável de [[Array]] com as definições de input,
		"Título da tela de perguntas",
		 @Variável do [[Array]] vazio das respostas passado de preferência por referência
		 )


O método pode ser usado dentro de uma sentença IF, pois caso seja executada corretamente retornará um valor verdadeiro e caso seja cancelada ou fechada retornará um valor falso.

  If Parambox(aPergs, "Meu Input Box", @aResps)
    [[Alert]]("Usuário clicou no OK.")
  Else
    [[Alert]]("Operação cancelada pelo usuário.")
  EndIf

Existem mais parâmetros que podem ser passados ao ParamBox para uma maior flexibilidade de casos de uso.
Parâmetros da função Parambox()
-------------------------------
01 - < aParametros > - Vetor com as configurações 
02 - < cTitle >      - Titulo da Janela
03 - < aRet >        - Vetor passador por referência que contém o retorno dos parâmetros
04 - < bOk >         - Code Block para validar o Botão OK
05 - < aButtons >    - Vetor com mais botões além dos botões de Ok e Cancel
06 - < lCentered >   - Centralizar a janela
07 - < nPosX >       - Se não centralizar janela coordenada X para início
08 - < nPosY >       - Se não centralizar janela coordenada Y para início
09 - < oDlgWizard >  - Utiliza o objeto da janela ativa
10 - < cLoad >       - Nome do perfil se caso for carregar
11 - < lCanSave >    - Salvar os dados informados nos parâmetros por perfil
12 - < lUserSave >   - Configuração por usuário

Caso alguns parâmetros para a função não seja passada será cosiderado DEFAULT as seguintes abaixo:
DEFAULT bOK          := {|| (.T.)}
DEFAULT aButtons     := {}
DEFAULT lCentered    := .T.
DEFAULT nPosX        := 0
DEFAULT nPosY        := 0
DEFAULT cLoad        := ProcName(1)
DEFAULT lCanSave     := .T.
DEFAULT lUserSave    := .F.



# Exemplos:
Exemplos com explicação dos parâmetros do ParamBox em [[Exemplo ParamBox]].