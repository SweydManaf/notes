## Listas não ordenas

Se você compreendeu a criação de listas ordenadas, com certeza vai entender as **unordered lists**, também chamadas de listas com marcadores, que são aquelas onde a ordem dos itens não influenciará no significado da lista. Ela é apenas uma ótima maneira para organizar os itens que não apresentam uma classificação necessariamente.
Para criar uma **unordered list**, vamos usar a tag `<ul>` para delimitar a lista e a tag `<li>` para criar cada um dos seus itens internos.

```html
<body>
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
        <li>Item 4</li>
        <li>Item 5</li>
    </ul>
</body>
```

O marcador padrão é a bolinha preta totalmente preenchida (circle), mas existe a opção de configurar a propriedade `type` da tag `<ul>` com os seguintes valores:

‣ disc - padrão. Uma bola preta totalmente pintada

‣ circle - Uma bola com uma borda preta e sem preenchimento

‣ square - Um pequeno quadrado preto totalmente pintado