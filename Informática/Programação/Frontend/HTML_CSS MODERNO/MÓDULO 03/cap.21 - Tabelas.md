# Tabelas

NB: Tabelas: Tabelas são para apresentar conteúdos, não para construir estruturas de sites.

Antes de começar a estudar as tabelas, vamos retirar um assunto da frente. Houve uma época em que os sites eram desenvolvidos como se fossem tabelas. Foi um tempo sombrio e que ficou no passado!

Com a evolução das CSS e com o surgimento da HTML na sua versão 5, os sites podem ser criados de forma mais organizada e dinâmica e não dependem mais das tabelas para existir, um movimento do design que ficou conhecido como tabelas layout (traçado sem tabelas).

## Estrutura de uma tabela pequena e simples

```html
<head>
<style>
        body{
            font-family: Arial, Helvetica, sans-serif;
        }

        table{
            width: 400px;
            height: 400px;
            padding: 8px;
            border-collapse: collapse;
        }

        td {
            border: 1px solid black;
            text-align: left; /* Alinhamento horizontal */
            vertical-align: bottom; /* Alinhamento vertical */
        }

        .numero{
            text-align: right;
        }
</head>
<body>
<h1>Minha primeira tabela</h1>
        <!--   
            HIERARQUIA DE TABELAS (simples)
            TABLE = tabela
                TABLE ROW = linha de tabela
                    TABLE HEADER = cabeçalho
                    TABLE DATA = dado de tabela
        -->
        <table>
            <tr> <!-- Primeira linha-->
                <td>A1</td>
                <td>B1</td>
                <td>C1</td>
            </tr>
            <tr> <!-- Segunda linha-->
                <td>A2</td> 
                <td>B2</td>
                <td class="numero">C2</td>
            </tr> 
            <tr> <!-- Terceira linha-->
                <td>A3</td>
                <td>B3</td>
                <td class="numero">C3</td>
            </tr>
            <tr> <!-- Quarta linha-->
                <td>A4</td>
                <td>B4</td>
                <td>C4</td>
            </tr>

        </table>
</body>
```

## Estrutura de uma tabela grande

```html
<!-- 
    ANATOMIA PARA TABELAS GRANDES
    
    TABLE
        CAPTION -> título da tabela 
        THEAD -> cabeçalho da tabela
             TR -> linha da tabela
                 TH -> titulo
        TBODY -> corpo da tabela
             TR -> linha da tabela
                 TD -> dado
        TFOOT -> rodapé da tabela
             TR - linha da tabela
                 TH, TD
    
    MACETE: table>caption+(thead>tr>th)>(tbody>tr>td)>tfoot>tr>th+td
-->
```

### Ao usar o &lt;th&gt;, defina o escopo

Perceba também que as células de “Cidade” e “População”, possuem seus dados abaixo delas (o que chamamos de escopo de coluna). Já a célula “Total” tem seu dado ao lado dela (o que chamamos de escopo de linha). Sendo assim, vamos fazer as declarações pontuais em cada caso.

```html
<tr>
    <th scope="col">Cidade</th>
    <th scope="col">População</th>
</tr>
...
<tr>
    <th scope="row">Total</th>
    <td>110.659.804</td>
</tr>
```

### Estilizando a tabela

```csss
table {
    width: 600px;
    border: 1px solid black;
    border-collapse: collapse;
}

td, th {
    border: 1px solid black;
}
```

### Efeito zebrado

```css
tbody > tr:nth-child(odd){ /* 2n-1*/
    background-color: white;
}

tbody > tr:nth-child(even){ /* 2n */
    background-color: lightgray;
}
```

A pseudo-classe `nth-child()` vai permitir selecionar as linhas pares `(even)` ou as linhas ímpares `(odd)`, configurando uma cor para cada uma delas. No exemplo acima, inclusive, se o fundo da página já está branco, o segundo seletor (para linhas ímpares) torna-se desnecessário.

### Mudando o alcance das células

Podemos fazer a mesclagem de células adicionando o parâmetro `colspan` ou `rowspan`.

### Personalização de colunas

Podemos criar um agrupamento de colunas, definindo um `<colgroup>` dentro da tabela, logo abaixo da tag `<table>`:

```html
<colgroup>
    <col class="amarelo">
    <col class="vermelho" span="2">
    <col class="amarelo">
</colgroup>
```

Isso vai atribuir uma classe a cada coluna (ou conjunto de colunas, quando usamos `span`). Ao criar uma configuração de cor para cada uma dessas três classes (c1, c2 e c3), podemos criar um efeito de configuração em grupos de colunas.

## Tabelas Responsivas

Para resolver essa limitação, principalmente para telas de celular, e garantir a visualização de todos os dados, uma das soluções mais simples é colocar a tabela dentro de uma caixa qualquer (pode ser uma `div`) e configurar a sua propriedade CSS `overflow-x` para os valores **auto** ou **scroll**. Isso vai fazer com que todo e qualquer conteúdo que “transborde” a largura (eixo x) do tamanho do box, vai ganhar uma barra de rolagem horizontal (por se tratar do eixo x apenas) caso seja necessário.