#arquivo #InputBox

# Resumo:
Arquivo no SIGACFG que cria uma tabela/grupo de perguntas

# Uso:
A ordem que aparece na tabela deve estar na mesma ordem que é desejado que apareça na tela do usuário.

Seguindo essa lógica o sistema cria 60 variáveis públicas (mv_parXX) durante a execução da tabela através do método [[Pergunte]].

As respostas serão gravadas da seguinte maneira:

Resposta da pergunta 1    ->   mv_par01
Resposta da pergunta 2    ->   mv_par02
Resposta da pergunta 3    ->   mv_par03
...
Resposta da pergunta 58  ->   mv_par58
Resposta da pergunta 59  ->   mv_par59  
Resposta da pergunta 60  ->   mv_par60  

# Obs:
Sempre que for criar um grupo de perguntas SX1, inicie o nome do grupo com X para evitar conflitos presentes e futuros com o sistema do Protheus.












