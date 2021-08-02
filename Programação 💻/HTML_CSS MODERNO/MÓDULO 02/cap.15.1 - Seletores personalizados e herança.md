cap.15.1 - Seletores personalizados e herança 

# Personalizando Seletores

Para começar a dar mais poder às CSS, criando estilos personalizados, precisamos aprender a utilizar os seletores de id (**#**) e de class (**.**) de maneira eficiente. Ao criar nosso conteúdo

em HTML, podemos **identificar** um determinado elemento único com um **id**, ou **agrupar** elementos múltiplos que tenham características semelhantes com um **class**. Vamos olhar um

exemplo simples de documento HTML, com propriedades identificadoras:

```html
<body>
    <h1 id="titulo principal">Aprenda Desenvolvimento Web</h1>
    <h1>Aprenda HTML</h1>
    <h2 class="topico">Semântica Web</h2>
    <p class="texto">Lorem ipsum dolor sit, amet consectetur adisicing elit.</p>
    <h1>Aprenda CSS</h1>
    <h2 class="topico">Estilos Web</h2>
    <p>Lorem ipsum dolor sit, amet consectetur adisicing elit.</p>
</body>
```

Olhando atentamente para ao documento, vimos que o `<h1>` principal se diferencia dos demais, pois ele possui um `id`.

Agora foque sua atenção e perceba que os dois títulos `<h2>` possuem o mesmo `class`.

Um id vai **identificar** um elemento único dentro da página atual. Essa identificação vai nos permitir criar um estilo especial para um elemento isolado. Já um class vai identificar uma **classe** à qual um ou mais elementos pertençam, compartilhando características em comum a todos os que façam parte desse grupo.

Em um documento HTML, só podemos usar um ida para único elemento, o que significa que não podemos ter dois elementos com o mesmo `id` dentro da mesma página.

Porém, podemos atribuir um mesmo `class` para vários elementos que possuam essa mesma característica.

Todo `id` em HTML é identificado nas CSS por um símbolo #. Toda `class` em HTML é identificada nas CSS por um ponto .

```css
h1 {
    font-size: 2em;
    color: darkgreen;
}

#titulos-principal {
    background-color: darkgreen;
    text-align: center;
    color: white;
}

.topico {
    text-align: right;
}
```

# Propriedades herdadas

Caso haja duplicidade nas configurações, o que fica valendo é a propriedade especifica (id ou class) adicionando ou sobrescrevendo a propriedade.