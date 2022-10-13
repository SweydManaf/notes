# Checkboxes e Radios

Para adicionar um **checkbox** em um formulário, devemos utilizar o elemento `<input>` com `type` igual a **checkbox**. Ao utilizar esse componente, é importante definir um valor para o atributo `value`. No envio do formulário, esse valor é transmitido ao Web Server se o **checkbox** correspondente estiver marcado.

Eventualmente é interessante agrupar um determinado conjunto de **checkboxes**. Por exemplo, considere um formulário que coleta as linguagens de programação que os usuários conhecem.

Para cada linguagem, podemos definir um **checkbox**. Para agrupar esses checkboxes, basta definir o atributo `name` com o mesmo valor para eles.

```html
<input type="checkbox" name="linguagens" id="java_id">
<label for="java_id">Java</label>
<input type="checkbox" name="linguagens" id="csharp_id">
<label for="csharp_id">C#</label>
<input type="checkbox" name="linguagens" id="php_id">
<label for="php_id">PHP</label>
<input type="checkbox" name="linguagens" id="ruby_id">
<label for="ruby_id">Ruby</label>
<input type="checkbox" name="linguagens" id="perl_id" checked>
<label for="perl_id">Perl</label>
```

Para adicionar um **radio** em um formulário, devemos utilizar o elemento `<input>` com `type` igual a **radio**. Ao utilizar esse componente, é importante definir um valor para o atributo `value`. No envio do formulário, esse valor é transmitido ao Web Server se o radio correspondente estiver marcado.

Eventualmente é interessante agrupar um determinado conjunto de radios. Por exemplo, considere um formulário que coleta o time preferido dos usuários. Para cada time, podemos definir um radio. Para agrupar esses radios, basta definir o atributo `name` com o mesmo valor para eles.

```html
<input type="radio" name="time-preferido" id="sp_id" value="sao-paulo">
<label for="sp_id">São Paulo</label>
<input type="radio" name="time-preferido" id="barcelona_id" value="barcelona">
<label for="barcelona_id">Barcelona</label>
<input type="radio" name="time-preferido" id="milan_id" value="milan" checked>
<label for="milan_id">Milan</label>
<input type="radio" name="time-preferido" id="mu_id" value="manchester-united">
<label for="mu_id">Manchester United</label>
```

Por padrão, quando um formulário é exibido para os usuários, os **checkboxes** e os **radios** não estão marcados. Algumas vezes, desejamos que determinados checkboxes e radios estejam marcados quando os formulários são apresentados aos usuários. Para resolver esse problema, podemos utilizar o atributo `checked` do elemento `<input>`. Esse atributo não precisa de valor.

# Seleção de cores

No HTML5, para coletar uma cor, podemos utilizar o elemento `<input>` com `type` igual a **color**.

```html
<input id="cor_id" name="cor" type="color">
```