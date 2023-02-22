## O desafio de mostrar conteúdo, não importa a mídia

O primeiro passo para adaptar o conteúdo ao tamanho da tela nós já demos! Quando começamos a estudar CSS, falamos bastante sobre recursos que facilitariam a responsividade, adaptando o conteúdo ao tamanho da tela usando valores percentuais e as medidas **vh** e **vw**. Porém, é preciso aprender mais para adaptar ainda mais os conteúdos e é aí que entram as **Media Queries**.

Os primeiros estudos sobre essa tecnologia surgiram com os **media types**, que basicamente criavam um formato específico para determinado tipo de mídia (tela, impressora, dispositivos para braille, portáteis handheld, projetores, conteúdo lido, TVs, telas de grade fixa, etc).

O principal problema é que só os media types não foram suficientes, pois quando falávamos em telas, tínhamos tamanhos, formatos, suporte máximo de cores, resoluções, proporções e compatibilidades muito diferentes. Um exemplo típico é comparar as telas de alguns modelos de smartphones.

É aí que surgiram as media queries. Elas são basicamente as media types somadas às media features, que são características extras que foram criadas para que possamos personalizar ainda mais nossas folhas de estilo. A seguir, enumero algumas dessas características que podem ser testadas:

- width e height
- device-height e device-width
- aspect-ratio e device-aspect-ratio
- orientation
- resolution
- color e color-index
- grid
- scan

## Como usar uma Media Query?

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Media Query</title>
    <!-- Chamadas de Media Query-->
    <link rel="stylesheet" href="estilos/principal.css" media="all">
    <link rel="stylesheet" href="estilos/tela.css" media="screen">
    <link rel="stylesheet" href="estilos/impressora.css" media="print">
</head>
```

## Media query definida nas CSS

```css
/* TABLET */
@media screen and (min-width: 768px) and (max-width:992px) {
   ...
}

/* DESKTOP */
@media screen and (min-width:992px) and (max-width:1200px) {
    ...
}

/* GRANDES TELAS */
@media screen and (min-width:1200px) {
    ...
}
```

## O conceito de Mobile First

Em uma abordagem mais tradicional, quando pensamos na construção de um site, idealizamos toda a estrutura e os recursos visuais que ele pode ter, criamos o layout completo, implementamos o projeto em um computador e depois nos preocupamos em adaptar toda a sua estrutura para que as telas menores possam exibir o site sem maiores problemas. Isso é o que chamamos de design responsivo.

Porém, em uma abordagem um pouco diferente, podemos trilhar exatamente o caminho contrário, pensando inicialmente no layout e funcionalidades da versão móvel e depois adaptando tudo a telas maiores. Esse é o conceito proposto pela linha chamada de **mobile first** (o móvel primeiro), esquema proposto por **Luke Wroblewski** em 2009. Atualmente chefe de produtos Google, LukeW é considerado um dos “pais” dessa abordagem de desenvolvimento.

E para contribuir ainda mais com essa visão, em 2018 o Google anunciou que passaria a valorizar mais na sua indexação os sites que tivessem a preocupação em gerar uma melhor experiência móvel ao usuário. E quem não quer ser valorizado na indexação orgânica da maior ferramenta de buscas do mundo?

Segundo o princípio fundamental da filosofia mobile first, pensar primeiro na versão móvel trás algumas vantagens:

- Uma maior divulgação do site, pois como vimos anteriormente, ferramentas de busca vão valorizá-lo.
- Uma melhor experiência do usuário, que vai ter acesso ao conteúdo que foi pensado para que pudesse ser consumido de forma mais confortável e sem confusões.
- Aumento na credibilidade, já que os visitantes vão ter a percepção (ainda que inconsciente) de que quem criou o site se preocupou com a sua experiência.
- Otimização do carregamento, uma vez que sofremos com conexões lentas e dispositivos populares sem tanto poder de processamento. Dessa maneira, respondendo à dúvida que havia sido levantada anteriormente, o código CSS que criamos não possui uma regra @media específica para dispositivos móveis pois ela simplesmente é a configuração padrão das nossas folhas de estilo. Não esquecemos as configurações para pequenas telas, simplesmente estamos usando o conceito de mobile first.