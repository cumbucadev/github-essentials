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

# Inicializando um Repositório Local

## git init

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark> cria um novo repositório Git. Ele pode ser utilizado principalmente para dois fins:

* Para **converter** um projeto existente, não versionado, em um repositório Git ou;
* Para **inicializar** um novo repositório vazio.

_Imagens 1 e 2 init_

A maioria dos outros comandos do Git não está disponível fora de um repositório inicializado, então este é geralmente o **primeiro** comando que você executa em um novo projeto.

O quê o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark> faz por debaixo dos panos é criar uma pasta **oculta** chamada `.git` dentro da pasta de trabalho atual.

Essa pasta é onde o Git armazenará todos os dados sobre as versões dos arquivos, as alterações feitas e outras informações importantes para o controle de versão.&#x20;

> imagem: pasta .git apontando para várias coisas que ela contém

Se você excluir essa pasta, o Git perderá a capacidade de acessar e gerenciar todas as informações essenciais do seu repositório. Portanto, é crucial que essa pasta sempre esteja presente para garantir o funcionamento adequado do Git.

{% hint style="warning" %}
E por que a pasta`.git` foi citada acima como uma pasta **oculta**?&#x20;

Bem, qualquer diretório ou arquivo que começa com um ponto (.) é tratado como escondido. Isso significa que, por padrão, ele não aparecerá nas listagens comuns de diretórios.&#x20;

Por exemplo, se você usar o comando `ls` no terminal Unix, os diretórios e arquivos ocultos não aparecerão. Para vê-los, você precisa usar `ls -a`.

Essa ocultação do diretório `.git` tem várias vantagens. Primeiro, mantém sua pasta de trabalho limpa e organizada, o que é especialmente útil em projetos grandes com muitos arquivos e diretórios. Imagine o caos se você tivesse que lidar com todos esses arquivos extras visíveis o tempo todo!&#x20;

Além disso, esconder o diretório `.git` ajuda a protegê-lo contra modificações acidentais. **Mexer nos arquivos dentro do diretório `.git` manualmente pode corromper o repositório, causando sérios problemas no funcionamento do Git.**&#x20;
{% endhint %}

<figure><img src="../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

No exemplo acima, primeiro usamos o comando `ls`, que lista os arquivos e diretórios no diretório atual. Como você pode ver, inicialmente não há nada listado.

Depois, usamos o comando `ls -a`, que mostra todos os arquivos e diretórios, incluindo os ocultos (aqueles que começam com um ponto), e vemos apenas `.` e `..`.

Então, executamos o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark>, que inicializa um repositório Git vazio e cria o diretório oculto `.git`.

Quando usamos novamente o comando `ls`, não vemos nada de diferente, pois `.git` é oculto. Mas ao usar `ls -a` novamente, a pasta `.git` aparece!

### **Estru**tura

O formato base do comando <mark style="color:purple;">git</mark>  <mark style="color:orange;">init</mark> é:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark> <mark style="color:blue;">\[opções]</mark> <mark style="color:green;">\[diretório]</mark>

em que <mark style="color:green;">diretório</mark> (opcional) se refere ao caminho do diretório onde você quer inicializar o repositório. Se você omitir o diretório, o Git inicializará um repositório no diretório atual.

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`init`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-init/pt_BR).
{% endhint %}
