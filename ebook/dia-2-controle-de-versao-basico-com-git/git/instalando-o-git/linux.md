# 🐧 Linux

{% hint style="info" %}
:mag:Curiosidade: O Git foi originalmente desenvolvido para versionar o sistema operacional Linux! É um projeto de código aberto maduro e com manutenção ativa desenvolvido em 2005 por Linus Torvalds, o famoso criador do kernel do sistema operacional Linux. :mag\_right:
{% endhint %}

Você pode instalar o Git no Linux de maneira simples usando o Terminal. Basta usar a ferramenta de gerenciamento de pacotes da sua distribuição.

## 1. Verificar o Git&#x20;

Procure por um aplicativo de prompt de comando chamado "Terminal".

<figure><img src="../../../.gitbook/assets/image (15).png" alt=""><figcaption><p>Terminal do Linux vai se parecer com este :)</p></figcaption></figure>

Depois de abrir seu aplicativo de terminal, digite:

```bash
git version
```

A saída irá dizer qual versão do Git está instalada, ou irá alertar que o git é um comando desconhecido. **Se for um comando desconhecido, continue lendo para descobrir como instalar o Git**.

<figure><img src="../../../.gitbook/assets/image (13) (1).png" alt=""><figcaption><p>Exemplo: Neste computador, a versão do Git é a 2.34.1</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (12) (1).png" alt=""><figcaption><p><em>Hoje a última versão do Git liberada é a 2.44.0.</em></p></figcaption></figure>

Como você pode perceber: a minha versão está um pouco desatualizada, mas não há problemas quanto a isso: o interessante é se preocupar sempre no primeiro número da versão, onde entram as maiores mudanças - chamadas de "Majors". Então V 2.34.1 não irá causar um problema tão grande quanto se no meu computador eu estivesse com a V 1.1.0!&#x20;

Feita a verificação, se o Git ainda não está instalado na sua máquina você precisará instalá-lo. você precisa seguir as instruções nos próximos passos. Caso contrário, pode pular direto para a próxima seção [clientes-git-git-clients.md](../clientes-git-git-clients.md "mention").

## 2. Identificar a Distribuição Linux

Se você não sabe qual distribuição do Linux está usando, siga estes passos:

### **a.** lsb\_release

**Digite o comando**: No terminal, digite o seguinte comando e pressione `Enter`:

```sh
lsb_release -a
```

### **b. Interprete o Output**

O comando `lsb_release -a` fornecerá informações sobre a distribuição. Veja um exemplo de output:

```sh
Distributor ID: Ubuntu
Description:    Ubuntu 20.04.3 LTS
Release:        20.04
Codename:       focal
```

**Distribuições Comuns**:

* **Ubuntu**: O campo `Distributor ID` mostrará "Ubuntu".
* **Debian**: O campo `Distributor ID` mostrará "Debian".
* **Fedora**: O campo `Distributor ID` mostrará "Fedora".
*   **Arch Linux**: Pode não ter `lsb_release` instalado por padrão. Caso não tenha, siga as intruções do próximo passo (c).\


    <figure><img src="../../../.gitbook/assets/image (14).png" alt=""><figcaption><p>Exemplo: aqui usamos Ubuntu!</p></figcaption></figure>

### **c. Alternativa para Arch Linux**&#x20;

Se você estiver usando Arch Linux ou uma distribuição que não tenha `lsb_release` instalado por padrão, use este comando:

```sh
cat /etc/os-release
```

O output será algo assim:

```sh
NAME="Arch Linux"
PRETTY_NAME="Arch Linux"
ID=arch
```

## 3. Instalar o Git

Depois de identificar a sua distribuição, use o comando apropriado para instalar o Git:

### **Ubuntu ou Debian:**

```sh
sudo apt update
sudo apt install git
```

### **Fedora:**

Até o Fedora 21:

```bash
yum install git
```

A partir do Fedora 22:

```sh
dnf install git
```

### **Arch Linux:**

```sh
sudo pacman -S git
```

## 4. Verificar a Instalação

Para verificar se o Git foi instalado corretamente, digite:

```sh
git --version
```

Isso deve exibir a versão do Git instalada, como por exemplo:

```
git version 2.36.1
```

Pronto! O Git está instalado e pronto para uso no seu sistema Linux.

{% hint style="info" %}
Para mais opções de instruções de como instalar o Git em outros vários sistemas Unix, veja na página do Git, em [Download Linux](https://git-scm.com/download/linux).
{% endhint %}
