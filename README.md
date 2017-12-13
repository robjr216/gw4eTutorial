# gw4eTutorial
Projeto desenvolvido para a cadeira de Testes de Validação(IF1009)

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
