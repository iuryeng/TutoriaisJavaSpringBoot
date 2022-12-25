# Como conectar MongoDB com Spring boot?

Para conectar o MongoDB com o Spring Boot, é necessário seguir os seguintes passos:

1. Instale o servidor MongoDB na sua máquina ou crie uma conta no Mongo Atlas e crie um cluster. Instale o servidor MongoDB na sua máquina ou crie uma conta no Mongo Atlas e crie um cluster. 

2. Adicione a dependência do Spring Data MongoDB ao seu projeto através do arquivo pom.xml (caso esteja usando Maven) ou do arquivo build.gradle (caso esteja usando Gradle).

3. Configure a conexão com o MongoDB no arquivo application.properties, adicionando as seguintes propriedades:

## Passo 1: 
Para conectar o MongoDB com Spring Boot, primeiro é preciso instalar o servidor MongoDB na sua máquina, se ainda não o tiver instalado. Você pode baixar o MongoDB no site oficial e seguir as instruções de instalação. baixe e instale a última versão disponível em https://www.mongodb.com/download-center/community. 
Após a instalção, inicie o servidor MongoDB executando o comando `mongod` em seu terminal.

## Passo 2: 
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
## Passo 3:

Em seguida, é preciso adicionar as configurações de conexão com o MongoDB no arquivo application.properties ou application.yml do seu projeto. As configurações incluem a URL de conexão, nome de usuário e senha (se for o caso). 

- _spring.data.mongodb.host_: Especifica o host (endereço IP ou nome de domínio) do servidor MongoDB. Se o servidor estiver sendo executado localmente na sua máquina, o valor padrão é "localhost".

- _spring.data.mongodb.port_: Especifica a porta que o servidor MongoDB está escutando. O valor padrão é 27017.

- _spring.data.mongodb.database_: Especifica o nome da base de dados a ser utilizada no MongoDB. É necessário criar a base de dados antes de tentar se conectar a ela.

- _spring.data.mongodb.username_: Especifica o nome de usuário para autenticação no servidor MongoDB. Isso é opcional e só é necessário se o servidor tiver sido configurado para exigir autenticação.

- _spring.data.mongodb.password_: Especifica a senha para autenticação no servidor MongoDB. Isso é opcional e só é necessário se o servidor tiver sido configurado para exigir autenticação e um nome de usuário tiver sido especificado.

- _spring.data.mongodb.authentication-database_: especifica o nome do banco de dados de autenticação para autenticação no servidor MongoDB. Este campo é opcional e só é necessário se o servidor MongoDB estiver configurado para exigir autenticação e o nome do banco de dados de autenticação for diferente do banco de dados especificado em 

Por exemplo:

```
spring.data.mongodb.host=localhost
spring.data.mongodb.port=27017
spring.data.mongodb.database=nome_do_banco
spring.data.mongodb.username=admin
spring.data.mongodb.password=secret
spring.data.mongodb.authentication-database=admin

```

Se você estiver usando o MongoDB Atlas, a URL de conexão será um pouco diferente, como mostrado abaixo:

```
spring.data.mongodb.uri=mongodb+srv://username:password@cluster0.mongodb.net/test

```

Com essas configurações, o Spring Boot já estará conectado ao MongoDB e pronto para persistir e recuperar dados. É possível testar a conexão criando uma classe de teste como a seguir:


```
@SpringBootTest
class ConexaoMongodbApplicationTests {

  @Autowired
  private MongoTemplate mongoTemplate;

  @Test
  void contextLoads() {
    assertNotNull(mongoTemplate);
  }

}


```


