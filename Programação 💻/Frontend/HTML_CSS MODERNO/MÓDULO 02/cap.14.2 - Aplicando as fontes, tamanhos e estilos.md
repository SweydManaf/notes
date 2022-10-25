---
title: cap.14.2 - Aplicando as fontes, tamanhos e estilos
updated: 2021-06-04 19:28:38Z
created: 2021-04-19 17:10:46Z
---

# Como aplicar isso na prática?

Para configurar a família tipográfica que será aplicada a um determinado texto, usamos a propriedade `font-family` das CSS. Se indicarmos mais de uma família na sequência, estamos indicando ao navegador que dê preferência para a primeira. Caso ela não seja encontrada, tente a próxima. E essa estratégia se seguirá até a última, que geralmente é a família genérica **serif**, **sans-serif** ou **monospaced**.

```html
<style>
    body{
        font-family: Arial, Helvetica, sans-serif;
        color: black;
    }
    h1{
        font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
        color: rgb(24, 97, 126);
    }
    h2{
        font-family: 'Times New Roman', Times, serif;
        color: rgb(33, 136, 161);
    }
    p{
        font-family: 'Courier New', Courier, monospace;
    }
</style>
```

# Unidades de medida

Para especificar tamanho de fontes, existem várias medidas como **cm** (centímetros), **in** (polegadas), **pt** (pontos), **pc** (paicas), **px** (pixels), etc.

Para tamanhos de fonte a serem exibidos na tela, o W3C recomenda o uso do **px** ou do **em**.

# Shorthand

As formatações de fontes são tão importantes e tão usadas em CSS, que existem “atalhos” para usá-las. São as chamadas **shorthands**. Existe uma shorthand para fontes que é a propriedade `font`. No lugar de fazer várias configurações em múltiplas linhas, podemos simplificar tudo de maneira muito simples.

Por exemplo, no lugar de configurar o estilo dos parágrafos do nosso site desse jeito:

```css
p{
        font-family: Arial, Helvetica, sans-serif;
        font-size: 1em;
        font-style: italic;
        font-weight: bold;	
}
 /* Usando shorthand */
 
 p{
 	font: italic bold 1em Arial, Helvetica, sans-serif;
 }
```

A ordem dos atributos de uma *shorthand é importante. No caso da propriedade `font`, devemos* informar na ordem: 

- font-style
- font-variante
- font-weight
- font-size/line-height
- font-family