# gw4eTutorial
Projeto desenvolvido para a cadeira de Testes de Validação(IF1009)
Equipe: - Robson Jr.
        - Ricardo Rodrigues
        - Sidney Felipe

GW4E é uma ferramente open source para testes baseados em modelo, mais conhecidos como MBT(Model Based Tests). Além das funcionalidades essenciais do Graphicwalker, o GW4E permite que outras funcionalidades sejam utilizadas, diretamente no Eclipse.  

# Prerequisitos

Para utilizar o GW4E, é necessário que os seguintes components estejam previamente instalados:

- Eclipse IDE;
- Maven;
- Xtext;
- GEF.

# Instalando o GW4E
  # Criando um repositório M2:
  - Inicie o Eclipse IDE;
  - Vá até a aba *Windows>Preferences*(Win/Linux) ou *Eclipse>Preferências*(Mac);
  - Selecione *Java>Build Path>Classpath Variables*;
  - Clique no botão *New*, e defina uma nova variável M2_REPO e aponte para o repositório Maven local. 
  # Instalando o GraphicWalker no repositório Maven:
  - Faça o download do *GraphicWalker Client Library*, através do link https://github.com/gw4e/gw4e.project/raw/gw-repo-4.0.0/graphwalker-cli-4.0.0-SNAPSHOT.jar;
  - Execute este comando no terminal: mvn install:install-file -Dfile=LOCAL-DO-DOWNLOAD-DO-JAR/graphwalker-cli-4.0.0-SNAPSHOT.jar -DgroupId=org.graphwalker -DartifactId=graphwalker-cli -Dversion=4.0.0-SNAPSHOT (É necessário configurar a variável mvn dentro do PATH do Windows previamente)
  - Desta maneira, o arquivo cli será adicionado no arquivo de dependências do projeto, permitindo sua utilização. 

# Instalando o Xtext
  - Dentro do Eclipse IDE, vá até a aba *Help*, e clique na opção *Install New Software*;
  - Clique em Add, e nomeie o novo endereço como XText;
  - Adicione o endereço   http://download.eclipse.org/modeling/tmf/xtext/updates/composite/releases/ na seção Location. 
  - Selecione a dependência XText. 
 
 # Instalando o GEF
  - Dentro do Eclipse IDE, vá até a aba *Help*, e clique na opção *Install New Software*;
  - Clique em Add, e nomeie o novo endereço como GEF;
  - Adicione o endereço  http://download.eclipse.org/tools/gef/gef4/updates/releases na seção Location.
  - Selecione todas as dependências relacionadas ao GEF.
  
 # Instalando o GW4E
  - No Eclipse IDE, vá até a aba *Help*, e clique na opção *Install New Software;*
  - Clique em Add, e nomeie o novo endereço como GW4E;
  - Adicione o endereço  https://github.com/gw4e/gw4e.project/raw/p2repo-4.0.0/repository na seleção Location.
  - Selecione a opção *GraphicWalker Integration for Eclipse*.
  - Clique em Next 2 vezes, selecione *GraphicWalker Integration for Eclipse* e leia os detalhes. 
  - Após isso, siga as instruções do assistente de instalação. 
  
 # Utilizando o GW4E
 
 O GW4E permite a criação de modelos gráficos, que podem ser transformados em testes manuais, testes funcionais, smoke tests, ou testes de estabilidade, e transformá-los em testes do JUnit, ou em modelos de testes manuais em .xlsl. 
  
 # Gerando Modelos no GW4E
 - Para iniciar um projeto GW4E, vá até a opção *Window>Perspective>Open Perspective>Other* e selecione a opçao GW4E Perspective;
 - Clique em *File>New>GW4E Project*;
 - Dê um nome ao seu projeto e clique em next;
 - Clique em *Next* novamente;
 - Selecione o tipo de modelo desejado (Modelo vazio, modelo simples, scripted model, e modelos compartilhados);
 - Clique em *Next*;
 - Em seguida em *Finish*;
 
 # Utilizando o GW4E

 A base para criar modelos é bastante intuitiva: 
 - O círculo verde indica um evento de início;
 - Os retângulos azuis, chamados de *vertex* indicam estados do programa;
 - As linhas, chamadas de *edges* indicam ações, que servirão de transição entre os estados do programa em teste;
 
 Cada objeto gráfico permite que seja adicionado uma descrição, bem como propriedades que podem ser atribuídas pelo usuário. Para fazer isto, basta clicar no objeto, e selecionar a aba *Properties*, próximo do terminal do EClipse IDE, onde os campos de nome, descrição/propriedade e serão apresentado. 
 
 Para adicionar um elemento, basta arrastá-lo até o dashboard, e nomeá-lo.
 
 # Gerando testes JUnit com o GW4E
 
 Para converter os modelos em testes JUnit:
 - Clique com o botão direito do mouse sobre o projeto, e selecione a opção *GW4E*, e *Convert To* em seguida;
 - Em seguida escolha a opção *Java Test Based*, e clique em *Next*;
 - Selecione *GraphicWalker Class Based Test*, e em seguida, na opção abaixo, que irá definir o elemento de início do teste;
 - Clique em *Next*, e em seguida, selecione o tipo de teste JUnit desejado(Smoke Test, Functionality Test, Stability Test);
 - Após clicar em *Next*, clique em *Finish*, e o arquivo JUnit será gerado. 
 
 Cada *vertex* e *edge* serão criados, e o usuário poderá adicionar em cada um os atributos necessários, bem como a parte dos testes que foram escolhidos na hora de fazer a conversão. 
 
 Para executá-lo, basta selecionar a opção *Run As*, e clicar a opção *JUnit test*.
 
 # Gerando testes manuais com o GW4E
 
 Para gerar e exportar arquivos de testes manuais:
 - Selecione a opção ao lado do botão *Run* no topo do Eclipse IDE;
 - Selecione a opção *Run configurations*;
 - Na aba de opções à esquerda, selecione a opção *GraphicWalker Manual Test Launcher*, e clique no ícone "New", logo acima da lista;
 - Clique no botão *Browse*, na opção Project, e selecione o projeto atual;
 - Clique no botão *Browse*, na opção GraphModel, e selecione o projeto atual;
 - Na opção *Path Generator*, selecion a primeira opção *(random(edge_coverage(100)))*;
 - Clique em *Apply*, e depois em *Run*;
 - Após a abertura do assistente, clique em *Next*;
 - Os passos do modelo serão apresentados, e logo abaixo da descrição as opções de falhar o passo aparecerão, podendo ser selecionadas ou não;
 - Clique em *Next* até que a página de Resumo da Execução apareça; 
 - Clique em *Next* mais uma vez;
 - Selecione a opção *Export as a Test Template*;
 - Selecione a segunda caixa de texto e escreva um nome para o arquivo, no formato *meuArquivo.xlsx*;
 - Escreva um título logo abaixo, e em seguida, insira o Id do teste;
 - Insira abaixo um nome de component, e defina a prioridade do caso de teste, clicando em *Finish* logo após. 
 - Um arquivo .xlsx será gerado, contendo toda a execução do caso de teste manual. 
