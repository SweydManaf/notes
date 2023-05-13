# Imagens de fundo

- Para definirmos um backgound estatico usamos a propriedade `background-color:` ;
- Para definirmos um backgound com degrade usamos background-image: `linear-gradient(to bottom, yellow, orange);`
- Para definirmos um background especifico (uma imagem) usamos `background-image:url('imagens/pattern003.png');`

## Personalizando a aplicação do background

- `background-repeat: repeat;` \- repete até preencher a div;
- `background-repeat: no-repeat;` \- não repete, aparece uma única vez;
- `background-repeat: repeat-x;` \- repete apenas no eixo x;
- `background-repeat: repeat-y;` \- repete apenas no eixo y;

Note que ao usar o no-repeat, isso não obriga o navegador a aumentar ou diminuir o tamanho da imagem para caber no tamanho da caixa. Para realizar essa adaptação, devemos usar outra propriedade.

- A propriedade `background-position` permite posicionar o referencial da imagem que pode ser: **left top**, **center top**, **right top**, **left center**, **center center**, **right center**, **left bottom**, **center bottom**, **right bottom**.

Outra coisa que podemos fazer é redimensionar a imagem para forçá-la a caber na caixa. Por padrão, nenhum redimensionamento será aplicado, e a imagem será exibida do seu tamanho natural. Porém, podemos usar a propriedade background-size para alterar esse comportamento.

Os valores aceitos por essa propriedade são:

|     |     |
| --- | --- |
| auto | (padrão) a imagem de fundo será aplicada em seu tamanho original. |
| \[length\] px \[length\] % | Redimensiona a largura da imagem e faz a altura se adaptar automaticamente.Podemos também informar as duas dimensões na sequência ou também usar valores percentuais. |
| cover | Muda o tamanho da imagem para que ela seja sempre totalmente exibida na tela, sem nenhum corte. |
| contain | Redimensiona a imagem para que ela cubra o contêiner, mesmo que para isso<br><br>ocorram alguns eventuais cortes. |

## Simplificando as coisas

```css
body{
    /*
    	background-color: black;
        background-image: url(imagens/wallpaper002.jpg);
        background-position: center center;
        background-repeat: no-repeat;
        background-size: cover;
        background-attachment: fixed; */
    
     	/*Shorthand - background
     	color > image > position > repeat > [size] > attachment */
     	
    	background: black url(imagens/wallpaper002.jpg) center center no-repeat fixed;
        background-size: cover;
}
```

## Centralizando a div

```css
#container{
            background-color: purple;
            background-image: url(imagens/target001.png);
            background-size: 100% 100%;

            position: relative;
            height: 96vh;
            padding: 10px;
        }

#conteudo{
            background-image: url(imagens/target001.png);
            background-size: 100% 100%;

            position: absolute;
            height: 200px;
            width: 400px;
            background-color: yellow;

            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            
        }
```