# Como conectar MongoDB com Spring boot?

Para conectar o MongoDB com o Spring Boot, é necessário seguir os seguintes passos:

- Instale o servidor MongoDB na sua máquina ou crie uma conta no Mongo Atlas e crie um cluster. baixe e instale a última versão disponível em    https://www.mongodb.com/download-center/community.

- Adicione a dependência do Spring Data MongoDB ao seu projeto através do arquivo pom.xml (caso esteja usando Maven) ou do arquivo build.gradle (caso esteja usando Gradle).

- Configure a conexão com o MongoDB no arquivo application.properties, adicionando as seguintes propriedades:

Para conectar o MongoDB com Spring Boot, primeiro é preciso instalar o servidor MongoDB na sua máquina, se ainda não o tiver instalado. Você pode baixar o MongoDB no site oficial e seguir as instruções de instalação. 

Após instalar o servidor MongoDB, é preciso adicionar a dependência do Spring Data MongoDB ao seu projeto. Isso pode ser feito adicionando a seguinte linha ao arquivo pom.xml (caso esteja usando Maven) ou build.gradle (caso esteja usando Gradle):

Maven:

```
<dependency>
  <groupId>org.springframework.boot</groupId>
  <artifactId>spring-boot-starter-data-mongodb</artifactId>
</dependency>
```

Gradle:

```
compile 'org.springframework.boot:spring-boot-starter-data-mongodb'
```

Em seguida, é preciso adicionar as configurações de conexão com o MongoDB no arquivo application.properties ou application.yml do seu projeto. As configurações incluem a URL de conexão, nome de usuário e senha (se for o caso). Por exemplo:

```
spring.data.mongodb.host=localhost
spring.data.mongodb.port=27017
spring.data.mongodb.database=nome_do_banco
spring.data.mongodb.username=admin
spring.data.mongodb.password=secret

```
