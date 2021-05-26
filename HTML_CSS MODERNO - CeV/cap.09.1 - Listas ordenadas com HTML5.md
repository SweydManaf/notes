cap.09.1 - Listas ordenadas com HTML5

## Listas Ordenas

Em HTML é chamada de  **ordered lists** todas aquelas listas onde a ordem do itens é algo muito importante. Um passo-a-passo para criar um bolo, uma lista com os carros mais caros do mundo são exemplos de listas ordenadas.

Para criar uma **ordered list**, vamos usar a tag `<ol>` para delimitar a lista e `<li>` (list item) para identificar cada item da lista.

```html
<body>
    <ol>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
        <li>Item 4</li>
        <li>Item 5</li>
    </ol>
</body>
```

A tag `<ol>` possui um parâmetro `type`, onde configuramos o tipo de marcador da lista atual. As opções de valores para esse parâmetro são:

‣ 1 - Valor padrão. Cria listas numeradas. Ex: 1, 2, 3, 4, …

‣ A - Cria listas alfabéticas em maiúsculas. Ex: A, B, C, D, …

‣ a - Cria listas alfabéticas em minúsculas. Ex: a, b, c, d, …

‣ I - Cria listas com algarismos romanos em maiúsculas. Ex: I, II, III, IV, …

‣ i - Cria listas com algarismos romanos em minúsculas. Ex: i, ii, iii, iv, …

Você também pode indicar o início da contagem usando o parâmetro start.
Por exemplo, a tag `<ol type=“I” start = “5”>` vai gerar itens numerados como V, VI, VII, VIII, IX,