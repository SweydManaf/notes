# Bem-vindo
- Lembre-se de que as máquinas só entendem binário. Onde os humanos escrevem o código-fonte , uma lista de instruções para o computador legível por humanos, as máquinas só entendem o que podemos chamar de código de máquina . Este código de máquina é um padrão de uns e zeros que produz um efeito desejado.
- Acontece que podemos converter o código - fonte `machine code` usando um software muito especial chamado `compilador` . Hoje, apresentaremos a você um compilador que permitirá converter código-fonte na linguagem de programação C em código de máquina.
- Hoje, além de aprender como codificar, você aprenderá como escrever um bom código.
- O código pode ser avaliado em três eixos. Primeiro, a **correção** refere-se a “o código é executado como pretendido?” Em segundo lugar, o **design** refere-se a “quão bem o código foi projetado?” Finalmente, **estilo** refere-se a “quão esteticamente agradável e consistente é o código?”

## Hello World
```
#include <stdio.h>

int main(void)
{
    printf("hello, world\n");
}
```

## Variáveis
```
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    string answer = get_string("What's your name? ");
    printf("hello, %s\n", answer);
}
```
## Condições
```
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    // Prompt user to agree
    char c = get_char("Do you agree? ");

    // Check whether agreed
    if (c == 'Y' || c == 'y')
    {
        printf("Agreed.\n");
    }
    else if (c == 'N' || c == 'n')
    {
        printf("Not agreed.\n");
    }
}
```
Observe que as aspas simples são utilizadas para caracteres simples. Além disso, observe que `==` garante que algo seja igual a outra coisa, onde um único sinal de igual teria uma função muito diferente em C. Finalmente, observe que `||` efetivamente significa **ou**.

## Loops
### while
```
#include <stdio.h>

int main(void)
{
    int i = 0;
    while (i < 3)
    {
        printf("meow\n");
        i++;
    }
}
```
### for
```
#include <stdio.h>

int main(void)
{
    for (int i = 0; i < 3; i++)
    {
        printf("meow\n");
    }
}
```
Observe que o **for loop** inclui três argumentos. O primeiro argumento `int i = 0` inicia nosso contador em zero. O segundo argumento `i < 3` é a condição que está sendo verificada. Por fim, o argumento `i++` diz ao loop para incrementar em um cada vez que o loop é executado.

## Linux e a linha de comando
- Alguns argumentos comuns de linha de comando que podemos usar incluem:
	- cd, para alterar nosso diretório atual (pasta)
	- cp, para copiar arquivos e diretórios
	- ls, para listar arquivos em um diretório
	- mkdir, para fazer um diretório
	- mv, para mover (renomear) arquivos e diretórios
	- rm, para remover (excluir) arquivos
	- rmdir, para remover (excluir) diretórios

## Abstração
- Abstração é a arte de simplificar nosso código de forma que ele lide com problemas cada vez menores.
```
#include <cs50.h>
#include <stdio.h>

int get_size(void);
void print_grid(int n);

int main(void)
{
    int n = get_size();
    print_grid(n);
}

int get_size(void)
{
    int n;
    do
    {
        n = get_int("Size: ");
    }
    while (n < 1);
    return n;
}

void print_grid(int n)
{
    for (int i = 0; i < n; i++)
    {
        for (int j = 0; j < n; j++)
        {
            printf("#");
        }
        printf("\n");
    }
}
```
Observe que temos três funções agora. Primeiro, temos a `main` função que chama duas outras funções chamadas `get_size` e `print_grid`. Em segundo lugar, temos uma segunda função chamada `get_size` que inclui o código exato que tínhamos para realizar esta tarefa anterior. Terceiro, temos outra função chamada `print_grid` que imprime a grade. Como abstraímos os problemas essenciais de nosso programa, nossa `main` função é muito curta.

## Operadores e Tipos
- Os operadores referem-se às operações matemáticas que são suportadas pelo seu compilador. Em C, esses operadores matemáticos incluem:
	- \+ para adição
	- \- para subtração
	- \* para multiplicação
	- / para divisão
	- % para resto
- Tipos referem-se aos possíveis dados que podem ser armazenados dentro de uma variável. Por exemplo, o char é projetado para acomodar um único caractere como **a** ou **2**.
- Os tipos são muito importantes porque cada tipo tem limites específicos. Por exemplo, devido aos limites da memória, o valor mais alto de `int` intpode ser **4294967296**.
- Os tipos com os quais você pode interagir durante este curso incluem:
	- `bool`, uma expressão booleana de true ou false
	- `char`, um único caractere como a ou 2
	- `double`, um valor de ponto flutuante com mais dígitos que um float
	- `float`, um valor de ponto flutuante ou número real com um valor decimal
	- `int`, inteiros até um determinado tamanho ou número de bits
	- `long`, inteiros com mais bits, para que possam contar mais do que um int
	- `string`, uma cadeia de caracteres