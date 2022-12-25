# Como conectar MongoDB com Spring boot?

Para conectar o MongoDB com o Spring Boot, é necessário seguir os seguintes passos:

1. Instale o servidor MongoDB na sua máquina ou crie uma conta no Mongo Atlas e crie um cluster. Instale o servidor MongoDB na sua máquina ou crie uma conta no Mongo Atlas e crie um cluster. 

2. Adicione a dependência do Spring Data MongoDB ao seu projeto através do arquivo pom.xml (caso esteja usando Maven) ou do arquivo build.gradle (caso esteja usando Gradle).

3. Configure a conexão com o MongoDB no arquivo application.properties

4. Configure o uso do Spring Data MongoDB no projeto.

5. Teste a conexão com o MongoDB 

## Passo 1: 
Para conectar o MongoDB com Spring Boot, primeiro é preciso instalar o servidor MongoDB na sua máquina, se ainda não o tiver instalado. Você pode baixar o MongoDB no site oficial e seguir as instruções de instalação. baixe e instale a última versão disponível em https://www.mongodb.com/download-center/community. 

Se preferir instale a CLI do MongoDb [CLI Atlas](https://www.mongodb.com/try/download/compass).

Se preferi instale o shell do MongoDb [Shell MongoDB](https://www.mongodb.com/try/download/shell)

Vá em : C:\Program Files\MongoDB\Server\6.0>mongod\bin e execute o commando: ```mongod```

O comando "mongod" é usado para iniciar o servidor do MongoDB. Ele deve ser executado no terminal a partir do diretório de instalação do MongoDB. 

Quando o comando mongod é executado, deve aparecer uma mensagem indicando que o servidor do MongoDB está sendo iniciado. Dependendo da configuração do servidor, também pode aparecer mensagens de log com informações sobre o processo de inicialização e o status do servidor. Se o servidor for iniciado com sucesso, a mensagem deve indicar que o servidor está pronto para aceitar conexões. 

![image](https://user-images.githubusercontent.com/38250160/209455679-df315f2f-4fac-440f-b341-b46f54b58805.png)


Se houver algum erro durante o processo de inicialização, a mensagem deve indicar o motivo do erro e fornecer informações adicionais para ajudar a diagnosticar e solucionar o problema.

O comando "mongo" é usado para iniciar o shell do MongoDB, que permite a realização de operações no banco de dados através de comandos do próprio shell. Por exemplo:```mongod```


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
## Passo 4: 

Crie uma classe de configuração para habilitar o uso do Spring Data MongoDB no projeto.

- Para incluir o suporte ao MongoDB no seu projeto Spring Boot, você deve criar um arquivo de configuração na pasta src/main/java. Neste arquivo, você deve adicionar a anotação  `@Configuration` para indicar que é uma classe de configuração do contexto do Spring e `@EnableMongoRepositories` para habilitar o suporte a repositórios MongoDB.

```
@Configuration
@EnableMongoRepositories
public class MongoDBConfig {
}

```

- O @Configuration é uma anotação em Spring que indica que uma classe é usada para configurar o contexto do Spring. É usada para especificar que um bean deve ser criado para o contexto do Spring e que pode ser injetado em outros beans. É comumente usada junto com @Bean para criar e gerenciar beans no contexto do Spring. Além disso, as classes de configuração também podem ser usadas para configurar as propriedades do aplicativo, como a configuração de conexão com o banco de dados, configuração de segurança, configuração de propriedades de desempenho, entre outros. É importante notar que as classes de configuração são geralmente criadas no pacote raiz do aplicativo e podem ser usadas para configurar vários beans em diferentes pacotes do aplicativo.

- O @EnableMongoRepositories é um anotação usada para habilitar o suporte para repositórios MongoDB no projeto Spring Boot. Ele é usado para ativar a configuração de repositório MongoDB, que inclui a configuração do MappingMongoConverter para converter objetos Java para e de Documentos MongoDB.Quando a anotação é adicionada em um projeto, o Spring Boot irá procurar por todos os repositórios MongoDB na aplicação e os registrará como beans no contexto da aplicação. Isso permite que eles sejam usados em qualquer parte da aplicação, como controllers e services.Além disso, a anotação também permite especificar o pacote base para os repositórios MongoDB na aplicação, para que o Spring Boot possa facilmente encontrá-los durante a inicialização da aplicação.

Com essas configurações, o Spring Boot já estará conectado ao MongoDB e pronto para persistir e recuperar dados.

## Passo 5: 

É possível testar a conexão criando uma classe de teste que conecte o MongoDB usando o Spring Boot. Para criar essa classe, siga os seguintes passos:

- Abra o arquivo de testes da sua aplicação, geralmente localizado em src/test/java.
- Crie uma nova classe de teste chamada, por exemplo, MongoDbTest.
- Adicione a anotação @RunWith(SpringRunner.class) para indicar que essa classe é um teste do Spring.
- Adicione a anotação @SpringBootTest para indicar que essa classe deve ser iniciada como uma aplicação Spring Boot.
- Injete a dependência do objeto MongoTemplate usando a anotação @Autowired. Esse objeto será usado para realizar operações no banco de dados.

Crie um método de teste com a anotação @Test. Nele, utilize o objeto MongoTemplate para realizar uma operação de consulta no banco de dados. Por exemplo:


```
@RunWith(SpringRunner.class)
@SpringBootTest
public class MongoDbTest {
  
  @Autowired
  private MongoTemplate mongoTemplate;
  
  @Test
  public void testConnection() {
    List<Document> documents = mongoTemplate.findAll(Document.class, "collection_name");
    assertThat(documents).isNotEmpty();
  }
}


```
- Execute o teste usando o método de teste criado. Se o teste passar, significa que você conseguiu se conectar ao banco de dados e realizar uma operação. Se o teste falhar, verifique se você configurou corretamente os parâmetros de conexão no arquivo application.properties. Também verifique se o servidor MongoDB está rodando e se você tem permissão para acessar o banco de dados.

