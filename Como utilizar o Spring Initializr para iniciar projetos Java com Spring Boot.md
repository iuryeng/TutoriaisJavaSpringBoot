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

Agora, vamos adicionar as dependências do projeto. Na seção "Dependencies", você pode pesquisar por dependências específicas e adicioná-las ao projeto clicando no botão "ADD DEPENDENCES" ou clicando CTR + B. Por exemplo, se você precisar de suporte a banco de dados, basta pesquisar por "Spring Data MongoDB" e adicionar a dependência ao projeto. Você pode adicionar, por exemplo, dependências basicas de uma API Rest. ( Verifique em:  Exemplos de dependencias para iniciar um projeto de API Rest )

![image](https://user-images.githubusercontent.com/38250160/209450526-78ba5e2f-578d-4aa3-9bea-1b61cc0d2b50.png)


Quando terminar de adicionar as dependências, clique em "Generate Project". Isso fará com que o Spring Initializr gere o projeto com as dependências e configurações selecionadas. O projeto será baixado como um arquivo .zip, que você pode descompactar e importar para a sua IDE de preferência.

Agora, você já tem um projeto Spring Boot pronto para começar a desenvolver sua aplicação. Aproveite o Spring Initializr como uma ferramenta útil para iniciar rapidamente

# Exemplos de dependencias para iniciar um projeto de API Rest:

Dependencias iniciais usadas no projeto Spring Initializr:

- Spring Web: Essa dependência é utilizada para desenvolver aplicações web com o Spring. Ela inclui os componentes necessários para criar controllers, gerenciar requisições HTTP e configurar o mapeamento de rotas.

- Lombok: Essa biblioteca é utilizada para simplificar a escrita de código Java, fornecendo anotações que geram automaticamente código boilerplate como getters, setters e construtores. Ela é especialmente útil para projetos com muitas entidades e evita a repetição de código.

- Spring Data MongoDB: Essa dependência fornece integração com o banco de dados MongoDB, permitindo a criação de repositórios que facilitam o acesso aos dados. Ela também inclui o suporte para o uso de consultas personalizadas com a linguagem de consultas do MongoDB (query language).

- Springfox Swagger: Essa biblioteca é utilizada para gerar documentação da API em formato Swagger, o que facilita o entendimento e o teste das rotas da API pelos desenvolvedores. Ela também gera uma interface web para visualização da documentação.

- Springfox Swagger UI: Essa dependência é utilizada para fornecer a interface web de visualização da documentação gerada pelo Springfox Swagger. Ela é importante para que os desenvolvedores possam visualizar e testar as rotas da API de forma mais intuitiva.


# Referência 

https://docs.spring.io/initializr/docs/current/reference/html/
