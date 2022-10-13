# Resumo

- A sigla **CSS** significa **Cascading Style Sheets.**
    
- Ao configurar os estilos com a técnica inline, as propriedades CSS são colocadas dentro da própria tag HTML, em um parâmetro chamado style.
    
- Para usar a técnica de estilos internos, a tag `<style>` deve estar dentro da área `<head>` do seu documento HTML.
    
- Em um mesmo documento HTML, utilizamos as técnicas de CSS interno e CSS inline para mudar a cor de um elemento e acabamos usando duas cores diferentes. As configurações duplicadas feitas nas CSS inline vão prevalecer.
    
- Para utilizar estilos CSS externos, devemos usar a tag `<link>` no documento HTML para fazer o carregamento.
    
- A tag de carga de estilos externos deve estar dentro da área `<head>` no documento.
    
- Para que os arquivos externos em CSS tenham compatibilidade com caracteres acentuados, devemos adicionar a regra:```css
    @charset "UTF-8";
    
- No fim das contas, vamos dar preferência à técnica de **CSS externos** sempre que for possível e vamos tentar evitar a técnica de **CSS inline** em nossos sites.