# Formatação de texto

## Elemento `<i>`

Ela indica a utilização desse elemento para definir **nomes científicos**, **termos técnicos**, **expressões idiomáticas** em outras línguas, **transliterações**, **pensamentos**. Normalmente, os navegadores definem o `i` como i**nline-level element** e exibem o seu conteúdo em itálico.

## Elemento `<b>`

Ela indica, por exemplo, a utilização desse elemento para definir as **palavras chave do resumo de um documento** e o **nome do produto em texto de avaliação**. Normalmente, os navegadores definem o `b` como **inline-level element** e exibem o conteúdo em negrito.

## Definições `<dfn>`

Podemos inserir definições em um documento HTML com o elemento **dfn**. Por padrão, esse elemento é exibido como elemento de linha. Normalmente, os navegadores definem o **dfn** como **inline-level element.**

## Data e hora

O elemento `time` permite que **datas** e **horários** sejam definidos em um documento HTML. Há duas formas de utilizar esse elemento. A primeira é definir a data e o horário desejado no conteúdo do elemento time. A segunda é definir a data e o horário desejado no valor do atributo datetime. Nessas duas opções, as datas e os horários devem ser escritos seguindo o formato definido na especificação da linguagem HTML ( http://www.w3.org/TR/html5/text-level-semantics.html#the-time-element ). Quando utilizamos o atributo `datetime`, o conteúdo do elemento time não precisa seguir um formato específico. Normalmente, os navegadores definem o time como **inline-level element**.

```html
<ul>
    <li><time>2010-8</time></li>
    <li><time>1984-10-30</time></li>
    <li><time>12-25</time></li>
    <li><time>09:00</time></li>
    <li><time>2013-12-25 23:59</time></li>
    <li><time datetime="2010-08">Fundação da K19</time></li>
    <li><time datetime="1984-10-30">Aniversário do Rafael</time></li>
</ul>
```