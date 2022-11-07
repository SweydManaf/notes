# Historia dos bancos de dados

### DEC. 50

- Antes dos computadores os dados eram guardados em papel;
- Nessa época a gente preenchia uma ficha, essa ficha preenchida era colocada dentro de uma pasta e essa pasta era armazenada dentro de um arquivo metálico;
- Os três componentes: a ficha, a pasta e o arquivo. Têm nomes específicos na área de tecnologia da informação.
    - As **fichas** são tratadas como **registros**.
    - As **pastas** como **tabelas**.
    - Os **armários** como **arquivos.**
- O grande desafio do final da década de 50 e inicio da década de 60 foi digitalizar o grande acumulo de todos esses dados (papelada). Isso porque a computação já havia começado a ganhar o mundo das empresas.
- O mundo ainda como se armazena os dados era bem arcaico. Basicamente era pegar uma ficha de forma digital e colocar uma após a outra dentro de um arquivo sequencial. Isso porque os arquivos antigamente eram guardados em fitas magnéticas ou cartões perfurados e esses meios de armazenamento eram sequencias. Por conta dessa característica da sequencia dos registros esse tipo de armazenamento ficou conhecido como **Arquivos Sequenciais**.
- Como o amanhã é sempre melhor depois das fitas surgiram os discos, disquetes e HD. E esses tipos de armazenamento armazenavam os dados de forma direta e não sequencial. Você não precisava ler o único do disco para ler a metade dele, você poderia ir direto. Nesses mecanismos de armazenamento era possível guardar todos os registros e manter dentro de uma espécie de tabela, índices ou numerações (chaves identificadoras ). A partir daí era só buscar o índice e cair **direto no arquivo**.

### DEC.60

- Na década de 60 o **Departamento de Defesa dos Estados Unidos** tinha como uma das tarefas criar uma maneira de armazenar dados de maneira mais segura e inteligente;
- O **Departamento de Defesa dos Estados Unidos** criou um evento chamado **CODASYL**. CODASYL foi um grande encontro que reuniu militares, empresas e universidades, lá foram discutidas várias tecnologias emergentes e tallz. Dessa conversa surgiu uma das linguagens mais valiosas da história o **COBOL**.
- Além da linguagem **COBOL** no CODASYL foi discutido o surgimento de uma nova tecnologia, **Banco de Dados**.
- E no modelo criado na década de 60  o Banco de Dados até hoje é composto por quatro partes:
    - A Base de Dados;
    - Sistema Gerenciador (SGBD) ou (DMS);
    - Linguagem de exploração;
    - Programa adicionais.
- A IBM foi uma empresa que teve muita importância nos estudos dos Banco de Dados. A primeira coisa que a IBM propôs foi a criação de dados hierárquicos, basicamente os dados iam ser armazenados e iriam ter uma hierarquia (pai, filho), esse modelo ficou conhecido como modo **modelo hierárquico**.
- Além do modelo hierárquico foi proposto um outro modelo, nele os dados quem é superior e quem é inferior, eles seriam ligados numa forma de rede inteligente, isso trouxe o **modelo em rede**.

### **DEC. 70**

Nesse período um dos pesquisadores da IBM o Edgar F. Codd propôs um novo modelo. Nesse novo paradigma os dados eles seriam armazenados invés de hierarquias ou ligações em redes eles teriam relações mais intrínsecas, eles teriam relação. E foi dos estudos de Codd que surgiu o **Modelo Relacional**.

## SQL

O primeiro nome dessa linguagem de exploração foi **Structured English Query Language** (SEQUEL). Não demorou muito para esse nome mudar para **Strutured Query Language** (**SQL**).

Então basicamente SQL é uma linguagem de consulta, é uma linguagem onde você vai poder dar comandos, dar instruções ao meio ambiente do banco de dados e aí ele vai retornar uma Query - uma solicitação ou uma resposta a uma solicitação; 

A ideia inicial era que a linguagem SQL fosse universal, você teria uma única linguagem SQL e todos os bancos de dados suportariam comando nessa linguagem. 

Só que com o andar do tempo cada um começou a dar uma apimentada no SQL criando assim uma despadronização pois existiam vários SQL's com comandos diferentes, portanto vieram os órgãos de organização para resolver a bagunça. Basicamente os órgãos americanos ANSI e ISO resolveram entrar na briga  e padronizaram.

A partir daí surgiram vários tipos de banco de dados:

- Pagos:
    - Oracle;
    - IBM com DB2;
    - dBASE (muito velho);
    - Microsoft com a SQL Server.
- Gratuitos:
    - MySQL;
    - MariaDB (fork do MySQL - 2015);
    - FireBird;
    - PostgressSQL.