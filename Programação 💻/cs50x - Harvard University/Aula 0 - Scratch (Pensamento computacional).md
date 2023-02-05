## Pensamento Computacional
- Essencialmente, a programação de computadores trata de pegar algumas entradas e criar algumas saídas - resolvendo assim um problema. O que acontece entre a entrada e a saída, o que poderíamos chamar de caixa preta, é o foco deste curso.
![cs50Week0Slide38.png](../_resources/cs50Week0Slide38.png)
- Por exemplo, podemos precisar de uma aula. Poderíamos usar um sistema chamado unário para contar, um dedo de cada vez. Os computadores hoje contam usando um sistema chamado binário . É do termo dígito binário que obtemos um termo familiar chamado bit . Um bit é um zero ou um.
- Os computadores só falam em termos de zeros e uns. Zeros representam desligado. Uns representam . Computadores são milhões, talvez bilhões, de transistores que estão sendo ligados e desligados.
- Se você imaginar usando uma lâmpada, uma única lâmpada só pode contar de zero a um.
- No entanto, se você tiver três lâmpadas, há mais opções disponíveis para você!
- Usando três lâmpadas, o seguinte poderia representar zero:
```
0 0 0
```
- Da mesma forma, o seguinte representaria um:
```
0 0 1
```
- Por essa lógica, poderíamos propor que o seguinte é igual a dois:
```
0 1 0 
```
- Estendendo ainda mais essa lógica, o seguinte representa três:
```
0 1 1
```
- Quatro apareceriam como:
```
1 0 0
```
- Poderíamos, de fato, usar apenas três lâmpadas para contar até sete!
```
1 1 1
```
- Como heurística, poderíamos imaginar que os seguintes valores representam cada lugar possível em nosso dígito binário :
```
4 2 1
```
- Os computadores usam 'base-2' para contar. Isso pode ser retratado da seguinte forma:
```
  2^2  2^1  2^0
  4    2    1
```
- Portanto, você poderia dizer que seriam necessários três bits (a casa do quatro, a casa do dois e a casa do um) para representar um número tão alto quanto sete.

Os computadores geralmente usam oito bits para representar um número. Por exemplo, `00000101` é o número 5 em *binário*.

