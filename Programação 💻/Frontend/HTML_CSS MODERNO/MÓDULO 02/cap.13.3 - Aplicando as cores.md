# Aplicando cores no site

Existem vários sites e serviços que vão te ajudar na escolha da paleta de cores do seu site. A que vai permitir mais opções, na minha opinião é o Adobe Color (disponível em [color.adobe.com](https://color.adobe.com/pt/)), que tem recursos gratuitos para te auxiliar na escolha das suas cores baseado nos esquemas de harmonia que vimos anteriormente.

Você já deve ter ouvido falar que as cores em uma tela são compostas da junção de três cores primárias: vermelho (**red**), verde (**green**) e azul (**blue**). Se usarmos todas as cores primárias no máximo, chegamos ao branco. Com todas as três no mínimo, obtemos o preto.

Cada cor primária pode ter um valor entre 0 e 255, totalizando 256 possibilidades para cada elemento.

Esta mesma cor indicada acima, pode ser representada em CSS com um outro formato baseado na maneira como o olho humano enxerga as cores: o padrão **HSL**. A função `hsl(179, 100%, 34%)` indica que temos 179 de **hue** (matiz), 100% de **saturation** (saturação) e 34% de **lightness** (luminância).

## Usando gradientes em CSS

Podemos gerar gradientes e aplicarmos a componentes visuais

usando folhas de estilo. Vamos usar um exemplo simples:

```html
<style>
    body{
        font-family: Arial, Helvetica, sans-serif;
        background-image: linear-gradient(90deg, yellow, red);
        color: black;
        }
</style>
```

A função **linear-gradient** é auto-explicativa e gera um gradiente linear angular. O primeiro parâmetro da função, indica o ângulo de inclinação de 90 graus (**90deg**) e as seguintes indicam as cores do degradê a ser criado. Você pode indicar quantas cores quiser e o navegador vai saber se virar pra gerar seu degradê personalizado.

Também é possível gerar os chamados gradientes radiais, que também são meio autoexplicativos. Veja o exemplo:

```html
<style>
    body{
        background-image: radial-gradient(circle, red, yellow, green);
    }
</style>
```

Você também pode personalizar ainda mais seu degradê colocando uma porcentagem ao lado da cor como **red 10%**, **yellow 40%**, **green 50%**.