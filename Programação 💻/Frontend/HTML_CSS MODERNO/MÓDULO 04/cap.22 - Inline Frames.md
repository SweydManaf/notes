# Inline Frames

## Entendendo quadros em linha

Um iframe é basicamente uma “janela aberta” dentro da nossa página para apresentar o conteúdo de outras páginas. Esse é um recurso bem antigo, presente desde as versões anteriores da HTML, mas que até hoje são utilizados por alguns sites, o que causa muita discussão em relação a segurança.

### Criando um iframe

```html
<p>Acessando o site do 
        <!-- Tamanho padrão 300x150-->

        <iframe src="https://www.cursoemvideo.com" frameborder="0" height="500">
        Curso em Video para aprender a programar.
        </iframe>
</p>
```

Note que acrescentamos uma frase entre &lt;iframe&gt; e &lt;/iframe&gt; para que seja exibida caso o navegador do usuário não suporte o uso desse tipo de recurso. Alguns celulares mais antigos possuem navegadores que bloqueiam a exibição de quadros por questões relacionadas ao tamanho da tela, uso de memória e até segurança.

### Gerando conteúdo dentro do iframe

No lugar de usar o parâmetro `src` para indicar a origem (source) do conteúdo de um quadro, podemos usar o parâmetro `srcdoc` para criar um conteúdo simples estaticamente dentro do `iframe`.

### Direcionando novo conteúdo para um iframe

Para adicionar um novo conteúdo para o `iframe` dinamicamente, adicionamos o parâmetro `name` no `iframe` e com a tag `a` adicionamos o parâmetro `target` que vai referenciar o nosso `iframe`.

### Problemas com mecanismos de busca

Segundo o próprio Google, podem acontecer problemas com a indexação de conteúdos contidos dentro de iframes e talvez não haja uma boa relação entre o que está fora (na página principal) e o que está dentro (na parte interna do iframe).

### Tornando as coisas mais seguras

Cientes dos problemas que um `iframe` mal configurado pode trazer, a HTML5 implementou o novo recurso de sandbox. Uma

caixa de areia (sandbox) é um ambiente controlado que permite exibir outros sites para seu visitante sem que ele possa “tomar

controle” do site principal e aos dados do visitante. Quando habilitamos a sandbox em nosso iframe, automaticamente o site que está

dentro do quadro perde algumas funcionalidades, dentre elas:

- Não pode mais enviar dados de formulários
- Não pode mais executar scripts
- Desabilita todo tipo de API, janelas modais e popups
- Desabilita todo tipo de plugin com &lt;embed&gt;, &lt;object&gt;, &lt;applet&gt;
- Evita que o site dentro do iframe assuma a navegação top level do navegador
- Bloqueia recursos como autoplay e foco automático em elementos de formulário

### Definindo a política de referência

Permite que os sites não criem coockicookieses ou histórico de navegação do nosso iframes.

### Exemplos de uso de iframes práticos

- Google Maps
- Google Docs
- Vimeo
- YouTube