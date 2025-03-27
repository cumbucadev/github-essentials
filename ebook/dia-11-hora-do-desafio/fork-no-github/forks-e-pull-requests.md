# Forks e Pull Requests

Forks e Pull Requests são ferramentas essenciais no GitHub para a colaboração em projetos open source. O **fork** permite criar uma cópia de um repositório para que você possa realizar alterações sem impactar o projeto original, enquanto o **Pull Request (PR)** serve para sugerir essas modificações ao repositório principal.

Analisando o processo de forma geral, as etapas são as seguintes:

1. **Criar um Fork**: Crie uma cópia do repositório original na sua conta do GitHub.
2. **Clonar o Repositório Forkado**: Clone o seu fork para o seu ambiente local para começar a trabalhar nas alterações.
3. **Fazer Modificações**: Realize as alterações necessárias no seu repositório local.
4. **Enviar as Alterações para o Fork**: Após fazer as modificações, envie as mudanças para o seu repositório remoto (origin) no GitHub.
5. **Criar um Pull Request (PR)**: Abra um Pull Request para sugerir as alterações feitas no seu fork para o repositório original.

Vamos explorar um pouco de cada uma dessas etapas a seguir.

## 1. Criando um Fork

O primeiro passo é escolher o repositório do qual deseja fazer um fork.

<figure><img src="../../.gitbook/assets/workflow com fork 1.png" alt=""><figcaption></figcaption></figure>

Acesse a página do repositório no GitHub e clique no botão **Fork**. Isso criará uma cópia do repositório original na sua conta, permitindo que você faça modificações sem alterar o projeto principal.

<figure><img src="../../.gitbook/assets/workflow com fork 2.png" alt=""><figcaption></figcaption></figure>

## 2. Clonando o Repositório Forkado

Pensando da perspectiva do seu fork, a nomenclatura utilizada é:

* **origin** → seu repositório (fork)
* **upstream** → o repositório original

Para sugerir mudanças no **upstream**, primeiro é necessário clonar o seu fork localmente. Execute o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">clone</mark> <mark style="color:green;">repositório.</mark>

<figure><img src="../../.gitbook/assets/workflow com fork 3.png" alt=""><figcaption></figcaption></figure>

O GitHub enviará uma cópia do seu **origin** para seu computador.

<figure><img src="../../.gitbook/assets/workflow com fork 4.png" alt=""><figcaption></figcaption></figure>

Essa cópia será armazenada automaticamente no seu ambiente local.

<figure><img src="../../.gitbook/assets/workflow com fork 5.png" alt=""><figcaption></figcaption></figure>

Agora, você tem uma versão local do repositório e pode começar a fazer alterações.

## 3. Fazendo Modificações

Edite os arquivos conforme necessário e salve as mudanças.

<figure><img src="../../.gitbook/assets/workflow com fork 6.png" alt=""><figcaption></figcaption></figure>

Em seguida, envie essas alterações para o seu repositório remoto (**origin**) no GitHub.

<figure><img src="../../.gitbook/assets/workflow com fork 7.png" alt=""><figcaption></figcaption></figure>

## 4. Criando um Pull Request

Assim que suas mudanças estiverem disponíveis no GitHub no seu repositório (**origin**), você poderá abrir um **Pull Request (PR)** para sugerir essas alterações ao repositório original (**upstream**).

<figure><img src="../../.gitbook/assets/workflow com fork 8.png" alt=""><figcaption></figcaption></figure>

Se o PR for aprovado pelas pessoas mantenedoras do repositório original, suas modificações serão incorporadas ao branch principal do **upstream**.

***

{% hint style="warning" %}
Nesta seção, evitamos mencionar **issues** e **branches** para manter o processo mais direto e claro. O fluxo completo será abordado mais adiante.
{% endhint %}

A seguir, veremos como realizar esse processo na prática.
