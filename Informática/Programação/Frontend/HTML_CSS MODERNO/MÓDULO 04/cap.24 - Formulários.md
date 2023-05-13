# Formulários
## Diferença entre os metodos post e get
Em primeiro lugar, podemos usar GET em um formulário contanto que:
- Os dados a serem enviados não sejam sensíveis, como endereços, números de documentos, senhas, etc.
- Tivermos formulários simples e que possam ser compartilhados facilmente através de uma URL. Por exemplo, o Google usa GET no seu formulário, pois você pode enviar um link para qualquer pessoa, já com a ação da busca embutida, como em http://google.com.br/search?q=Gustavo+Guanabara
- Os dados a serem enviados nunca ultrapassem 3000 bytes.
- Não contenha envio de arquivos como imagens (i.e. fotos de perfil), arquivos PDF, etc.

Já o método POST é mais recomendado para casos em que:
- Não queremos que os dados apareçam explicitamente na URL do navegador.
- Capturamos dados como senhas, documentos e outro tipo de dado sensível.
- Precisamos enviar muitos dados (acima de 3000 bytes ~ sem limites).
- Precisamos enviar imagens ou outros tipos de arquivos.

## Usar name ou id: qual é o mais útil e recomendado?

Outra dúvida bem comum entre os meus alunos é em relação ao uso dos atributos **name** e **id** em elementos de formulários. Pode parecer que os dois servem para identificar os elementos e que o uso de ambos é algo desnecessário, mas não é.

Vamos dar uma olhada na linha do exercício que estamos criando:
```
<input type="text" name="fnome" id="camponome">
```

De forma objetiva, use sempre os dois em todos os seus elementos, pois cada um terá sua utilidade específica.
O **name** será bem útil durante o envio dos dados do formulário, independente do método escolhido para enviá-los. É ele que aparece na URL (ao usar GET) e no corpo do HTTP request (ao usar POST). É também através do name escolhido que vamos nos referenciar quando for a hora de programar o arquivo em PHP que vai receber esses dados.

Já o id será muito útil para fazer a ligação com o \<label\> (sempre use labels, por favor) e também será referenciado nos casos em que quisermos tratar esses dados usando JavaScript para realizar qualquer ação, como por exemplo, fazer validação
local dos campos antes de enviá-los.