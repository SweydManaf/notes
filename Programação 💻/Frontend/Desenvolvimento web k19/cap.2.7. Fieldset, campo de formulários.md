---
title: cap.2.7. Fieldset, campo de formulários
updated: 2021-03-11 23:00:14Z
created: 2021-03-11 22:35:13Z
---

# Fieldset

Os campos de um formulário muito longo podem ser agrupados logicamente com o elemento `fieldset`. No conteúdo desse elemento, podemos utilizar o elemento `legend` para definir a legenda do fieldset. Normalmente, o `fieldset` é definido pelos navegadores como **block-level element**.

```html
<body>
    <fieldset>
        <legend>Dados Pessoais</legend>
        ...
    </fieldset>
    <fieldset>
        <legend>Formação</legend>
        ...
    </fieldset>
    <fieldset>
        <legend>Experiência</legend>
        ...
    </fieldset>
</body>
```