---
title: cap.15.2 - Pseudo-classes e pseudo-elementos
updated: 2021-06-04 20:15:03Z
created: 2021-06-04 20:02:51Z
---

# Pseudo-classes

Uma **pseudo-classe CSS** é uma palavra-chave adicionada às declarações de um seletor após um sinal de dois pontos e especificam um estado especial de um elemento. Existem várias pseudo-classes para estilos, podemos citar **:hover**, **:visited**, **:active**, **:checked**, **:empty** e **:focus**.

```css
a:visited {
    color: darkred;
}

a:hover {
    text-decoration: underline;
}
```

# Pseudo-elementos

Já um **pseudo-elemento CSS** é uma palavra-chave adicionada às declarações de um seletor após dois sinais de dois pontos e permitem que você formate um pedaço específico do elemento referenciado. Os principais pseudo-elementos usados nas CSS são **::before**, **::after**, **::first-letter**, **::first-line**.

```css
.especial::before {
    content: " >> ";
    font-weight: lighter;
}

.especial::after {
    content: " << ";
    font-weight: lighter;
}
```

**MAIS UM SÍMBOLO**: Toda vez que usamos o símbolo **>** em um seletor, indicamos os filhos (children) imediatos de um elemento. No exemplo HTML que criamos, dizemos que o primeiro parágrafo é direct children da div.

```html
<head>
    <style>
        body {
            font-family: Arial, Helvetica, sans-serif;
        }
        
        div > p {
            display: none;
        }
        
        div:hover > p {
            display: block;
            color: white;
            background-color: red;
            width: 300px;
        }
        
        div:hover {
            color: red;
        }
    </style>
</head>
<body>
    <h1>Exemplo de hover</h1>
    <p>Passe o mouse sobre o texto abaixo</p>
    <div>
        Passe o mouse aqui
        <p>TEXTO ESCONDIDO</p>
    </div>
    <p>Fim do exemplo</p>
</body>
```