cap.2.10. Partes de um documento HTML

# Partes de um documento HTML

Normalmente, um documento HTML pode ser dividido em “pedaços”. Por exemplo, é comum existir cabeçalhos, rodapés e menus de navegação na maior parte das páginas web. No HTML5, diversos elementos foram adicionados para definir especificamente os principais “pedaços” que geralmente um documento HTML possui.

## `header`

O elemento `header` é utilizado para definir um cabeçalho de um documento HTML ou de uma seção de um documento HTML. O objetivo desse elemento é definir um conteúdo de introdução ou de navegação. Normalmente, no `header`, encontramos os elementos `h1`, `h2`, `h3`, `h4`, `h5` e `h6`. No conteúdo do `header`, também é comum encontrar **sumários**, **formulários** de **busca**, **logos**, entre outros.

## `footer`

O elemento `footer` é utilizado para definir um rodapé para o documento HTML ou para uma seção do documento HTML. É muito comum encontrarmos em seu conteúdo informações sobre a seção a qual ele pertence como **quem a escreveu**, **links relacionados ao conteúdo da seção** e **informações legais**.

## `nav`

O elemento `nav` é utilizado para definir um bloco com os principais **links** de um documento HTML. É comum, definir os principais links de um documento HTML nos rodapés. Dessa forma, o elemento `nav` aparecerá com frequência no conteúdo do elemento `footer`.

## `section`

O elemento `section` é utilizado para definir uma seção genérica de um documento. Uma seção é o agrupamento de um conteúdo dentro de um tema. Normalmente, as seções possuem **cabeçalho** e **rodapé**.

## `article`

O elemento `article` é utilizado para definir uma composição independente em um documento HTML. A princípio, um `article` pode ser distribuído independentemente ou facilmente reutilizado. É apropriado utilizar esse elemento para **definir um post de um fórum**, **um artigo de uma revista ou jornal**, **um post de um blog**, **um comentário enviado por um usuário**, um widget interativo ou qualquer item independente de conteúdo.

Considere um blog no qual os usuários podem enviar comentários sobre os posts publicados. Os posts desse blog podem ser definidos com o elemento `article`. Os comentários podem ser definidos com elementos `article` internos aos que definem os posts. Um elemento `article` dentro de outro elemento `article` deve definir algo relacionado ao conteúdo do `article` que o contém.

## `aside`

O elemento `aside` é utilizado para definir algum conteúdo que esteja relacionado ao conteúdo principal, mas não é o foco do documento HTML. Normalmente, **esse elemento é exibido em uma coluna lateral em relação ao conteúdo principal**.

## `figure`

O elemento `figure` deve ser utilizado para definir um conteúdo que é auto-suficiente e tipicamente referenciado como uma unidade singular do fluxo principal do documento. Opcionalmente o conteúdo pode possuir uma legenda. Por exemplo, esse elemento pode ser utilizado para definir **ilustrações**, **diagramas**, **fotos**, **vídeos**, **códigos fonte em um documento HTML**. Normalmente, esse itens são referenciados no conteúdo principal mas podem ser removidos sem afetar o fluxo do documento.

## `figcaption`

O elemento `figcaption` deve ser filho de um elemento `figure`. Ele **é utilizado para definir a legenda do conteúdo do elemento pai**. Além disso, o elemento `figcaption` deve ser o primeiro ou último filho de um elemento figure.

![Captura de tela_2021-03-13_02-56-51-edit.png](../_resources/44a4f5da5bca49a6bdb1a4ee12862bd0.png)

Normalmente, os elementos `header`, `footer`, `nav`, `header`, `article`, `aside`, `section`, `figure` e `figcaption` são definidos pelos navegadores como **block-level elements**.