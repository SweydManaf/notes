cap.08 - Formatações de texto

# RESUMO SOBRE FORMATAÇÕES DE TEXTOS EM HTML5

> Semântica é o significado dos vocábulos, por oposição à sua forma.
> Sendo assim o HTML5 é focado no significado das coisas, na semântica. E as CSS são responsáveis pela forma.

- A versão anterior da linguagem, a HTML4 era bastante focada na forma do conteúdo. Já a versão HTML5 já fica mais voltada para o significado.
    
- A HTML5 chegou com a proposta de definir as chamadas tags semânticas, onde cada instrução passa a ter um significado, não apenas uma forma.
    
- No lugar da tag `<b>` para **negrito** use a `<strong>`
    
- No lugar da tag `<i>` para *itálico* use a tag `<em>`
    
- A tag `<big>` e `<small>` servem para texto '<big>grande</big>' e texto '<small>pequeno</small>' respectivamente.
    
- Para <mark>marcar</mark> uma parte do texto usamos a tag `<mark>` por padrão o fundo é amarelo, podemos alterar dando o parâmetro `bg`, que só funcionará pra essa ocasião.
    
- Quando for para <ins>sublinhar</ins> um texto no sentido de chamar atenção para ele, deixamos de usar o antigo `<u>` e passamos a usar o novo `<ins>`.
    
- Quando for para colocar um ~texto deletado~ usamos a tag `<del>` que significa que o texto está ali mas deve ser desconsiderado.
    
- Para criar um texto sobrescrito como (x<sup>2</sup>) usamos a tag `<sup>`.
    
- Para criar um texto subscrito como (H<sub>2</sub>O) usamos a tag `<sub>`.
    
- Em HTML5 podemos criar citações utilizando a tag `<blockquote>`, incluindo o parâmetro `cite` para indicar o link para o conteúdo original da citação.
    
- Quando quisermos fazer uma abreviação usamos a tag `<abbr>` com o parâmetro title dando o significado da sigla.
    
- Para inverter uma palavra ou frase devemos usar a tag `<bdo>` com o parâmetro dir configurado para o valor rtl.
    
- Quando quisermos inserir um código de uma linguagem usamos a tag `<code>` se quisermos formatar colocamos dentro da tag `<pre>`
    

## Algumas tag obsoletas

- basefont
- big
- blink
- center
- font
- marquee
- multicol
- nobr
- spacer
- tt