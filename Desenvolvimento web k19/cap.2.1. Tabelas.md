cap.2.1. Tabelas

# Tabelas

  Suponha que você esteja desenvolvendo o site de uma empresa e precisa apresentar alguns relatórios em documentos HTML. Considere que os dados desses relatórios são obtidos a partir de

planilhas. Daí surge a necessidade de exibir dados de forma tabular em páginas web.

Para resolver esse problema, podemos utilizar o elemento `<table>`.

Esse elemento permite apresentar dados de forma tabular.

- As linhas de uma tabela são definidas com o elemento `<tr>`.
- As células de títulos com o elemento `<th>`.  
- As células de dados com o elemento `<td>`.

O `colspan` define quantas colunas uma célula deve ocupar e o `rowspan` define quantas linhas uma célula deve ocupar. Normalmente, o table é definido pelos navegadores como **block-level element**.

## Cabeçalho, corpo e rodapé

Para melhorar a semântica das tabelas, podemos definir explicitamente o cabeçalho, o corpo e o

rodapé de uma tabela através dos elementos `<thead>`, `<tbody>` e `<tfoot>` respectivamente.

## Títulos

Também podemos definir um título para uma tabela através do elemento `<caption>`. Esse elemento deve ser o primeiro filho do elemento `<table>`.

## Agrupando colunas

Podemos dividir as colunas de uma tabela em grupos. Normalmente, o principal motivo para estabelecer essa divisão é poder depois definir formatações específicas para cada grupo de colunas.

Para dividir em grupos as colunas de uma tabela, devemos utilizar os elementos `<colgroup>` e `<col>`. O atributo `span` do elemento `<col>` define a quantidade de colunas de um determinado grupo.

```html
<table>
    <colgroup>
        <!-- Agrupando a primeira e a segunda coluna -->
        <col span="2" style="background-color:gray">
    
        <!-- Agrupando apenas a terceira coluna -->
        <col style="background-color:yellow">
    </colgroup>
    ...
</table>
```