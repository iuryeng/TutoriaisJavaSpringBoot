# TutoriaisJavaSpringBoot

## Para instalar o Java Adopt, siga os seguintes passos:

1. Acesse o site do AdoptOpenJDK (https://adoptopenjdk.net/) e selecione a versão do Java que você deseja instalar. Você pode escolher entre as versões LTS (Long Term Support) ou as versões mais recentes.

2. Selecione o sistema operacional Windows como o sistema operacional em que você deseja instalar o Java.

3. Clique no botão "Download" para iniciar o download do arquivo de instalação. Certifique-se de que você está baixando a versão correta para o seu sistema operacional.

4. Na página de download, selecione o arquivo ".msi" na seção "Windows Installer (64-bit)" para baixar o arquivo de instalação para o Windows.

5. Quando o download for concluído, localize o arquivo de instalação e clique duas vezes nele para iniciar o processo de instalação. Siga as instruções na tela para concluir a instalação.

6. Configure a Variável de Ambiente JAVA_HOME durante a Instalação do AdoptOpenJDK (ver na sessão abaixo)

7. Depois de instalar o Java, é importante verificar se a instalação foi bem-sucedida. Abra o prompt de comando ou o terminal e digite o comando ``java -version``. Se a instalação foi bem-sucedida, o prompt exibirá informações sobre a versão do Java instalada.

![image](https://user-images.githubusercontent.com/38250160/209458681-1677f891-6169-4537-94d6-f5f443ff7b92.png)


Se você tiver problemas durante o processo de instalação, verifique se você está baixando a versão correta para o seu sistema operacional e siga as instruções na tela. Se você continuar enfrentando problemas, pode ser necessário desinstalar o Java e reinstá-lo ou entrar em contato com o suporte do AdoptOpenJDK para obter ajuda.


## Personalizando a Instalação do AdoptOpenJDK: Configurando a Variável de Ambiente JAVA_HOME"

Durante a instalação do AdoptOpenJDK, você pode selecionar a opção "Custom Setup" na tela de configuração para personalizar a instalação. Essa opção geralmente permite que você escolha quais componentes do Java deseja instalar e onde deseja instalá-los.

Uma das opções que você pode selecionar na tela de configuração personalizada é a opção "Set JAVA_HOME". JAVA_HOME é uma variável de ambiente que é usada para especificar o caminho para o diretório principal do Java no seu sistema. Ela é usada por algumas ferramentas e aplicativos para encontrar o Java instalado no sistema.

Para selecionar a opção "Set JAVA_HOME", basta clicar na caixa de seleção ao lado da opção e selecionar o diretório onde o Java foi instalado. Em geral, o diretório padrão para a instalação do Java é C:\Program Files\Java. Se você instalou o Java em outro lugar, pode selecionar o diretório correspondente.

Depois de selecionar a opção "Set JAVA_HOME" e especificar o diretório de instalação do Java, basta clicar em "Next" para continuar com o processo de instalação. Siga as instruções na tela para concluir a instalação do AdoptOpenJDK.

![image](https://user-images.githubusercontent.com/38250160/209458594-4cd8f90f-0f53-4191-88a4-8e797d8b887f.png)


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

# Além disso, você pode estar interessado em saber mais sobre:

## O que é o JRE ?

JRE (Java Runtime Environment) é um ambiente de execução Java que permite que os programas escritos na linguagem de programação Java sejam executados em um computador. Ele inclui a JVM (Java Virtual Machine) e as bibliotecas de tempo de execução necessárias para executar aplicativos Java.

O JRE é distribuído gratuitamente pela Oracle e está disponível para download em seu site. Ele é normalmente instalado automaticamente junto com o JDK (Java Development Kit) durante o processo de instalação do Java.

O JRE é usado para executar aplicativos Java, mas não inclui as ferramentas de desenvolvimento incluídas no JDK. Se você deseja desenvolver aplicativos Java, precisará instalar o JDK, que inclui o JRE e as ferramentas de desenvolvimento necessárias.

Ao instalar o JRE, você pode escolher instalar apenas o JRE ou instalar o JRE junto com o navegador web e o plugin Java, que permite que os aplicativos Java sejam executados no navegador web. Se você deseja executar aplicativos Java em um navegador web, precisará instalar o plugin Java junto com o JRE.

## O que é uma JVM ?
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


## Entendendo a Nomeclatura das versões - Exemplo JDK: jdk-11.0.17+8

A nomeclatura "jdk-11.0.17+8" se refere a uma versão específica do JDK (Java Development Kit). O JDK é um conjunto de ferramentas de desenvolvimento de software que é usado para criar aplicativos Java.

O número "11" na nomeclatura indica a versão principal do JDK. O JDK é atualizado periodicamente para incluir novas funcionalidades e corrigir problemas. A cada nova versão principal, o JDK é atualizado para uma nova versão, como a versão 11 ou a versão 14.

O número "0.17" na nomeclatura indica a versão menor do JDK. As atualizações menores são lançadas periodicamente para incluir novas funcionalidades e corrigir problemas em versões específicas do JDK. Por exemplo, a versão 0.17 pode ser uma atualização menor para a versão principal 11 do JDK.

O número "+8" na nomeclatura é um código de build que indica a versão específica do JDK. Cada build do JDK é uma versão específica que inclui correções de erros e outras atualizações. O código de build é usado para identificar a versão específica do JDK que está sendo usada.

Em resumo, a nomeclatura "jdk-11.0.17+8" se refere a uma versão específica do JDK, que é a versão 11 com a atualização menor 0.17 e o código de build +8. Ela inclui todas as funcionalidades e correções de erros incluídas nas versões anteriores e pode ser usada para desenvolver aplicativos Java.


## Qual a diferença entre uma JVM Ponto de acesso para OpenJ9 ?

A JVM Ponto de Acesso é um projeto de código aberto da Oracle que fornece uma implementação da JVM (Java Virtual Machine) para a linguagem de programação Java. A JVM Ponto de Acesso é projetada para ser rápida, leve e fácil de usar, e é usada em muitos ambientes de produção para executar programas Java.

OpenJ9 é uma outra implementação da JVM que também é um projeto de código aberto, mas é mantida pela IBM e pelo Eclipse Foundation. Como a JVM Ponto de Acesso, a OpenJ9 é projetada para ser rápida, leve e fácil de usar, e é usada para executar programas Java em muitos ambientes diferentes.

A principal diferença entre a JVM Ponto de Acesso e a OpenJ9 é que a JVM Ponto de Acesso é mantida pela Oracle, enquanto a OpenJ9 é mantida pela IBM e pelo Eclipse Foundation. Além disso, a JVM Ponto de Acesso é otimizada para rodar em sistemas operacionais Windows, enquanto a OpenJ9 é otimizada para rodar em sistemas operacionais Linux e macOS.

Ambas as JVMs são populares e amplamente utilizadas para executar programas Java, e cada uma delas tem suas próprias características e vantagens. A escolha entre elas geralmente depende das necessidades específicas do projeto e do ambiente de execução.



