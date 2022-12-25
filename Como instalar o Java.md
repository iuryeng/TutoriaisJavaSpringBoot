# TutoriaisJavaSpringBoot

## Para instalar o Java Adopt, siga os seguintes passos:

1. Acesse o site do AdoptOpenJDK (https://adoptopenjdk.net/) e selecione a versão do Java que você deseja instalar. Você pode escolher entre as versões LTS (Long Term Support) ou as versões mais recentes.

2. Selecione o sistema operacional em que você deseja instalar o Java. Você pode escolher entre Windows, macOS, Linux ou outro sistema operacional.

3. Clique no botão "Download" para iniciar o download do arquivo de instalação. Certifique-se de que você está baixando a versão correta para o seu sistema operacional.

4. Quando o download for concluído, localize o arquivo de instalação e clique duas vezes nele para iniciar o processo de instalação. Siga as instruções na tela para concluir a instalação.

5. Depois de instalar o Java, é importante verificar se a instalação foi bem-sucedida. Abra o prompt de comando ou o terminal e digite o comando "java -version". Se a instalação foi bem-sucedida, o prompt exibirá informações sobre a versão do Java instalada.

Se você tiver problemas durante o processo de instalação, verifique se você está baixando a versão correta para o seu sistema operacional e siga as instruções na tela. Se você continuar enfrentando problemas, pode ser necessário desinstalar o Java e reinstá-lo ou entrar em contato com o suporte do AdoptOpenJDK para obter ajuda.


## Para instalar o Java Oracle, siga os seguintes passos:

1. Acesse o site da Oracle e baixe o instalador do Java. Você pode fazer isso acessando o link https://www.oracle.com/java/technologies/javase-downloads.html e clicando em "Download" na opção "Java SE Development Kit (JDK)".

2. Execute o instalador baixado e siga as instruções do assistente de instalação. É importante prestar atenção nas opções de instalação e garantir que o Java seja instalado na pasta correta.

3. Quando a instalação estiver concluída, é necessário configurar as variáveis de ambiente do sistema. Para fazer isso, vá até o Painel de Controle do sistema operacional e clique em "Sistema e Segurança".

4. Em seguida, clique em "Sistema" e vá até a aba "Avançadas". Clique em "Variáveis de Ambiente" e, na seção "Variáveis de Sistema", clique em "Novo".

5. Na caixa de diálogo que aparece, digite "JAVA_HOME" no campo "Nome da Variável" e o caminho da pasta onde o Java foi instalado no campo "Valor da Variável". Por exemplo, se o Java foi instalado na pasta "C:\Program Files\Java\jdk1.8.0_241", o valor da variável seria "C:\Program Files\Java\jdk1.8.0_241".

6. Clique em "OK" para criar a variável de ambiente JAVA_HOME. Em seguida, clique em "Novo" novamente e crie uma nova variável de ambiente chamada "Path".

7. No campo "Valor da Variável", adicione o seguinte texto: "%JAVA_HOME%\bin" (sem as aspas). Isso fará com que o Java seja adicionado à lista de programas executáveis do sistema.

8. Clique em "OK" para criar a variável de ambiente "Path" e finalize o processo de configuração das variáveis de ambiente.

9. Para verificar se a instalação foi realizada corretamente, abra o Prompt de Comando do sistema operacional e digite "java -version". Se a instalação foi realizada corretamente, o sistema deverá exibir a versão do Java instalada.

## Para instalar o Java da Azul Systems, siga os seguintes passos:

1. Acesse o site da Azul Systems (https://www.azul.com/) e faça o download do instalador do Java, de acordo com o sistema operacional da sua máquina.

2. Abra o instalador baixado e siga os passos de instalação.

3. Quando a instalação for concluída, abra o terminal e digite o comando "java -version" para verificar se a instalação foi realizada com sucesso.

4. Se a instalação foi realizada corretamente, o terminal exibirá a versão do Java instalada na sua máquina.

Se você deseja definir o Java da Azul como o Java padrão em sua máquina, é necessário configurar as variáveis de ambiente. Para fazer isso, siga os seguintes passos:

No Windows:

- Clique no botão Iniciar e, em seguida, clique em Configurações > Sistema > Sobre.

- Clique em Configurações avançadas do sistema.

- Na aba Avançado, clique em Variáveis de ambiente.

- Na seção Variáveis do sistema, procure a variável JAVA_HOME e clique em Editar.

- Na caixa de diálogo Editar variável de ambiente, defina o caminho para a pasta onde o Java da Azul foi instalado (por exemplo, C:\Program Files\Azul\Zulu\jdk-11.0.9.1-x64).

- Na seção Variáveis de usuário, procure a variável Path e clique em Editar.

- Na caixa de diálogo Editar variável de ambiente, clique em Novo e adicione o caminho para a pasta bin do Java da Azul (por exemplo, C:\Program Files\Azul\Zulu\jdk-11.0.9.1-x64\bin).

- Clique em OK para salvar as alterações.

No Linux:

- Abra o arquivo ~/.bashrc com um editor de texto (por exemplo, nano ou vim).

- Adicione as seguintes linhas no final do arquivo:
    export JAVA_HOME=caminho_para_o_java_da_azul
    export PATH=$PATH:$JAVA_HOME/bin
    
- Salve o arquivo e feche o editor.

No terminal, digite o comando "source ~/.bashrc" para atualizar as variáveis de ambiente.

# Além disso, você pode estar interessado em saber mais sobre:

## O que é uma JVM?
JVM (Java Virtual Machine) é um ambiente de execução que permite que os programas escritos na linguagem de programação Java sejam executados em diferentes sistemas operacionais e plataformas. A JVM é responsável por carregar, interpretar e executar os programas Java.

Quando um programa Java é compilado, ele é convertido em um conjunto de instruções chamadas código de máquina Java, que é específico para a JVM. Quando o programa é executado, a JVM carrega o código de máquina e o interpreta, convertendo as instruções em ações que o sistema operacional entende e pode executar. Isso permite que o programa Java seja executado em qualquer sistema operacional que tenha uma JVM instalada, independentemente de qual linguagem de programação foi usada para escrever o sistema operacional.

A JVM também fornece um conjunto de serviços e bibliotecas que podem ser usados pelos programas Java, como a capacidade de gerenciar memória, acessar o sistema de arquivos e se comunicar com outros programas através de redes. Além disso, a JVM inclui um conjunto de ferramentas de depuração e perfis que podem ser usadas para identificar e solucionar problemas em programas Java.

## O que é um JDK ?

JDK (Java Development Kit) é um conjunto de ferramentas de desenvolvimento de software que é usado para criar aplicativos Java. Ele inclui um compilador Java, um interpretador Java e uma série de bibliotecas e ferramentas que são usadas para desenvolver, testar e depurar aplicativos Java.

O JDK é uma parte essencial da plataforma de desenvolvimento Java e é necessário para qualquer pessoa que deseje desenvolver aplicativos Java. Ele é distribuído gratuitamente pela Oracle e está disponível para download em seu site.

O JDK inclui o seguinte:

- Compilador Java: um programa que converte o código fonte Java em um conjunto de instruções que a JVM (Java Virtual Machine) entende e pode executar.

- Interpretador Java: um programa que lê o código de máquina Java e o executa.

- Bibliotecas: conjuntos de classes pré-escritas que fornecem funcionalidades comuns usadas pelos aplicativos Java, como entrada e saída de dados, gerenciamento de memória e acesso ao sistema de arquivos.

- Ferramentas de depuração: ferramentas que ajudam a identificar e corrigir problemas em aplicativos Java.

- Ferramentas de teste: ferramentas que ajudam a testar aplicativos Java para garantir que eles estejam funcionando corretamente.

O JDK também inclui documentação e exemplos de código que ajudam os desenvolvedores a aprender a usar as ferramentas e bibliotecas incluídas no kit de desenvolvimento.

