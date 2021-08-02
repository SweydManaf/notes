cap.09.3 - Listas de definição com HTML5

## Listas de definição

É como se fosse um dicionário, temos os termos e as suas descrições. É uma lista sem demarcadores, mas bem útil em alguns casos.
Toda lista de definições está dentro de uma tag `<dl> </dl>` (definition list) Cada termo é um `<dt>` (definition term) e cada descrição é um `<dd>` (definition description).
Assim como os itens da lista, essas duas últimas tags possuem fechamento opcional, segundo a referência oficial da HTML5.

```html
<body>
    <dl>
        <dt>HTML</dt>
        <dd>Linguagem de marcação utilizada para criar conteúdo de sites</dd>
        
        <dt>CSS</dt>
        <dd>Linguagem de marcação para especificação de estilos em sites</dd>
        
        <dt>JavaScript</dt>
        <dd>Linguagem de programação para criar interatividades em sites.</dd>
    </dl>
</body>
```