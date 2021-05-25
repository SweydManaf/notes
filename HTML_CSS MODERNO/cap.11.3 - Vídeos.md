cap.11.3 - Vídeos

# Vídeos

Para inserir um vídeo em nosso site, podemos utilizar a nova tag `<video>` da HTML5, caso o arquivo esteja hospedado no nosso próprio servidor. 

```html
<video width=""600" poster="thumb.jpg" controls autoplay>
    <source src="meu-video.webm" type="video/webm">
    <source src="meu-video.mp4" type="video/mp4">
    <source src="meu-video.ogv" type="video/ogg">
    <p>Infelizmente seu navegador não conseguiu carregar o vídeo.</p>
</video>
```

Antes de mais nada, vamos criar a tag `<video>` e configurar alguns atributos importantes:

‣ **width** vai indicar a largura que o vídeo vai ter na tela. Nesse exemplo, 600px.

‣ **poster** configura uma imagem que vai aparecer como uma capa, enquanto o visitante não aperta o play para reproduzir o vídeo

‣ **controls** vai configurar se os controles do vídeo vão aparecer na parte inferior da mídia. Por padrão, os controles não aparecerão, mas basta colocar a palavra **controls** na tag `<video>`.

‣ **autoplay** diz para o navegador se o vídeo vai começar a tocar automaticamente, assim que a página for carregada.

## E os formatos?

|     |     |
| --- | --- |
| Navegador | Arquivos compatíveis |
| Microsoft Edge | .mp4 .m4v |
| Apple Safari | .mp4 .m4v |
| Google Chrome | .mp4 .m4v .webm .ogv |
| Mozilla Firefox | .webm .ogv |
| Opera | .webm .ogv |

## Hospedagem local

Quando colocamos vídeos no nosso próprio servidor, podemos passar por problemas com alto consumo de banda, site lento e incompatibilidades com alguns navegadores por conta dos codecs. E geralmente só percebemos esses problemas quando colocamos nosso projeto no ar e lançamos oficialmente.

Vamos fazer uma conta simples: um vídeo simples, com poucos minutos, em formato mp4 com codec padrão deve ocupar uns 150MB com facilidade. Agora imagine que você lance seu site e 200 visitantes (um número super possível) acessem seu site e reproduzam o vídeo. Pronto, você acabou de utilizar 29GB de tráfego! Imagine o quanto isso pode deixar seu site lento ou consumir sua franquia de hospedagem, caso não seja ilimitada.

## Hospedagem externa

o YouTube ou o Vimeo! Esses são serviços para a hospedagem de vídeos que vai evitar consumir nossos próprios recursos de host contratado. Cada um tem suas vantagens e desvantagens:

- **YouTube** é o serviço de hospedagem de vídeos mais popular do mundo e é gerenciado pelo Google. Sua principal vantagem é que seus servidores são ultra rápidos. Por outro lado, a ideia do Google é deixar todos os vídeos públicos e disponíveis, o que pode ser uma dor de cabeça caso você queira limitar quem vai ter acesso a determinado vídeo (uma escola online, por exemplo, onde queremos que apenas os alunos matriculados possam assistir).

- **Vimeo** resolve o problema que apontamos anteriormente. Ele permite limitar quem vai poder ver o vídeo, o que é especialmente vantajoso para quem quer criar produtos em forma de vídeo, entregues por demanda dentro de um site personalizado. Como desvantagens desse serviço, ele é pago por uma taxa anual e seus algoritmos não são tão eficientes quanto os do YouTube, logo os vídeos apresentam pequenos travamentos às vezes.

Para incorporar vídeos que você subiu no **YouTube** ou **Vimeo**, existem recursos que te dão o código pronto em HTML5.