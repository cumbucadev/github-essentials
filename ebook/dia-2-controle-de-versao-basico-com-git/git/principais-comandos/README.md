---
description: >-
  Nesta seção, vamos explorar os comandos essenciais do Git, desde a
  inicialização de um repositório até a colaboração com outras pessoas
  desenvolvedoras.
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Principais Comandos

Caso já tenha seguido as instruções da seção [instalando-o-git.md](../instalando-o-git.md "mention"), não é necessário instalar e nem configurar mais nada para ter acesso à Git CLI. Apenas abra o terminal e todos os comandos git já estão disponíveis para você.

> Imagem: captura de tela rodando o comando "git"

### git

O comando `git` é o ponto de entrada para **todas** as operações do Git. Ele é utilizado para invocar quaisquer outros comandos disponíveis no Git. Para utilizá-lo, basta digitar no terminal de comando `git` seguido pelo nome do comando que deseja executar e quaisquer argumentos necessários.

A estrutura básica para utilizar o comando `git` é a seguinte:

<mark style="color:purple;">`git`</mark><mark style="color:orange;">`comando`</mark><mark style="color:blue;">`[opções]`</mark><mark style="color:green;">`[argumentos]`</mark>

* <mark style="color:purple;">git:</mark> A palavra-chave que inicia todos os comandos do Git.
* <mark style="color:orange;">comando</mark>: A ação específica que você deseja executar.\
  Por exemplo, para inicializar um novo repositório Git, você digita <mark style="color:purple;">`git`</mark><mark style="color:orange;">`init`</mark>. Isso cria um novo repositório Git vazio.&#x20;
* <mark style="color:blue;">\[opções]:</mark> São como ajustes extras que você pode usar com um comando.\
  Por exemplo, quando você quer adicionar todas as mudanças feitas nos arquivos ao índice do Git, você usa o comando `git add` com a opção `all`: <mark style="color:purple;">`git`</mark><mark style="color:orange;">`add`</mark><mark style="color:blue;">`--all`</mark>. Isso significa que você está dizendo ao Git para adicionar todas as mudanças, não importa quais arquivos foram modificados.
* <mark style="color:green;">\[argumentos]</mark>: São as entradas sobre as quais você quer que o comando aja.\
  Por exemplo, se você quer adicionar um arquivo específico para o próximo commit, você diz ao Git qual arquivo usar como um argumento. Então, o Git sabe exatamente com o que você está lidando: <mark style="color:purple;">`git`</mark><mark style="color:orange;">`add`</mark><mark style="color:green;">`arquivo.txt`</mark>

A partir de agora, vamos adotar a seguinte convenção de cores para facilitar a identificação:

* <mark style="color:purple;">roxo para identificar git</mark>
* <mark style="color:orange;">laranja para identificar o comando</mark>
* <mark style="color:blue;">azul para identificar \[opções]</mark>
* <mark style="color:green;">verda para identificar \[argumentos]</mark>

Os colchetes `[ ]` indicam que tanto opções quanto argumentos são opcionais, ou seja, podem haver casos em que nem um nem outro são necessários. Um exemplo é o <mark style="color:purple;">`git`</mark><mark style="color:orange;">`init`</mark>, que veremos logo em seguida.&#x20;

{% hint style="info" %}
Se você digitar apenas <mark style="color:purple;">`git`</mark> no terminal, será exibida uma lista de comandos comuns do Git, como <mark style="color:orange;">`clone`</mark>, <mark style="color:orange;">`init`</mark>, <mark style="color:orange;">`add`</mark>, entre outros. Não se preocupe se parecer muita informação - você não precisa aprender tudo de uma vez. Esta lista simplesmente mostra quais comandos estão disponíveis e o que eles fazem.
{% endhint %}

Em resumo, toda interação com o Git é feita através do comando <mark style="color:purple;">`git`</mark>. Ele é o seu meio de comunicação com o Git e permite que você execute uma ampla variedade de tarefas de controle de versão em seu projeto.

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git/pt\_BR).
{% endhint %}
