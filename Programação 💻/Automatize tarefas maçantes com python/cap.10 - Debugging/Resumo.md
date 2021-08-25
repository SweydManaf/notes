Resumo

As **asserções**, as **exceções**, o **logging** e o **debugger** são ferramentas valiosas para encontrar e evitar bugs em seu programa.

As asserções com a instrução `assert` do Python são uma ótima maneira de implementar “**verificações de sanidade**” que avisarão com antecedência quando uma condição necessária não for verdadeira. As asserções servem somente para os erros dos quais o

programa não deverá tentar se recuperar e devem falhar rapidamente. Caso contrário, utilize uma exceção. Uma exceção pode ser capturada e tratada pelas instruções `try` e `except`.

O módulo `logging` é uma ótima maneira de olhar seu código enquanto ele estiver executando e é muito mais conveniente do que usar a função print() por causa dos seus diferentes níveis de logging e da capacidade de fazer log em um arquivo-texto.

O debugger permite executar seu programa passo a passo, uma linha de cada vez. De modo alternativo, seu programa poderá ser executado em velocidade normal e o debugger poderá fazer uma pausa na execução sempre que alcançar uma linha com um breakpoint definido. Ao usar o debugger, podemos ver o estado de qualquer variável em qualquer ponto do tempo de vida do programa. Essas ferramentas e técnicas de debugging ajudarão você a criar programas que funcionem. Introduzir bugs acidentalmente em seu código é um fato da vida, independentemente de quantos anos de experiência de codificação você

possa ter.