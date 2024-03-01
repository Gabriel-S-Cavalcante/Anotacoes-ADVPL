#InputBox 
#necessário-atualizar

# Resumo:



[1]-Tipo 6 - Arquivo
[2]-Descricao
[3]-String contendo 0 inicializador do campo
[4]-String contendo a Picture do campo
[5]-String contendo a validacao
[6]-String contendo a validacao when
[7]-Tamanho do MsGet
[8]-Flag [.T.]('.T.')/[.F.]('.F.') Parametro Obrigatirio ?
[9]-Texto contendo os tipos de arquivo, exemplo: "Arquivos .CSV |* .CSV"
[10]-Diretorio inicial do cGetFIle
[11]-Número relativo a visualização, podendo ser por diretório ou por arquivo (0,1,2,4,8,16,32,64,128)

[[aAdd]](aPergs, {6, "Informe o arquivo:", "", "", "", "", 80, [.F.]('.F.'), "Arquivo .CSV |* .CSV", "", GETF_LOCALHARD+GETF_NETWORKDRIVE})

# Uso:
Local aPergs         := {}
Local aResps         := {}

[[aAdd]](aPergs, {6, "Informe o arquivo:", "", "", "", "", 80, [.F.]('.F.'), "Arquivo .xlsx |* .xlsx", "", GETF_LOCALHARD+GETF_NETWORKDRIVE})

Seus parâmetros de configuração devem ser passados dentro do [[array]] aPergs.
E as respostas virão no [[array]] aResps


If [[Parambox]](aPergs, "Arquivo", @aResps)
   [[Alert]]("Usuário clicou no OK.")
Else
   [[Alert]]("Operação cancelada pelo usuário.")
EndIf


![[Pasted image 20240301110244.png]] 



