# 🪟 Windows

## 1. Verificar o Git

:window: Windows: abra o prompt de comando do Windows ou "Git Bash".&#x20;

<figure><img src="../../../.gitbook/assets/image (11) (1) (1) (1).png" alt=""><figcaption><p>No Windows 11, vai se parecer com este! </p></figcaption></figure>

Depois de abrir seu aplicativo de terminal, digite:

```bash
git version
```

A saída irá dizer qual versão do Git está instalada, ou irá alertar que o git é um comando desconhecido. **Se for um comando desconhecido, continue lendo para descobrir como instalar o Git**.

<figure><img src="../../../.gitbook/assets/image (13) (1) (1) (1).png" alt=""><figcaption><p>Exemplo: Neste computador, a versão do Git é a 2.34.1</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (12) (1) (1) (1).png" alt=""><figcaption><p><em>Hoje a última versão do Git liberada é a 2.44.0.</em></p></figcaption></figure>

Como você pode perceber: a minha versão está um pouco desatualizada, mas não há problemas quanto a isso: o interessante é se preocupar sempre no primeiro número da versão, onde entram as maiores mudanças - chamadas de "Majors". Então V 2.34.1 não irá causar um problema tão grande quanto se no meu computador eu estivesse com a V 1.1.0!&#x20;

Feita a verificação, se o Git ainda não está instalado na sua máquina você precisará instalá-lo. você precisa seguir as instruções nos próximos passos. Caso contrário, pode pular direto para a próxima seção [clientes-git-git-clients.md](../clientes-git-git-clients.md "mention").

## **2. Baixar o Instalador do Git:**

* Acesse o site oficial do Git: [git-scm.com](https://git-scm.com/).
* Clique no botão de download para Windows.
* O download deve começar automaticamente. Aguarde até que o arquivo seja baixado completamente.

## **3. Executar o Instalador:**

* Após o download, abra o arquivo executável (`.exe`) do instalador do Git.
* Siga as instruções do assistente de instalação. Você pode deixar as opções padrão ou personalizar de acordo com suas preferências.

## **4. Configurar o Instalador:**

* Durante a instalação, você será solicitado a fazer algumas escolhas, como a localização de instalação e a seleção de componentes.
* Para a maioria dos usuários, as opções padrão funcionam bem. Basta seguir as instruções na tela.

## **5. Concluir a Instalação:**

* Após concluir a instalação, você pode fechar o instalador.
* O Git agora está instalado no seu sistema Windows.

## **6. Verificar a Instalação:**

Após a instalação, verifique se o Git foi instalado corretamente executando:

```sh
git --version
```

O Terminal deve exibir a versão do Git instalada, como por exemplo:

```
git version 2.36.1
```



{% hint style="info" %}
Para mais opções de instruções de como instalar o Git em outros vários sistemas Unix, veja na página do Git, em [Download Windows](https://git-scm.com/download/win).
{% endhint %}
