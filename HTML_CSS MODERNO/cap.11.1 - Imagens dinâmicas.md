cap.11.1 - Imagens dinâmicas

# Imagens Flexíveis

Nosso primeiro passo no caminho de adaptar nosso conteúdo ao tamanho da tela vai ser aprender a gerar imagens de tamanho diferentes e a fazer o navegador carregar a imagem certa para cada situação. Para isso, devemos conhecer as tags `<picture>` e `<source>`.

Para esse exemplo, criamos as três imagens ao lado: a menor tem **300x300px**, a média tem **700x700px** e a maior tem **1000x1000px**.

Essas imagens serão carregadas pelo navegador de acordo com o tamanho da janela atual. Para isso, criamos o seguinte código base:

```html
<picture>
    <img src="foto-g.png" alt="A imagem flexível funciona">
</picture>
```

A novidade aqui é que inserimos essa imagem dentro da tag `<picture>`, que vai concentrar as outras fontes de imagem. Por padrão, a imagem **foto-g.png** (1000x1000px) será carregada.

O problema vai começar a surgir quando a janela do navegador chegar perto dos 1000 pixels de largura, pois a foto não vai mais caber lá. Vamos agora adicionar uma linha para resolver esse problema:

```html
<picture> 
    <source media="(max-width: 1050px)" srcset="foto-m.png" type="image/png">
    <img src="foto-g.png" alt="A imagem flexível funciona">
</picture>
```

Note que a tag `<source>` possui três atributos:

‣ **type** vai indicar o media type da imagem que usamos (veja mais informações sobre media types no capítulo 10)

‣ **srcset** vai configurar o nome da imagem que será carregada quando o tamanho indicado for atingido

‣ **media** indica o tamanho máximo a ser considerado para carregar a imagem indicada no atributo srcset.

Você vai perceber que a imagem muda automaticamente conforme aumentamos ou diminuímos o tamanho da tela.

Vamos continuar e acrescentar mais um `<source>` à nossa imagem:

```html
<picture>
    <source media="(max-width: 750px)" srcset="foto-p.png" type="image/png">
    <source media="(max-width: 1050px)" srcset="foto-m.png" type="image/png">
    <img src="foto-g.png" alt="A imagem flexivel funciona">
</picture>
```

É importante que existe uma ordem entre os `<source>`, e nessa nossa configuração, os itens mais acima sejam os menores tamanhos para **max-width** e que os seguintes sejam maiores, de forma crescente. O último item dentro de `<picture>` deve ser a imagem padrão.