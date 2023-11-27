Instalar o Python no Linux
O gerenciador de pacotes usado dependerpa da versão do Linux. As distribuições Linux mais populares incluem APT (um acrônimo para "Advanced Packaging Tool") ou YUM (um acrônimo para "Yellowdog Updater, Modified").

Fornecemos instruções para APT e YUM nesta unidade. Se a distribuição do Linux usar um gerenciador de pacotes diferente, talvez seja necessário pesquisar <sua distribuição do Linux > instalar o Python 3.

Instalar usando APT
Se você usar a APT, poderá usar estas instruções para instalar o Python 3.

Abra uma janela do terminal.

Insira o comando a seguir para atualizar índices de pacote APT.

Bash

Copiar
sudo apt-get update
O comando apt-get update atualiza a lista de pacotes (os índices de pacote) dos repositórios e dos PPAs (arquivos de pacotes pessoais) dos quais está ciente. Essa atualização permite que apt-get encontre as últimas versões dos pacotes que você deseja instalar e suas dependências.

 Observação

O comando sudo eleva temporariamente suas permissões para a raiz, o nível mais avançado do sistema. Ao usar sudo, geralmente será solicitada a senha da sua conta de usuário.

apt-get update exibe todos os itens que serão atualizados. Ele pode solicitar que você aprove digitando y ou yes e pressione Enter.

Execute o comando a seguir para instalar o Python 3 em um prompt do Bash

Bash

Copiar
sudo apt-get install python3.10
 Observação

O apt-get install localiza os pacotes apropriados do índice de pacote, baixa os arquivos necessários e instala os arquivos nas pastas apropriadas.

Execute o comando python3 para confirmar se o Python 3 foi instalado corretamente:

Bash

Copiar
python3.10 --version
A saída deve conter a palavra Python com um conjunto de números separados por caracteres .. O exemplo a seguir mostra a saída que você pode ver.

Saída

Copiar
Python 3.10.0
Se o primeiro número for 3, o Python 3 foi instalado com êxito.

Se a instalação falhar, você poderá ver uma mensagem de erro. Insira a mensagem de erro exata no navegador para localizar possíveis causas e soluções.

Instalar usando YUM
O gerenciador de pacotes YUM é usado principalmente pelos sistemas Red Hat, como Red Hat Enterprise Linux e Fedora, bem como pelo CentOS. Se o APT não estiver instalado no seu sistema, você poderá tentar o YUM.

Abrir uma janela do Terminal

Execute sudo yum update para atualizar os índices do pacote YUM

Bash

Copiar
sudo yum update
O yum update garantirá que todos os pacotes e suas dependências estejam atualizados. É uma boa ideia atualizar a lista de pacotes antes de instalar o novo software.

Execute o seguinte comando yum install para instalar o Python 3

Bash

Copiar
sudo yum install rh-python3.10
Execute python3.10 --version para verificar a instalação:

Bash

Copiar
python3.10 --version
A saída inclui a palavra Python com um conjunto de números separados por caracteres ., por exemplo:

Saída

Copiar
Python 3.10.0
Se o primeiro número for 3, o Python 3 foi instalado com êxito.

Se a instalação falhar, você verá uma mensagem de erro; a etapa 5 ajudará a resolver qualquer mensagem de erro.

(Opcional) Habilitar o recurso Coleções de Software no Bash
As Coleções de Software permitem que você instale várias versões dos mesmos componentes de software em seu sistema Red Hat. Quando você executa a ferramenta SCL, ela cria um processo filho (subshell) do shell atual. Executar o comando novamente cria um subshell do subshell. Quando a ferramenta Coleções de Software estiver habilitada, você precisará especificar qual versão do Python você deseja executar no shell.

Execute o comando scl enable em um prompt do Bash:

Bash

Copiar
scl enable rh-python3.10 bash
Novamente, verifique se tudo está OK executando python3.10 --version.

Bash

Copiar
python3.10 --version
O resultado daquele comando deve ser semelhante ao seguinte formato:

Saída

Copiar
Python 3.10.0
Se o primeiro número for 3, o Python 3 foi instalado com êxito, no contexto de uma Coleção de Software.

O scl enable python36 inicia uma nova sessão do Bash, definindo o Python 3.6 como a versão padrão do Python. No entanto, o Python 3.6 é a versão padrão somente para a sessão do shell atual. Se você sair da sessão ou abrir uma nova sessão de outro terminal, o Bash será revertido para a versão padrão do Python.

Para obter mais informações, confira as Coleções de Software Red Hat 3.8.

 Importante

Caso você precise usar scl enable para executar python3.10 --version, talvez seja necessário executar esse comando toda vez que queira trabalhar no Python. Há soluções alternativas, mas essa é a funcionalidade pretendida das Coleções de Software. Confira Fazer uma Coleção de Software Red Hat persistir para obter uma solução alternativa possível.

Agora, você instalou o Python com êxito em seu sistema local.