cap.2.8. Autocomplete

# Autocomplete

Para melhorar a usabilidade, podemos utilizar o recurso do autocomplete nas caixas de entrada.

Para utilizar esse recurso, devemos criar uma lista de sugestões com o elemento `datalist`. É fundamental identificar as listas de sugestões com o atributo `id`.

```html
<input type="text" name="comida" id="comida_id" list="comidas_id">
<datalist id="comidas_id">
    <option value="Lasanha"></option>
    <option value="Pizza"></option>
    <option value="Sopa"></option>
    <option value="Salada"></option>
</datalist>
```

As opções devem ser definidas no conteúdo do elemento `datalist` e elas são adicionadas com o elemento `option`. O atributo value de um elemento `option` define uma sugestão.

Com a lista de sugestões criada, podemos associá-la a uma caixa de entrada através do atributo `list` do elemento `input`.