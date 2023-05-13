---
title: cap.2.3.  Caixas de entrada específicas
updated: 2021-02-28 11:53:33Z
created: 2021-02-27 14:14:17Z
---

# Caixas de entrada específicas

As caixas de texto são componentes muito genéricos. Antes do HTML5, informações de natureza bem distintas eram obtidas através desses componentes. Para melhorar a semântica dos documentos HTML, tipos específicos de caixas foram adicionados no HTML5.

# Caixas de busca

Assim como as caixas de texto, as caixas de busca são adicionadas nos formulário com o elemento `<input>`. A diferença é que o valor do atributo `type` deve ser **search** ao invés de **text**.

```html
<input id="keywords_id" name="keywords" type="search">
```

As caixas de busca devem ser utilizadas para coletar palavras chave que serão utilizadas em algum tipo de pesquisa. A princípio não há nenhuma diferença prática entre as caixas de texto e as caixas de busca. Contudo, essa diferenciação adiciona valor semântico aos documentos HTML e possibilita, por exemplo, que os navegadores diferenciem visualmente esses dois tipos de caixas.

# Caixa de números

Para coletar dados numéricos, podemos utilizar caixas específicas para números. No HTML5, há dois tipos de caixas para esse propósito. Os dois são definidos com o elemento `<input>`. O valor do atributo `type` é **number** para o primeiro tipo e **range** para o segundo tipo.

```html
<input id="numero1_id" name="numero1" type="number">
<input id="numero2_id" name="numero2" type="range">
```

Para definir a sequência dos números que podem ser selecionados pelos usuários, podemos utilizar os atributos `min`, `max` e `step`.

# Caixas de email, telefone e url

No HTML5 foram definidas caixas de entradas específicas para emails, telefones e urls. Essas caixas são adicionadas com o elemento `<input>`. O valor do atributo `type` deve ser **email**, **tel** e **url** para emails, telefones e urls respectivamente.

```html
<input id="email_id" name="email" type="email">
<input id="telefone_id" name="telefone" type="tel">
<input id="url_id" name="url" type="url">
```

A usabilidade das páginas web melhora com a utilização dessas caixas. Por exemplo, a configuração do teclado dos celulares ou tablets pode ser alterada de acordo com o tipo de caixa de entrada. Nas caixas de **email**, o caractere “@” pode ser adicionado ao teclado. Nas caixas de **telefone**, o teclado não precisa conter as letras do alfabeto. Nas caixas de **url**, teclas especiais como “.com” ou “www” podem ser adicionadas ao teclado.

# Caixas de datas e horas

Diversos tipos de caixas de entrada para coletar datas e horas foram adicionados no HTML5.

Todas essas caixas são adicionadas com o elemento `<input>` e o valor do atributo `type` desse elemento assumirá um dos valores listados a seguir.

- **date**: Utilizado para coletar data (dia, mês e ano) sem fuso horário.
- **datetime**: Utilizado para coletar data (dia, mês e ano) e hora (hora, minuto, segundo e fração

de segundo) com fuso horário em UTC.

- **datetime-local**: Utilizado para coletar data (dia, mês e ano) e hora (hora, minuto, segundo e

fração de segundo) sem fuso horário.

- **month**: Utilizado para coletar data composta por mês e ano sem fuso horário.
- **time**: Utilizado para coletar hora (hora, minuto, segundo e fração de segundo) sem fuso horá-

rio.

- **week**: Utilizado para coletar data composta por semana e ano sem fuso horário.

# Caixas de senha

As senhas devem ser coletadas com caixas específicas para esse tipo de informação. Para adicionar uma caixa de senha em um formulário, devemos utilizar o elemento `<input>` com o valor **password** para o atributo `type`. Normalmente, os navegadores utilizam símbolos como o asterisco ou o círculo para omitir o conteúdo das caixas de senha.

```html
<input id="senha_id" name="senha" type="password">
```

# Caixas de texto longo

Para coletar um texto com várias linhas, podemos utilizar o elemento `<textarea>`. A quantidade de linhas de um `<textarea>` é definida com o atributo `rows` e a quantidade de colunas com o atributo `cols`.

Podemos definir o limite de caracteres que podem ser inseridos no conteúdo do elemento `<textarea>` através do atributo `maxlength`.