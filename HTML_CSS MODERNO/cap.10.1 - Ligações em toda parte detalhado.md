cap.10.1 - Ligações em toda parte detalhado

# Criando links

Para criar um hyperlink, devemos criar âncoras através da tag `<a>`. O principal atributo dessa tag é o `href`, que cria uma referência hipertexto. Vamos ver um exemplo simples:

```html
<h1>Vamos criar um link</h1>
<a href="https://gustavoguanabara.github.io">Acesse meu perfil</a>
```

- Note que dentro do atributo `href`, o que colocamos foi uma URL completa para outro site.
- Outro atributo bem útil da tag de âncora é o `hreflang`, que permite indicar qual é o idioma principal do site para onde o link está desviando o fluxo de navegação. Isso vai permitir avisar ao navegador e a softwares de tradução como lidar caso o visitante opte por traduzir automaticamente os conteúdos.

## Controlando o comportamento dos links

Por padrão, sempre que um visitante clique em um hyperlink, o site de destino abre na mesma janela do site que continha esse link. Ou seja, o conteúdo anterior vai deixar de ser exibido para mostrar o novo conteúdo.

Para poder controlar onde o site de destino vai abrir, podemos usar o atributo `target`, que suporta os seguintes valores:

‣  **_blank** vai abrir o link em uma nova janela em branco

‣  **_self** vai abrir o link na janela ou frame atual (padrão)

‣  **_top** vai desfazer todos os frames e abrir o destino no navegador completo

‣  **_parent** similar ao uso do _top em uma referência à janela mãe

‣  nome-do-frame caso esteja usando frames, indicar o nome da janela a abrir

## Indicando a natureza dos links

Existe um recurso bem interessante para links que é indicar qual é a natureza do destino usando o atributo `rel`. Esse atributo aceita vários valores, entre eles vou citar:

‣  **next** indica que o link é para a próxima parte do documento atual

‣  **prev** indica que o link é para a parte anterior do documento atual

‣  **author** indica que é um link para o site do autor do artigo atual

‣  **external** indica que é um link para outro site que não faz parte do site atual

‣  **nofollow** indica que é um link para um site não endossado, como um link pago

## Links para downloads

Outra coisa que aparece bastante em sites são os links para efetuar download de algum material em PDF, ou de um arquivo ZIP qualquer. A partir da versão HTML5, as âncoras receberam atributos especiais para isso. Basta fazer o link diretamente para o arquivo que se deseja efetuar o download e adicionar o atributo download com o valor configurado para o nome do arquivo a ser baixado e o atributo `type` para indicar ao navegador que tipo de arquivo está sendo baixado. Vamos ver um exemplo:

```html
<a href="arquivos/meulivro.pdf" download="meulivro.pdf" type="application/pdf">
    Baixe aqui o PDF do meu livro
</a>
```

Aqui vão alguns media types bem usados no nosso dia-a-dia:

|     |     |     |
| --- | --- | --- |
| application/zip | video/mp4 | audio/mpeg |
| text/html | video/H264 | font/ttf |
| text/css | video/JPEG | image/jpeg |
| text/javascrip | audio/aac | image/png |