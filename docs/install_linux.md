# Instalar o Python no Linux

> **Observação**
>
> Se você não utiliza linux pode pular esta parte, mas se quiser saber um pouco mais fique por aqui.

## Gerenciador de pacotes

O gerenciador de pacotes usado depende da distribuição do Linux. As distribuições Linux mais populares como Debian, Ubuntu e Mint incluem o APT, já distros como RHEL, Fedora e CentOS incluem YUM ou DNF.

Abaixo temos instruções para APT e YUM. Se sua distribuição Linux usar um gerenciador de pacotes diferente, talvez seja necessário pesquisar como instalar o Python 3 na sua distribuição do Linux.

## Instalar usando APT

Abra uma janela do terminal.

Digite o comando a seguir para atualizar os índices de pacotes do APT.

```Bash
$ sudo apt-get update
```

O comando ``apt-get update`` atualiza a lista de pacotes (os índices de pacotes) dos repositórios e dos PPAs (arquivos de pacotes pessoais). Essa atualização permite que apt-get encontre as últimas versões dos pacotes que você deseja instalar e suas dependências.

<br>
> Observação
>
>O comando sudo eleva temporariamente suas permissões para o root, o nível mais avançado do sistema. Ao usar sudo, geralmente será solicitada a senha da sua conta de usuário.

Após a execução, o  ``apt-get update`` vai exibir todos os itens que serão atualizados. Ele pode solicitar que você aprove, digitando y (yes) e pressione Enter.

Execute o comando a seguir para instalar o Python 3.

```Bash
$ sudo apt-get install python3
```

<br>
> Observação
>
>O comando ``apt-get install`` localiza os pacotes apropriados no índice de pacotes, baixa os arquivos necessários e os instala nos diretórios apropriados.

Execute o comando a seguir para confirmar se o Python 3 foi instalado corretamente:

```Bash
$ python3 --version
```

A saída deve ser semelhante a esta:

```Bash
$ Python 3.11.4
```

<br>
> **Observação**
>
>Se a instalação falhar, você poderá ver uma mensagem de erro. Insira a mensagem de erro exata no navegador para localizar possíveis causas e soluções.

## Instalar usando YUM

Abrir uma janela do Terminal

Execute o comando a seguir para atualizar a lista de pacotes do YUM

```Bash
$ sudo yum update
```

<br>
> **Observação**
>
> No caso de utilizar o DNF, o que vai mudar é justamente o nome do gerenciador de pacotes ``sudo dnf update``

O comando ``yum update`` garantirá que todos os pacotes e suas dependências estejam atualizados.
É recomendado atualizar a lista de pacotes antes de instalar qualquer novo software.

Execute o seguinte comando para instalar o Python 3

```Bash
$ sudo yum install python3
```

Execute este comando para verificar a instalação:

```Bash
$ python3 --version
```

A saída deve ser semelhante a seguinte:

```Bash
$ Python 3.11.4
```

<br>
> **Observação**
>
>Se a instalação falhar, você poderá ver uma mensagem de erro. Insira a mensagem de erro exata no navegador para localizar possíveis causas e soluções.

**Pronto! Você instalou o Python com êxito em seu sistema.**
