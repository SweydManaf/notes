# Botões

## Botões genéricos

Para adicionar um botão genérico em um formulário, podemos utilizar o elemento `<input>` com `type` igual a **button**. As ações desse tipo de componente são definidas com **JavaScript**. Os textos desses botões são definidos com o atributo `value`.

Outra forma de adicionar um botão genérico em um documento HTML é utilizar o elemento `<button>` com `type` igual a **button**. Diferentemente do elemento `<input>`, o elemento `<button>` permite a criação de botões com imagens além de texto.

```html
<button id="botao_id" type="button">
    Botão genérico
    <img src="botao.png" alt="Botão">
</button>
```

## Botões de reset

Para adicionar um botão de reset em um formulário, podemos utilizar o elemento `input` com `type` igual a **reset**. Esse tipo de botão reinicia os dados do formulário. Os textos desses botões são definidos com o atributo value.

```html
<input id="botao_id" type="reset" value="reiniciar">
```

## Botões de upload

      Para adicionar um botão de upload em um formulário, podemos utilizar o elemento `input` com `type` igual a **file**. Esse tipo de botão permite selecionar um arquivo para um eventual upload. O formulário que contém esse botão deve possuir o atributo `enctype` com o valor **multipart/form-data**.

```html
<input id="botao_id" name="file" type="file">
```