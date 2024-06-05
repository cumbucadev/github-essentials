---
description: >-
  Como iniciar um novo repositório Git usando o comando git init e como clonar
  repositórios existentes com o comando git clone. Essas são as etapas
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

em que <mark style="color:green;">diretório</mark> se refere ao caminho do diretório onde você quer inicializar o repositório. Se você omitir o diretório, o Git inicializará um repositório no diretório atual.

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`init`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-init/pt\_BR).
{% endhint %}

### git clone

Quando um projeto já foi configurado em um repositório central, utiliza-se o comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`clone`</mark> para obter uma cópia de desenvolvimento do projeto em seu computador.&#x20;

> imagem: explicando clone

Assim como o <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark>, clonar é geralmente uma operação única. Uma vez que um desenvolvedor tenha obtido uma cópia de trabalho, todas as operações de controle de versão e colaborações são gerenciadas por meio do seu repositório local.

#### Estrutura

O formato base do comando <mark style="color:purple;">git</mark>  <mark style="color:orange;">clone</mark> é:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">clone</mark> <mark style="color:blue;">\[opções]</mark> <mark style="color:green;">repositório \[diretório]</mark>

Em que:

* **`[opções]` (opcional)**: Várias opções que podem ser usadas para personalizar o comando de clonagem.
* **`repositório`**: A URL do repositório que você deseja clonar. Pode ser uma URL de um repositório remoto (como do GitHub) ou o caminho de um repositório local.
* **`[diretório]` (opcional)**: O nome do diretório onde o repositório clonado será armazenado. Se não for especificado, o Git usará o nome do repositório original.

#### Exemplo de uso

Vamos analisar um exemplo que demonstra como clonar um repositório Git hospedado em um servidor remoto:

<mark style="color:purple;">`git`</mark><mark style="color:orange;">`clone`</mark><mark style="color:green;">`ssh://maria@examplo.com/caminho/para/meu-projeto.git`</mark>

* <mark style="color:purple;">`git`</mark><mark style="color:orange;">`clone`</mark>: Este é o comando principal utilizado para clonar um repositório Git.
* <mark style="color:green;">`ssh://`</mark>: Isso indica que estamos usando o protocolo SSH para comunicar com o servidor. Não é preciso se preocupar com isso neste momento. Apenas compreender que é uma forma de comunicação do seu computador com o repositório central.
* <mark style="color:green;">`maria@exemplo.com`</mark>: Este é o nome de usuário e o endereço do servidor onde o repositório está hospedado. Neste caso, "joao" é o nome de usuário e "exemplo.com" é o nome do servidor.
* <mark style="color:green;">`/caminho/para/meu-projeto.git`</mark>: Este é o caminho para o diretório do repositório no servidor remoto. O Git clonará todo o conteúdo deste diretório para o seu computador local.

Ao executar esse comando, o Git fará uma conexão SSH com o servidor remoto, autenticando-se como o usuário "maria" e copiará todo o conteúdo do repositório localizado no caminho especificado para um diretório chamado "meu-projeto" no seu computador local.

> Imagem: mostrando o servidor com o usuário e a pasta e fazendo o clone
>
> Imagem: ls mostrando a nova pasta criada
>
> Imagem: ls -la mostrando o conteúdo da nova pasta criada

Para começar a trabalhar no projeto, basta entrar no novo diretório "meu-projeto" criado executando o comando `cd`&#x20;

```bash
cd meu-projeto
# Começar a trabalhar no projeto
```



{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`clone`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-clone/pt\_BR).
{% endhint %}

### git init vs git clone

Os comandos <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark> e <mark style="color:purple;">git</mark> <mark style="color:orange;">clone</mark> podem ser facilmente confundidos. Em um nível mais alto, ambos são utilizados para "inicializar um novo repositório git".  No entanto, <mark style="color:purple;">git</mark> <mark style="color:orange;">clone</mark> depende do <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark>.&#x20;

O <mark style="color:purple;">git</mark> <mark style="color:orange;">clone</mark> é usado para criar uma cópia de um repositório existente. Internamente, <mark style="color:purple;">git</mark> <mark style="color:orange;">clone</mark> primeiro chama <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark> para criar um novo repositório. Em seguida, ele copia os dados do repositório existente e verifica um novo conjunto de arquivos de trabalho.

> imagem: diferença entre o init e clone
