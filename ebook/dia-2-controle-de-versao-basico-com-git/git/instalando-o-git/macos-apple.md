# 🍎 MacOS (Apple)

Existem inúmeras formas de instalar o Git no MacOS. Para iniciantes, o jeito mais fácil é utilizando o [Homebrew](https://brew.sh/), que é um gerenciador de pacotes consideravelmente simples de usar. Aqui está o passo a passo.

## **1. Verificar o Git**

Abra o Terminal, você pode encontrá-lo em **Finder >** **Aplicativos > Utilitários > Terminal**

<figure><img src="../../../.gitbook/assets/image (19).png" alt=""><figcaption><p>Terminal do MacOS vai se parecer com este :)</p></figcaption></figure>

Depois de abrir seu aplicativo de terminal, digite:

```bash
git version
```

A saída irá dizer qual versão do Git está instalada, ou irá alertar que o git é um comando desconhecido. **Se for um comando desconhecido, continue lendo para descobrir como instalar o Git**.

<figure><img src="../../../.gitbook/assets/image (13) (1) (1).png" alt=""><figcaption><p>Exemplo: Neste computador, a versão do Git é a 2.34.1</p></figcaption></figure>



<figure><img src="../../../.gitbook/assets/image (12) (1) (1).png" alt=""><figcaption><p><em>Hoje a última versão do Git liberada é a 2.44.0.</em></p></figcaption></figure>

Como você pode perceber: a minha versão está um pouco desatualizada, mas não há problemas quanto a isso: o interessante é se preocupar sempre no primeiro número da versão, onde entram as maiores mudanças - chamadas de "Majors". Então V 2.34.1 não irá causar um problema tão grande quanto se no meu computador eu estivesse com a V 1.1.0!&#x20;

Feita a verificação, se o Git ainda não está instalado na sua máquina você precisará instalá-lo. você precisa seguir as instruções nos próximos passos. Caso contrário, pode pular direto para a próxima seção [clientes-git-git-clients.md](../clientes-git-git-clients.md "mention").

## **2. Instalar o** [**Homebrew**](https://brew.sh/) **(caso você ainda não o tenha):**&#x20;

Execute o seguinte comando no terminal:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Siga as instruções no Terminal para concluir a instalação.

## **3. Instalar o Git com Homebrew:**&#x20;

Ainda no Terminal, execute o seguinte comando:

```sh
brew install git
```

O Homebrew irá baixar e instalar a versão mais recente do Git para você.

## **4. Verificar a Instalação:**&#x20;

Após a instalação, verifique se o Git foi instalado corretamente executando:

```sh
git --version
```

O Terminal deve exibir a versão do Git instalada, como por exemplo:

```
git version 2.36.1
```



{% hint style="info" %}
Para mais opções de instruções de como instalar o Git em outros vários sistemas Unix, veja na página do Git, em [Download MacOS](https://git-scm.com/download/mac).
{% endhint %}

