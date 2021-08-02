cap.16.1 - Modelo de caixas

Modelo de caixas

## O que é uma caixa?

De forma simples e objetiva, baseado em um conceito chamado “box model”, a grande maioria dos elementos **HTML** que temos no nosso site são como caixas. Elas são *containers* que armazenam conteúdos ou até mesmo outras caixas.

## Anatomia de uma caixa

<img src="../../../_resources/8315f446f303438f863c0aa2c2e3ed67.png" alt="anatomiaCaixa.png" width="371" height="208">

- conteúdo (**content**) \- conteúdo da caixa
- largura (**width**) e altura (**height**) -  e a esse conjunto de propriedades, damos o nome de **box-size** (tamanho da caixa)
- borda (**border**) \- 'linha' em volta da caixa ele pode ter espessura, cor e um formato.
- preenchimento (**padding**) \- situa-se entre a borda e o conteúdo.
- margem (**margin**) \- da borda para fora.

Entre a margem e a borda, podemos determinar o contorno (**outline**) que é muito pouco utilizado, mas existe. Ele é um traçado visual que podemos criar fora da borda e o cálculo da sua espessura faz parte da margem estabelecida.

## Tipos de caixa

Dependendo do comportamento da caixa, podemos classificar um elemento em uma de duas categorias:

### Caixa do tipo block-level

Um elemento dito block-level sempre vai se iniciar em uma nova linha e vai ocupar a largura total do elemento onde ele está contido. Se não estiver contido em nenhuma outra caixa, ele vai ocupar 100% da largura do `<body>`.

|     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- |
| &lt;address&gt; | &lt;article&gt; | &lt;aside&gt; | &lt;blockquote&gt; | &lt;canvas&gt; | &lt;dd&gt; |
| &lt;div&gt; | &lt;dl&gt; | &lt;dt&gt; | &lt;fieldset&gt; | &lt;figcaption&gt; | &lt;figure&gt; |
| &lt;footer&gt; | &lt;form&gt; | &lt;h1&gt; - &lt;h6&gt; | &lt;header&gt; | &lt;hr&gt; | &lt;li&gt; |
| &lt;main&gt; | &lt;nav&gt; | &lt;noscript&gt; | &lt;ol&gt; | &lt;p&gt; | &lt;pre&gt; |
| &lt;section&gt; | &lt;table&gt; | &lt;tfoot&gt; | &lt;ul&gt; | &lt;video&gt; |     |

### Caixa do tipo inline-level

Um elemento do tipo inline-level não vai começar em uma nova linha, e sim no ponto exato onde foram definidos. E a largura dele vai ocupar apenas o tamanho relativo ao seu conteúdo.

|     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- |
| &lt;a&gt; | &lt;abbr&gt; | &lt;acronym&gt; | &lt;b&gt; | &lt;bdo&gt; | &lt;br&gt; |
| &lt;button&gt; | &lt;cite&gt; | &lt;code&gt; | &lt;dfn&gt; | &lt;em&gt; | &lt;i&gt; |
| &lt;img&gt; | &lt;input&gt; | &lt;kbd&gt; | &lt;label&gt; | &lt;map&gt; | &lt;object&gt; |
| &lt;output&gt; | &lt;q&gt; | &lt;samp&gt; | &lt;script&gt; | &lt;select&gt; | &lt;small&gt; |
| &lt;span&gt; | &lt;strong&gt; | &lt;sub&gt; | &lt;textarea&gt; | &lt;tt&gt; | &lt;var&gt; |