## Texto
- Assim como os números são padrões binários de uns e zeros, as letras também são representadas usando uns e zeros!
- Como há uma sobreposição entre os uns e os zeros que representam números e letras, o padrão ASCII foi criado para mapear letras específicas para números específicos.
- Por exemplo, a carta Afoi decidida a mapear para o número 65.
- Se você recebeu uma mensagem de texto, o binário dessa mensagem pode representar os números 72, 73 e 33. Mapeando-os para ASCII, sua mensagem ficaria assim:
```
  H   I   !
  72  73  33
```
- Graças a Deus por padrões como ASCII que nos permitem concordar com esses valores!
- Aqui está um mapa expandido de valores ASCII:
![cs50Week0Slide93.png](../_resources/cs50Week0Slide93.png)
- Se desejar, você pode aprender mais sobre [ASCII](https://en.wikipedia.org/wiki/ASCII).

## emojis
- Com o passar do tempo, há cada vez mais maneiras de se comunicar via texto.
- Como não havia dígitos suficientes em binário para representar todos os vários caracteres que poderiam ser representados por humanos, o padrão Unicode ampliou o número de bits que podem ser transmitidos e compreendidos pelos computadores.
- Existem emojis que você provavelmente usa todos os dias. O seguinte pode parecer familiar para você:
![cs50Week0Slide103.png](../_resources/cs50Week0Slide103.png)
- Os cientistas da computação enfrentaram um desafio ao querer atribuir vários tons de pele a cada emoji para permitir que a comunicação fosse ainda mais personalizada. Nesse caso, os criadores e colaboradores dos emojis decidiram que os bits iniciais seriam a estrutura do próprio emoji, seguida do tom de pele.
- Mais e mais recursos estão sendo adicionados ao padrão Unicode para representar outros caracteres e emojis.
- Se desejar, você pode aprender mais sobre [Unicode](https://en.wikipedia.org/wiki/Unicode) .
- Se desejar, você pode aprender mais sobre [emojis](https://en.wikipedia.org/wiki/Emoji) .

## RGB
- Vermelho, verde e azul (chamado RGB) é uma combinação de três números.
![cs50Week0Slide118.png](../_resources/cs50Week0Slide118.png)
- Pegar nossos 72, 73 e 33 usados ​​anteriormente, que diziam HI!via texto, seria interpretado pelos leitores de imagens como um tom claro de amarelo. O valor vermelho seria 72, o valor verde seria 73 e o azul seria 33.
![cs50Week0Slide120.png](../_resources/cs50Week0Slide120.png)

## Algoritmos
- A resolução de problemas é fundamental para a ciência da computação e programação de computadores.
- Imagine o problema básico de tentar localizar um único nome em uma lista telefônica.
- Como você pode fazer isso?
- Uma abordagem pode ser simplesmente ler da página um para a próxima até chegar à última página.
- Outra abordagem poderia ser pesquisar duas páginas por vez.
- Uma abordagem final e talvez melhor seria ir até o meio da lista telefônica e perguntar: “O nome que estou procurando está à esquerda ou à direita?” Em seguida, repita esse processo, cortando o problema ao meio e meio e meio.
- Cada uma dessas abordagens poderia ser chamada de algoritmos. A velocidade de cada um desses algoritmos pode ser retratada da seguinte maneira no que é chamado de *notação big-O* :
![cs50Week0Slide141.png](../_resources/cs50Week0Slide141.png)
Observe que o primeiro algoritmo, destacado em vermelho, tem um grande O `n` porque, se houver 100 nomes na lista telefônica, pode levar até 100 tentativas para encontrar o nome correto. O segundo algoritmo, em que duas páginas foram pesquisadas por vez, tem um grande O de **'n/2**' porque pesquisamos duas vezes mais rápido nas páginas. O algoritmo final tem um grande O de **log 2 n**, pois dobrar o problema resultaria apenas em mais uma etapa para resolvê-lo.

## Pseudocódigo e os blocos básicos de construção da programação
- A capacidade de criar *pseudocódigo* é fundamental para o sucesso de uma pessoa tanto nesta classe quanto na programação de computadores.
- Pseudocódigo é uma versão legível por humanos do seu código. Por exemplo, considerando o terceiro algoritmo acima, poderíamos compor o pseudocódigo da seguinte forma:
```
	1	Pick up phone book
  2  Open to middle of phone book
  3  Look at page
  4  If person is on page
  5      Call person
  6  Else if person is earlier in book
  7      Open to middle of left half of book
  8      Go back to line 3
  9  Else if person is later in book
  10     Open to middle of right half of book
  11     Go back to line 3
  12 Else
  13     Quit

```
- A pseudocodificação é uma habilidade tão importante por pelo menos dois motivos. Primeiro, quando você pseudocodifica antes de criar um código formal, isso permite que você pense na lógica do seu problema com antecedência. Em segundo lugar, quando você pseudocodifica, pode posteriormente fornecer essas informações a outras pessoas que buscam entender suas decisões de codificação e como seu código funciona.
- Observe que a linguagem em nosso pseudocódigo tem alguns recursos exclusivos. Primeiro, algumas dessas linhas começam com verbos como pegar, abrir, olhar. Posteriormente, chamaremos essas funções .
- Em segundo lugar, observe que algumas linhas incluem instruções como `if` ou `else if`.Essas são chamadas de condicionais .
- Terceiro, observe como existem expressões que podem ser declaradas como verdadeiras ou falsas, como “a pessoa está no início do livro”. Chamamos essas expressões booleanas de .
- Por fim, observe como essas declarações como “volte para a linha 3.” Chamamos esses loops .

Você pode continuar a leitura sobre Scratch em: https://cs50.harvard.edu/x/2023/notes/0/#scratch