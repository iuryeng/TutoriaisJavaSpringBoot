# Como utilizar o Spring Initializr para iniciar projetos Java com Spring Boot

Bem-vindo ao tutorial sobre o Spring Initializr! Neste tutorial, você aprenderá o que é o Spring Initializr, como utilizá-lo e como ele pode facilitar o processo de criação de aplicações Java Spring Boot. O Spring Initializr é uma ferramenta online que permite a criação de projetos Java Spring Boot de maneira rápida e fácil, fornecendo um modelo básico para que você possa iniciar o desenvolvimento da sua aplicação. Além disso, o Spring Initializr permite a adição de dependências específicas de acordo com as necessidades da sua aplicação, permitindo um maior controle sobre os recursos utilizados. Neste tutorial, você aprenderá a utilizar o Spring Initializr para criar projetos Java Spring Boot e adicionar as dependências necessárias para o seu projeto. Vamos começar!

O tutorial a seguir irá mostrar como utilizar o Spring Initializr para iniciar um projeto Spring Boot com as dependências e configurações necessárias. O Spring Initializr é uma ferramenta online que permite criar rapidamente um projeto Spring Boot com as dependências selecionadas pelo usuário. Além disso, é possível gerar o projeto em diferentes formatos, como Maven ou Gradle, e em diferentes linguagens, como Java ou Kotlin.

Para começar, acesse o site do Spring Initializr em https://start.spring.io/. Na tela inicial, você verá os campos para preencher as informações do projeto.

