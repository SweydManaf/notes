# Como surgiu?

- O MySQL surgiu em **1994** na Suécia pelo **Michael Widenius** e **David Axmark**;
- Michael e David decidem criar um modelo gratuito e Open-Soure de banco de dados baseada no modelo relacional, surgi então o MySQL;
- Em 2007 a empresa **Sun Microsystems** comprou o MySQL;
- Em 2009 a **Sun Microsystems** foi comprada pela **Oracle** e deixou de existir;
- Por conta da Oracle ter adquirido o MySQL o Michael e David insatisfeitos abandonaram o projeto MySQL e criaram o projeto **MariaDB;**
- O projeto MariaDB é um fork do MySQL ou seja o MariaDB inicialmente era igual ao MySQL no entanto a partir do fork para frente foram se divergindo com ideias "diferentes";
- Empresas que usam o MySQL: NASA, Google, Wikipédia, Adobe, CISCO, eBay, empresas de comunicação...

# Comandos específicos

Por definição o MySQL possui dentro dele algumas instruções que se caracterizam como linguagens do tipo, por exemplo:

- - **DDL** (linguagem de definição) - aqui você vai definir; por exemplo criar um banco de dados, criar uma tabela, alterar esse banco de dados. Qualquer comando de definição da estrutura da base de dados é mantida dentro do MySQL pela porção DDL.
    - **DML** (porção de manipulação) - aqui você vai poder, incluir novos dados, excluir dados, manipular dados de qualquer maneira (alterar a composição deles).
    - **DQM** (porção de solicitações) - aqui você vai poder fazer um *select ,* qualquer solicitação que você vai precisar a DQL vai ser a responsável;
    - **DCL** (porção de controle) -  aqui você pode definir que usuários podem acessar o seu banco, que tipo de acesso ele vai poder fazer, que tipo de comandos ele vai poder executar e muito mais.
    - **DTL** (porção de transações) - transação é qualquer solicitação que pode ser feita a um banco de dados te atendendo da melhor maneira possível seguindo os 4 princípios da DICA, que são:
        - **D** \- Durabilidade: todo dado deve permanecer 'desse' jeito enquanto eu quiser;
        - **I** \- Isolamento: se eu tiver duas transações feitas ao mesmo tempo elas devem ser executadas sem uma interferir na outra, devem ser isoladas;
        - **C** \- Consistência: toda transação entre bancos de dados tem que levar de um estado consistente a outro estado consistente, se tudo estava OK antes tem que continuar OK.
        - **A** \- Atomicidade: toda transação tem que ser atômica, ou toda ela acontece ou nada acontece.

## Configurando o ambiente MySQL com WAMP

1.  Baixar e instalar o MySQL Workbench a partir do site oficial: [www.mysql.com](http://www.mysql.com);
2.  Baixar o WAMP a partir do site oficial: [www.wampserver.com](http://www.wampserver.com);
3.  Certificar-se que todos os pré-requisitos estão disponíveis a partir do link na instalação;
4.  Instalar o WAMP Server;
5.  Executar o Wamp Server
6.  Iniciar o Mysql console. Se o usuário for **root **caso do Windows a senha será vazia -> Enter;
7.  Por fim iniciar o MySQL Workbench.