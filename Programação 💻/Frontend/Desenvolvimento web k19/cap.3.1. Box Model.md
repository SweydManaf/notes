<img src="../../../_resources/box-model.png" alt="box-model.png" width="519" height="318">

Na imagem, os boxes dos **block-level elements** foram exibidos com **linha contínua** enquanto os boxes dos **inline-level elements** foram exibidos com **linha tracejada**. Os boxes dos block-level elements ocupam todo o espaço horizontal e provocam quebras de linha. Por outro lado, os boxes dos inline-level elements ocupam horizontalmente somente o espaço necessário para o seu conteúdo e não provocam quebras de linha.

<img src="../../../_resources/boxModel.png" alt="boxModel.png" width="509" height="339">

Observe que a **largura de um box** corresponde à soma dos seguintes comprimentos.

•   Margem externa da esquerda (`margin-left`)

•   Borda da esquerda (`border-left`)

•   Margem interna da esquerda (`padding-left`)

•   Largura do conteúdo (`width`)

•   Margem interna da direita (`padding-right`)

•   Borda da direita (`border-right`)

•   Margem externa da direita (`margin-right`)

Analogamente, a **altura de um box** corresponde à soma dos seguintes comprimentos.

•   Margem externa superior (`margin-top`)

•   Borda superior (`border-top`)

•   Margem interna superior (`padding-top`)

•   Altura do conteúdo (`height`)

•   Margem interna inferior (`padding-bottom`)

•   Borda inferior `(border-bottom`)

•   Margem externa inferior (`margin-bottom`)

# Comentários

Podemos adicionar comentários no código CSS através dos marcadores /* e */.

```css
/* uma regra CSS para formatar os parágrafos */
p  {
    color: red;
}
```