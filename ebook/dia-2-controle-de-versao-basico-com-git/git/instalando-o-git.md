---
description: >-
  Como instalar o Git nos 3 principais Sistemas Operacionais:  Linux, Mac e
  Windows!
---

# Instalando o Git



<figure><img src="../../.gitbook/assets/GITU,BUCA MELHORADO).png" alt=""><figcaption><p>Aprender sobre o Git é com a Cumbuca Dev! <span data-gb-custom-inline data-tag="emoji" data-code="1f49c">💜</span><span data-gb-custom-inline data-tag="emoji" data-code="1f965">🥥</span></p></figcaption></figure>

Antes de começar a usar o Git, você precisa que ele esteja disponível em seu computador. Na verdade, o Git já vem instalado por padrão na maioria das máquinas Mac e Linux, mas mesmo se ele já tiver sido instalado, é sempre uma boa prática atualizar para a versão mais recente.

### Verificando o Git&#x20;

:penguin: Linux: procure por um aplicativo de prompt de comando chamado "Terminal".

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption><p>Terminal do Linux vai se parecer com este :)</p></figcaption></figure>

:apple:Mac: procure por um aplicativo de prompt de comando chamado "Terminal".&#x20;

INSERIR IMAGEM TERMINAL GAMELA

:window: Windows: abra o prompt de comando do Windows ou "Git Bash".&#x20;

<figure><img src="../../.gitbook/assets/image (11) (1).png" alt=""><figcaption><p>No Windows 11, vai se parecer com este! </p></figcaption></figure>



Depois de abrir seu aplicativo de terminal, digite:

&#x20;`git version`

A saída irá dizer qual versão do Git está instalada, ou irá alertar que o git é um comando desconhecido. **Se for um comando desconhecido, continue lendo para descobrir como instalar o Git**.

<figure><img src="../../.gitbook/assets/image (13) (1).png" alt=""><figcaption><p>Exemplo: Neste computador, a versão do Git é a 2.34.1</p></figcaption></figure>