![image](https://user-images.githubusercontent.com/38250160/209449924-84d509a1-485c-40b5-a890-514a2ad685b2.png)


Abaixo segue uma tabela com os campos do Spring Initializr e suas respectivas descrições:

| Campo                | Descrição                                     |
| -------------------- | ----------------------------------------------| 
|Group	               | Identifica o grupo ao qual o projeto pertence.|
|Artifact              | Nome do projeto.                              |
|Description           | Descrição do projeto.                         |
|Package Name	         | Nome do pacote base do projeto.               |
|Packaging	           | Tipo de embalagem do projeto (war, jar, etc). |
|Java Version	         | Versão do Java a ser utilizada.               |
|Language	             | Linguagem de programação utilizada (Java, Kotlin, etc).  |
|Spring Boot           | Versão do Spring Boot a ser utilizada.                   |
|Dependencies	         | Dependências adicionais que o projeto deve possuir.      |
|Build	               | Ferramenta de build a ser utilizada (Maven, Gradle, etc).|


O campo Group é importante para identificar o grupo ao qual o projeto pertence, enquanto o campo Artifact é o nome do projeto em si. A Description fornece uma descrição do projeto, enquanto o Package Name é o nome do pacote base do projeto. O Packaging indica o tipo de embalagem do projeto (war, jar, etc) e o Java Version especifica a versão do Java a ser utilizada.

O campo Language indica a linguagem de programação utilizada (Java, Kotlin, etc) e o Spring Boot indica a versão do Spring Boot a ser utilizada. As Dependencies são as dependências adicionais que o projeto deve possuir e os Custom Commands são comandos personalizados que podem ser executados durante a inicialização. Por fim, o Build indica a ferramenta de build a ser utilizada (Maven, Gradle, etc).

# Como nomear da melhor forma os campos do Initialzr?

O nome dos campos no Spring Initializr deve ser escolhido de forma a representar de forma clara e precisa o que eles fazem no projeto. Alguns critérios que podem ser considerados na hora de nomear os campos são:

- Evite usar nomes muito genéricos, como "campo1" ou "objeto". 

- Use nomes que descrevam o que o campo representa, como "nomeProduto" ou "dataNascimento".

- Se for preciso usar abreviações, explique-as na documentação do projeto. Por exemplo, ao invés de usar "cpf", pode-se usar "numeroCpf".

- Use nomes em inglês, mesmo que o projeto seja em outra língua. Isso ajuda a padronizar e a facilitar a leitura pelos desenvolvedores que trabalham no projeto.

- Mantenha os nomes curtos e simples, evitando palavras muito longas ou termos técnicos desnecessários.

- Considere o uso de camelCase ou snake_case para separar as palavras dos campos.

Em resumo, o ideal é que os campos do Initializr tenham nomes claros e precisos, que ajudem a entender o que eles fazem no projeto e facilitem a leitura pelos desenvolvedores.

Agora, vamos adicionar as dependências do projeto. Na seção "Dependencies", você pode pesquisar por dependências específicas e adicioná-las ao projeto clicando no botão "ADD DEPENDENCES" ou clicando CTR + B. Por exemplo, se você precisar de suporte a banco de dados, basta pesquisar por "Spring Data MongoDB" e adicionar a dependência ao projeto. Você pode adicionar, por exemplo, dependências basicas de uma API Rest. ( Verifique em:  Exemplos de dependencias para iniciar um projeto de API Rest )

![image](https://user-images.githubusercontent.com/38250160/209450526-78ba5e2f-578d-4aa3-9bea-1b61cc0d2b50.png)


Quando terminar de adicionar as dependências, clique em "Generate Project". Isso fará com que o Spring Initializr gere o projeto com as dependências e configurações selecionadas. O projeto será baixado como um arquivo .zip, que você pode descompactar e importar para a sua IDE de preferência.

![image](https://user-images.githubusercontent.com/38250160/209450942-ad09db7d-9be0-4641-a122-c6d837232221.png)

Agora, você já tem um projeto Spring Boot pronto para começar a desenvolver sua aplicação. Aproveite o Spring Initializr como uma ferramenta útil para iniciar rapidamente.

# Como abrir o projeto criado? 

Para abrir um projeto criado com o Spring Initializr com Maven ou Gradle, siga os seguintes passos:

- Abra o Eclipse ou outra IDE de sua preferência.
- No menu principal, selecione a opção "File" e clique em "Import".
- Na janela de importação, selecione a opção "Existing Maven Projects" ou "Existing Gradle Projects", dependendo do gerenciador de dependências escolhido na criação do projeto.
- Clique em "Next".
- Na próxima tela, selecione o diretório onde o projeto foi salvo. Esse diretório deve conter o arquivo "pom.xml" (Maven) ou "build.gradle" (Gradle).
- Clique em "Finish" para finalizar o processo de importação. O projeto agora estará disponível na sua IDE para ser editado e executado.

Observação: é importante verificar se o Maven ou o Gradle estão corretamente configurados na sua máquina e na sua IDE. Se houver algum problema de configuração, o projeto pode não ser importado corretamente.

# Exemplos de dependencias para iniciar um projeto de API Rest:

Dependencias iniciais usadas no projeto Spring Initializr:

- Spring Web: Essa dependência é utilizada para desenvolver aplicações web com o Spring. Ela inclui os componentes necessários para criar controllers, gerenciar requisições HTTP e configurar o mapeamento de rotas.

- Lombok: Essa biblioteca é utilizada para simplificar a escrita de código Java, fornecendo anotações que geram automaticamente código boilerplate como getters, setters e construtores. Ela é especialmente útil para projetos com muitas entidades e evita a repetição de código.

- Spring Data MongoDB: Essa dependência fornece integração com o banco de dados MongoDB, permitindo a criação de repositórios que facilitam o acesso aos dados. Ela também inclui o suporte para o uso de consultas personalizadas com a linguagem de consultas do MongoDB (query language).


# Por que algumas dependencias não são encontradas no Initializr? 

Existem algumas razões pelas quais algumas dependências podem não estar disponíveis no Spring Initializr:

- A dependência pode ter sido descontinuada ou removida pelos mantenedores.

- A dependência pode não ser compatível com a versão do Spring Boot que você está usando.

- A dependência pode não estar disponível para o tipo de empacotamento que você está usando (por exemplo, WAR ou JAR).

- A dependência pode não ser compatível com o tipo de projeto que você está criando (por exemplo, Maven ou Gradle).

- A dependência pode ter sido adicionada recentemente e ainda não estar disponível no Initializr.

Se você estiver tentando adicionar uma dependência que não está disponível no Initializr, pode ser necessário adicioná-la manualmente ao arquivo de configuração do projeto (por exemplo, pom.xml para projetos Maven ou build.gradle para projetos Gradle).


# Referência 

https://docs.spring.io/initializr/docs/current/reference/html/
