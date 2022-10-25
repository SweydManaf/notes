---
title: cap.2.9. Validação
updated: 2021-03-13 00:20:05Z
created: 2021-03-13 00:12:35Z
---

# Validação

Alguns recursos para realizar a validação dos campos de um formulário foram adicionados no HTML5. Essas validações ocorrem antes do envio dos formulários. Por padrão, algumas validações são realizadas automaticamente de acordo com o tipo do campo. Por exemplo, os navegadores verificam se o conteúdo de uma caixa de email é um email válido e ai vai.

Outras validações devem ser definidas explicitamente. Por exemplo, se um determinado campo é obrigatório, devemos utilizar o atributo `required`. Esse atributo não precisa de valor.

Se um determinado campo deve respeitar uma **expressão regular**, devemos utilizar o atributo `pattern`.

```html
<input 
    type="text" 
    id="placa_id"
    name="placa" 
    pattern="[A-Z]{3} [0-9]{4}" 
    title="As placas são formadas por 3 letras ou 4 números">
```

Se o conteúdo de um campo numérico deve estar em um determinado intervalo, podemo utilizar os atributos `min` e `max`.