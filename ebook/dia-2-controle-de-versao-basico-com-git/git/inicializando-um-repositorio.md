---
description: >-
  Como iniciar um novo repositório Git usando o comando git init. Essa etapa
  junto com o comando git clone, que será explicado mais a frente, são
  fundamentais para começar a trabalhar com o Git.
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

# Inicializando um Repositório

### git init

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark> cria um novo repositório Git. Ele pode ser utilizado principalmente para dois fins:

* Para **converter** um projeto existente, não versionado, em um repositório Git ou;
* Para **inicializar** um novo repositório vazio.

A maioria dos outros comandos do Git não está disponível fora de um repositório inicializado, então este é geralmente o **primeiro** comando que você executa em um novo projeto.

O quê o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark> faz por debaixo dos panos é criar uma pasta (diretório) chamada `.git` dentro da pasta de trabalho atual.

> imagem: ls de um projeto em que tem a pasta .git

Essa pasta é onde o Git armazenará todos os dados sobre as versões dos arquivos, as alterações feitas e outras informações importantes para o controle de versão.&#x20;

> imagem: pasta .git apontando para várias coisas que ela contém

Se você excluir essa pasta, o Git perderá a capacidade de acessar e gerenciar todas as informações essenciais do seu repositório. Portanto, é crucial que essa pasta sempre esteja presente para garantir o funcionamento adequado do Git.

#### Estrutura

O formato base do comando <mark style="color:purple;">git</mark>  <mark style="color:orange;">init</mark> é:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark> <mark style="color:blue;">\[opções]</mark> <mark style="color:green;">\[diretório]</mark>

em que <mark style="color:green;">diretório</mark> (opcional) se refere ao caminho do diretório onde você quer inicializar o repositório. Se você omitir o diretório, o Git inicializará um repositório no diretório atual.

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`init`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-init/pt\_BR).
{% endhint %}
