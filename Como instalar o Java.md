# TutoriaisJavaSpringBoot

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