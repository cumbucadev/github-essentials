# Alterando o Último Commit

O Git oferece diversas formas de modificar o último commit **local**, permitindo ajustes rápidos quando algo não sai como esperado. Vamos focar nas opções mais simples e úteis para iniciantes:&#x20;

* Corrigir a mensagem do commit
* Adicionar arquivos esquecidos
* Modificar o último commit, adicionando arquivos e mudando a mensagem

## **Modificar a Mensagem do Último Commit**

Se você deseja apenas alterar a mensagem do último commit, utilize:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark> <mark style="color:blue;">--amend -m "Nova mensagem do commit"</mark>

Isso irá modificar a mensagem do commit sem alterar seu conteúdo.

## **Adicionar Arquivos ao Último Commit**

Se você esqueceu de adicionar um arquivo antes do commit, utilize o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark> <mark style="color:blue;">--amend --no-edit</mark> após adicionar o arquivo:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">arquivo\_esquecido.txt</mark>
>
> <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark> <mark style="color:blue;">--amend --no-edit</mark>

Isso adiciona o arquivo ao commit sem modificar a mensagem.

## **Modificar o Último Commit, Adicionando Arquivos e Mudando a Mensagem**

Se você precisa adicionar um arquivo e também alterar a mensagem do último commit, use:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">arquivo\_esquecido.txt</mark>
>
> <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark> <mark style="color:blue;">--amend -m "Nova mensagem com arquivos adicionados"</mark>

Isso faz as duas coisas: adiciona o arquivo e altera a mensagem do commit.

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades da opção <mark style="color:blue;">`--amend`</mark> do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`commit`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-commit/pt_BR).
{% endhint %}
