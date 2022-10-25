---
title: cap.3.2. Transição
updated: 2021-04-06 15:12:18Z
created: 2021-04-06 13:58:19Z
---

# Posicionamento

Como vimos anteriormente, as regras CSS podem ser aplicadas aos elementos HTML de acordo com o estado atual do mesmo. Por exemplo, considere as duas regras CSS a seguir.

```css
div {      
    width: 50px;
    height: 50px;
}
div:hover {
    width: 100px;
    height: 100px;
}
```

De acordo com as duas regras CSS acima, quando o ponteiro do mouse for colocado por cima de um `div`, a largura e a altura desse elemento HTML aumentará instantaneamente de `50px` para `100px`.

## `transition-duration`

A duração das transições pode ser controlada com a propriedade **transition-duration**. 

Os navegadores devem gerar, automaticamente, frames intermediários entre visual inicial e o final. Esses frames devem ser exibidos sequencialmente durante o tempo determinado com a pro priedade transition-duration.

## `transition-delay`

Podemos estabelecer um atraso para o início de uma transição com a propriedade **transition-delay.**

`transition-timing-function`

Os frames que formam uma transição podem ser exibidos com padrões diferentes. Por exemplo, uma transição pode iniciar devagar, no meio acelerar e terminar devagar. O padrão desejado pode ser determinado através da propriedade **transition-timing-function**.

|     |     |
| --- | --- |
| **Valor** | **Descrição** |
| linear | Mesma velocidade do início até o final da transição. Equivale a cubic-bezier(0, 0, 1, 1). |
| ease | O início da transição é lento, o meio é rápido e o final volta a ser lento (padrão). Equivale a cubic-bezier(0.25, 0.1, 0.25, 0.1). |
| ease-in | O início da transição é lento. O meio e o final são rápidos. Equivale a cubic-bezier(0.42, 0, 1, 1) |
| ease-out | O início e o meio da transição são rápidos e o final é lento. Equivale a cubic-bezier(0, 0, 0.58, 1). |
| ease-in-out | Semelhante ao valor **ease ** início e final mais longos. Equivale a cubic-bezier(0.42, 0, 0.58, 1). |
| cubic-bezier(n, n, n, n) | A transição seguirá o padrão definifo pela função cúbica de bezier. |

## `transition-property`

Podemos escolher quais propriedades CSS devem ser consideradas nas transições através da propriedade **transition-property**.