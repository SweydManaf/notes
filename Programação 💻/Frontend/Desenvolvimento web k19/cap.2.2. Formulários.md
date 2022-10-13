# Formulários

Para tornar os sites e as aplicações web mais interativos, podemos utilizar formulários. Através

dos formulários, os usuários podem enviar informações aos Web Servers.

Para criar um formulário, devemos utilizar o elemento `<form>`. Esse elemento possui um atributo chamado `action`. O valor desse atributo indica para qual endereço os dados do formulário serão enviados.

Os formulários são compostos por caixas de texto, checkboxes, rádios, caixas de seleção, botões, entre outros componentes.

# Caixa de texto

Geralmente, os formulários possuem uma ou mais caixas de texto. As caixas de texto são adicionadas nos documentos HTML através do elemento `<input>`. Esse elemento possui um atributo chamado type. Para definir uma caixa de texto, o valor do atributo `type` deve ser **text**. Normalmente, o input é definido pelos navegadores como **inline-level element**.

# Rótulos

Nos formulários, os rótulos são fundamentais para informar aos usuários quais dados devem ser preenchidos. Para adicionar um rótulo, devemos utilizar o elemento `<label>`. Os textos dos rótulos são definidos no conteúdo desse elemento.

Para melhorar a acessibilidade dos documentos HTML, os rótulos devem ser explicitamente associados aos campos dos formulários. Para estabelecer esse vínculo, o primeiro passo é identificar os campos através do atributo `id`. O segundo passo é definir o atributo `for` do elemento `<label>` com o identificador do campo correspondente ao rótulo.

```html
<label for="nome_id">Nome: </label>
<input type="text" name="nome" id="nome_id">
```

# Placeholders

Como vimos, os rótulos são utilizados para informar aos usuários quais dados devem ser preenchidos nos formulários. Além dos rótulos, podemos utilizar `placeholders` para dar dicas ou exemplos do conteúdo que desejamos em cada caixa de entrada. Um `placeholder` é criado através do atributo `placeholder` do elemento `<input>`.

```html
<label for="nome_id">Nome: </label>
<input id="nome_id" type="text" name="nome" placeholder="Digite o seu nome">
```

# Botões de submit

Para adicionar um botão de submit em um formulário, podemos utilizar o elemento `<input>` com `type` igual a **submit**. Esse tipo de botão envia os dados do formulário para o Web Server. Os textos desses botões são definidos com o atributo `value`.

Outra forma de adicionar um botão de submit em um documento HTML é utilizar o elemento `<button>` com `type` igual a **submit**. Diferentemente do elemento `<input>`, o elemento `<button>` permite a criação de botões com imagens além de texto.