---
title: cap.2.6. Drop-down list
updated: 2021-03-11 22:35:04Z
created: 2021-03-11 22:24:45Z
---

# Drop-down list

Muitos formulários permitem que os usuários selecionem um ou mais itens de uma lista de opções. Essa seleção pode ser realizada através de um **drop-down list**. Para adicionar esse tipo de componente, devemos utilizar o elemento `select`. Normalmente, o `select` é definido pelos navegadores como **inline-level element**.

As opções devem ser definidas no conteúdo do elemento `select` e elas são adicionadas com o elemento `option`. O conteúdo do elemento `option` é exibido para os usuários. Esse elemento possui um atributo chamado `value`. Quando o formulário for enviado, o valor do atributo `value` é transmitido ao Web Server se a opção correspondente foi selecionada pelo usuário. Se esse atributo não estiver definido, o conteúdo do elemento `option` é transmitido ao Web Server se a opção correspondente foi selecionada pelo usuário.

```html
<select name="estado" id="estado_id">      
    <option value="SP">São Paulo</option>
    <option value="RJ">Rio de Janeiro</option>
    <option value="RS">Rio Grande do Sul</option>
    <option value="RN">Rio Grande do Norte</option>
</select>
```

Por padrão, apenas um item de um **drop-down list** pode ser selecionado pelos usuários. Mas, utilizando o atributo `multiple`, um ou mais itens podem ser selecionados.

Nos **drop-down lists** com muitas opções, é interessante agrupar as opções em categorias. Esse agrupamento pode ser realizado com o elemento `optgroup`. Esse elemento possui um atributo chamado `label`. O valor desse atributo é exibido no `drop-down list`.

## Drop-down list com items pré-selecionados

Quando um **drop-down list** é exibido para os usuários, opções podem estar por padrão selecionadas. O atributo `selected` do elemento `option` define as opções que devem estar selecionadas quando um **drop-down list** é exibido para os usuários. Esse atributo não precisa de valor.