No site que contém a [documentação oficial do Git](https://git-scm.com/), sempre vão conter as informações mais importantes para o uso dele.&#x20;



:bulb: Inclusive este é um bom hábito para iniciantes: sempre que estiver usando algum programa (linguagem de programação/biblioteca/framework...) que seja novidade para você, é interessante dar uma olhada na documentação oficial, que é onde vais encontrar as instruções de uso, últimas versões, boas práticas, dicas e até fóruns com as dúvidas mais comuns referentes à ele. Vale à pena "gastar um tempinho" conhecendo antes para não ter problemas depois!&#x20;



<figure><img src="../../.gitbook/assets/image (12) (1).png" alt=""><figcaption><p>Hoje a última versão do Git liberada é a 2.44.0</p></figcaption></figure>



Como você pode perceber: a minha versão está um pouco desatualizada, mas não há problemas quanto a isso: o interessante é se preocupar sempre no primeiro número da versão, onde entram as maiores mudanças - chamadas de "Majors". Então V 2.34.1 não irá causar um problema tão grande quanto se no meu computador eu estivesse com a V 1.1.0!&#x20;



_Caso tenhas alguma dificuldade para fazer a instalação ou a atualização do Git, estamos disponíveis para te ajudar tanto no_ _fórum quanto no grupo do telegram do treinamento ou no e-mail cumbucadev@gmail.com._



Feita a verificação, se o Git ainda não está instalado na sua máquina você pode instalá-lo como um pacote, através de outro instalador, ou baixar o código fonte e compilá-lo. A instalação muda de acordo com o sistema operacional do seu computador, e abaixo seguem as instruções para os 3 mais utilizados.

&#x20;&#x20;

### :penguin: Instalando no Linux&#x20;

:mag:Curiosidade: O Git foi originalmente desenvolvido para versionar o sistema operacional Linux! É um projeto de código aberto maduro e com manutenção ativa desenvolvido em 2005 por Linus Torvalds, o famoso criador do kernel do sistema operacional Linux. :mag\_right:

Se você deseja instalar o Git no Linux através do terminal, pela linha de comando é possível sim, e você pode geralmente fazê-lo através da ferramenta básica de gerenciamento de pacotes que vem com sua distribuição.&#x20;

Se você não sabe qual a distribuição do Linux que usa, é só abrir o terminal e usar o comando:

`$ lsb_release -a`

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption><p>Exemplo: aqui usamos Ubuntu!</p></figcaption></figure>

Verificada a distribuição - ou caso você já saiba qual utiliza: acesse seu shell de prompt de comando e execute o seguinte comando para garantir que tudo esteja atualizado:&#x20;

`$ sudo apt-get update`&#x20;

* Se você usar **Fedora**, por exemplo, você pode usar o _yum_:

`$ sudo yum install git-all`&#x20;

* Se você usar uma distribuição baseada em Debian como o **Ubuntu**, use o _apt-get_:

`$ sudo apt-get install git-all`&#x20;

Para mais opções de instruções de como instalar o Git em outros vários sistemas Unix, veja na página do Git, em [Download Linux](https://git-scm.com/download/linux).



### :apple: Instalando no Mac&#x20;

Existem várias maneiras de instalar o Git em um Mac. O mais fácil é provavelmente instalar as ferramentas pela linha de comando Xcode.&#x20;

No Mavericks (10,9) ou acima, você pode fazer isso simplesmente rodando **git** a partir do Terminal pela primeira vez. Se você não tiver o Git instalado, ele irá avisar e pedir para que você instale.

Se você quiser uma versão mais atualizada, você também pode instalá-lo através de um instalador binário. Um instalador OSX Git é mantido e disponível para [download no site do Git](https://git-scm.com/download/mac).

Git OS X installer.  Instalador do Git no OS X. Você também pode instalá-lo como parte do instalador GitHub para Mac. Sua ferramenta GUI Git tem uma opção para instalar as ferramentas de linha de comando. Você pode baixar essa ferramenta a partir da página GitHub para Mac, em http://mac.github.com.



<mark style="background-color:yellow;">Instalar Git no Mac A maioria das versões do MacOS já terá o Git instalado, e você pode ativá-lo pelo terminal com git version. No entanto, se você não tiver o Git instalado por qualquer motivo, você pode instalar a versão mais recente do Git usando um dos vários métodos populares listados abaixo: Instalar Git a partir de um instalador Acesse o instalador mais recente do Git para macOS e faça o download da versão mais recente. Depois que o instalador iniciar, siga as instruções fornecidas até que a instalação seja concluída. Abra o prompt de comando "terminal" e digite git version para verificar se o Git foi instalado. Nota: git-scm é um recurso popular e recomendado para baixar o Git em um Mac. A vantagem de baixar o Git do git-scm é que seu download começa automaticamente com a versão mais recente do Git. A fonte de download é o mesmo instalador do Git para macOS referenciado nos passos acima. Instalar Git do Homebrew O Homebrew é um gerenciador de pacotes popular para o macOS. Se você já tiver o Homebrew instalado, você pode seguir os passos abaixo para instalar o Git: Abra uma janela do terminal e instale o Git usando o seguinte comando: brew install git. Depois que a saída do comando for concluída, você pode verificar a instalação digitando: git version.</mark>

### &#x20;:window: Instalando no Windows&#x20;

Há também algumas maneiras de instalar o Git no Windows. A compilação mais oficial está disponível para download no site do Git. Basta ir ao http://git-scm.com/download/win e o download começará automaticamente. Note que este é um projeto chamado Git para Windows (também chamado msysGit), que é algo separado do Git; para mais informações sobre isso, vá para http://msysgit.github.io/.

Para fazer uma instalação automatizada, você pode usar o pacote Git do Chocolatey. Note que o pacote Chocolatey é mantido pela comunidade.

Outra forma fácil de obter Git instalada é através da instalação de GitHub para Windows. O instalador inclui uma versão de linha de comando do Git, bem como a GUI. Ele também funciona bem com o PowerShell, e configura o cache de credenciais sólidas e as devidas configurações CRLF. Vamos saber mais sobre isso um pouco mais tarde, por enquanto basta dizer que estas são coisas que você deveria ter. Você pode baixá-lo da página GitHub para Windows, em http://windows.github.com.

<mark style="background-color:yellow;">Instalar Git no Windows Acesse o instalador mais recente do Git para Windows e faça o download da versão mais recente. Depois que o instalador iniciar, siga as instruções fornecidas na tela do assistente de configuração do Git até que a instalação seja concluída. Abra o prompt de comando do Windows (ou Git Bash se você optou por não usar o prompt de comando padrão do Git para Windows durante a instalação do Git). Digite git version para verificar se o Git foi instalado. Nota: git-scm é um recurso popular e recomendado para baixar o Git para Windows. A vantagem de baixar o Git do git-scm é que seu download começa automaticamente com a versão mais recente do Git incluída com o prompt de comando recomendado, Git Bash. A fonte de download é o mesmo instalador do Git para Windows referenciado nos passos acima.</mark>



\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ esta parte pensei em não colocar:&#x20;

Instalando da Fonte Algumas pessoas podem achar interessante instalar Git a partir da fonte, para ter a versão mais recente. Os instaladores binários tendem a ficar um pouco atrás, embora após o Git ter amadurecido nos últimos anos, isso faz cada vez menos diferença.

Se você deseja instalar o Git a partir da fonte, você precisa ter as seguintes bibliotecas das quais o Git: curl, zlib, openssl, expat, e libiconv. Por exemplo, se você estiver em um sistema que tem yum (como o Fedora) ou apt-get (tal como um sistema baseado em Debian), você pode usar um destes comandos para instalar as dependências mínimas para compilar e instalar os binários do Git:

source,console]

$ sudo yum install dh-autoreconf curl-devel expat-devel gettext-devel\
openssl-devel perl-devel zlib-devel $ sudo apt-get install dh-autoreconf libcurl4-gnutls-dev libexpat1-dev\
gettext libz-dev libssl-dev Para incluir a documentação em vários formatos (doc, html, info), essas dependências adicionais são necessárias:

$ sudo yum install asciidoc xmlto docbook2X getopt $ sudo apt-get install asciidoc xmlto docbook2x getopt Além disso, se estiver usando o Fedora/RHEL/derivados-do-RHEL, vai precisar executar

$ sudo ln -s /usr/bin/db2x\_docbook2texi /usr/bin/docbook2x-texi devido a diferenças nos nomes dos binários.

Quando você tiver todas as dependências necessárias, você poderá baixar o tarball com a última versão de vários lugares. Você pode obtê-lo através da página Kernel.org, em https://www.kernel.org/pub/software/scm/git, ou no espelho no site do GitHub, em https://github.com/git/git/releases. Em geral, é um pouco mais claro qual é a versão mais recente na página do GitHub, mas a página kernel.org também tem assinaturas se você quiser verificar o seu download.

Então, compile e instale:

$ tar -zxf git-2.0.0.tar.gz $ cd git-2.0.0 $ make configure $ ./configure --prefix=/usr $ make all doc info $ sudo make install install-doc install-html install-info Depois de ter feito isso, você poderá atualizar o Git através dele mesmo:

$ git clone git://git.kernel.org/pub/scm/git/git.git



{% embed url="https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-Instalando-o-Git" %}

{% embed url="https://github.com/git-guides/install-git" %}
