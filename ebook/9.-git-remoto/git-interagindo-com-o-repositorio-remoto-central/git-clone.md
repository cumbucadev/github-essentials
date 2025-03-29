---
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

# git clone

## Como Funciona

Quando um projeto já foi configurado em um repositório central, utiliza-se o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">clone</mark> para obter uma cópia de desenvolvimento do projeto em seu computador.

<div><figure><img src="../../.gitbook/assets/git clone 1 (1).png" alt=""><figcaption><p>Funcionamento do git clone - etapa 1</p></figcaption></figure> <figure><img src="../../.gitbook/assets/git clone 2 (1).png" alt=""><figcaption><p>Funcionamento do git clone - etapa 2</p></figcaption></figure></div>

Assim como o <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark>, clonar é geralmente uma operação única. Uma vez que uma pessoa tenha obtido uma cópia de trabalho, todas as operações de controle de versão e colaborações são gerenciadas por meio do seu repositório local.

Quando você **clona** um repositório do Git, significa que está copiando todos os arquivos e o histórico do projeto que está armazenado em um servidor remoto para o seu computador. Ao fazer isso, o Git já entende que aqueles arquivos fazem parte do controle de versão. Isso significa que:

* O Git **já está monitorando** todas as alterações nesses arquivos.
* Se você modificar um arquivo, o Git será capaz de detectar essa mudança.

Ou seja, ao clonar um repositório, você não precisa executar <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> nos arquivos copiados, porque o Git já os considera parte do repositório e os está rastreando desde o início.

## Estrutura

O formato base do comando <mark style="color:purple;">git</mark>  <mark style="color:orange;">clone</mark> que iremos utilizar aqui é:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">clone</mark> <mark style="color:green;">repositório</mark>

Em que:

* <mark style="color:green;">**repositório**</mark>: A URL do repositório que você deseja clonar, como por exemplo, a URL de um repositório remoto no GitHub.

## Exemplo de uso

Vamos analisar um exemplo que demonstra como clonar um repositório Git hospedado em um servidor remoto:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">clone</mark> <mark style="color:green;">ssh://maria@examplo.com/caminho/para/meu-projeto.git</mark>

* <mark style="color:purple;">git</mark> <mark style="color:orange;">clone</mark>: Este é o comando principal utilizado para clonar um repositório Git.
* <mark style="color:green;">ssh://</mark>: Isso indica que estamos usando o protocolo SSH para comunicar com o servidor. Não é preciso se preocupar com isso neste momento. Apenas compreender que é uma forma de comunicação do seu computador com o repositório central.
* <mark style="color:green;">maria@exemplo.com</mark>: Este é o nome de usuário e o endereço do servidor onde o repositório está hospedado. Neste caso, "maria" é o nome de usuário e "exemplo.com" é o nome do servidor.
* <mark style="color:green;">/caminho/para/meu-projeto.git</mark>: Este é o caminho para o diretório do repositório no servidor remoto. O Git clonará todo o conteúdo deste diretório para o seu computador local.

Ao executar esse comando, o Git fará uma conexão do tipo SSH com o servidor remoto, autenticando-se como o usuário "maria" e copiará todo o conteúdo do repositório localizado no caminho especificado para um diretório chamado "meu-projeto" no seu computador local. Sendo assim, agora existirá uma nova pasta no computador local chamada "meu-projeto" - que é a cópia da pasta original do servidor.

Para começar a trabalhar no projeto, basta entrar no novo diretório "meu-projeto" criado executando o comando `cd`&#x20;

```bash
cd meu-projeto
# Começar a trabalhar no projeto
```

## git init vs git clone

Os comandos <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark> e <mark style="color:purple;">git</mark> <mark style="color:orange;">clone</mark> podem ser facilmente confundidos. Em um nível mais alto, ambos são utilizados para "inicializar um novo repositório git".  No entanto, <mark style="color:purple;">git</mark> <mark style="color:orange;">clone</mark> depende do <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark>.&#x20;

O <mark style="color:purple;">git</mark> <mark style="color:orange;">clone</mark> é usado para criar uma cópia de um repositório existente. Internamente, <mark style="color:purple;">git</mark> <mark style="color:orange;">clone</mark> primeiro chama <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark> para criar um novo repositório. Em seguida, ele copia os dados do repositório existente e verifica um novo conjunto de arquivos de trabalho.

***

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`clone`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-clone/pt_BR).
{% endhint %}
