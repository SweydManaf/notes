# A ideia do projeto

A ideia inicial é criar uma espécie de site de notícias, só que com uma notícia só 😅 . O objetivo aqui é apenas ensinar como organizar o conteúdo e apresentá-lo em forma de página Web.

Tudo começa desenhando o que chamamos de **wireframe**, planejando qual vai ser a estrutura e comportamento do site. Ele vai servir de base na hora de planejar as caixas que farão parte da página.

\[...\]

## Personalizando ainda mais as listas

No nosso projeto, quero adicionar uma lista com todas as 14 versões principais do sistema Android. Se fizermos usando apenas os elementos comuns sem configurá-los, teremos uma listagem que ocupa um grande espaço vertical. A solução aqui é dividir a lista em duas colunas e modificar o marcador para personalizar ainda mais a exibição do conteúdo.

```css
ul {
    list-style-type: '\2714\0020\0020';
    columns: 2;
    list-style-position: inside;	
}
```

A primeira linha de declarações faz com que o marcador seja personalizado com o parâmetro `list-style-type`. O valor **\\2714** corresponde ao símbolo ✔ que tem o código **Unicode U+2714** (confira no site da Emojipedia). O valor **\\0020** corresponde **a um espaço em branco**.

## Vídeos do YouTube mais flexíveis

Quando incorporamos um vídeo do YouTube ou Vimeo, isso é feito através de uma tag `<iframe>` que já vem com as configurações de um tamanho fixo e precisamos alterar isso para que nossa interface possa se tornar **mais responsiva** e adaptar o tamanho do vídeo dinamicamente, principalmente para telas pequenas.

Para isso, vamos colocar o `<iframe>` de incorporação dentro de uma `<div>` para que o vídeo esteja limitado dentro de um **contêiner**.

A partir daí, vamos fazer configurações de estilo para os dois elementos:

```css
div.video {
    position: relative;
    background-color: var(--cor4);
    height: 0px;
    margin-left: -20px;
    margin-right: -20px;
    margin-bottom: 15px;
    padding-bottom: 59%;
}

div.video > iframe {
    position: absolute;
    top: 5%;
    left: 5%;
    width: 90%;
    height: 90%;
}
```

O que nos importa mais aqui é entender o funcionamento da propriedade **position**, que é a única que não vimos até aqui. O valor padrão para essa propriedade de posicionamento é **static**, que mantém a hierarquia conforme estabelecido no documento **HTML**.

Na `div`, nós colocamos o valor como relative para que seja considerado o posicionamento atual do elemento de divisão e que ele se mantenha adaptável para o caso de alteração no tamanho do navegador.

Já dentro do `iframe`, nós usamos o posicionamento **absolute** para que a `div` \- que é o seu contêiner - torne-se o ponto de partida para o posicionamento do frame. A partir daí, podemos utilizar propriedades para configurar o deslocamento à esquerda (**left**) e ao topo (**top**) e seu tamanho em largura (`width`) e altura (`height`), todos em porcentagem de tela.