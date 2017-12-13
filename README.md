# gw4eTutorial
Projeto desenvolvido para a cadeira de Testes de Validação(IF1009)

GW4E é uma ferramente open source para testes baseados em modelo, mais conhecidos como MBT(Model Based Tests). Além das funcionalidades essenciais do Graphicwalker, o GW4E permite que outras funcionalidades sejam utilizadas, diretamente no Eclipse.  

# Prerequisitos

Para utilizar o GW4E, é necessário que os seguintes components estejam previamente instalados:

- Eclipse IDE;
- Maven.

# Instalando o GW4E
  # Criando um repositório M2:
  - Inicie o Eclipse IDE;
  - Vá até a aba *Windows>Preferences*(Win/Linux) ou *Eclipse>Preferências*(Mac);
  - Selecione *Java>Build Path>Classpath Variables*;
  - Clique no botão *New*, e defina uma nova variável M2_REPO e aponte para o repositório Maven local. 
  # Instalando o GraphicWalker no repositório Maven:
  - Faça o download do *GraphicWalker Client Library*, através do link https://github.com/gw4e/gw4e.project/raw/gw-repo-4.0.0/graphwalker-cli-4.0.0-SNAPSHOT.jar;
  - Execute este comando no terminal: mvn install:install-file -Dfile=LOCAL-DO-DOWNLOAD-DO-JAR/graphwalker-cli-4.0.0-SNAPSHOT.jar -DgroupId=org.graphwalker -DartifactId=graphwalker-cli -Dversion=4.0.0-SNAPSHOT
