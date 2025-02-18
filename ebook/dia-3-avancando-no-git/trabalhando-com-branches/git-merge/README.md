---
description: >-
  O comando git merge é utilizado para combinar as mudanças de diferentes
  branches no Git, integrando alterações feitas em um branch para o branch
  atual.
---

# git merge

git pull, git push? local? remoto?

O <mark style="color:purple;">git</mark> <mark style="color:orange;">merge</mark> pega as alterações feitas em um branch específico e as aplica no branch em que você está atualmente. Isso acontece de forma automática, quando não há conflitos, ou pode exigir uma intervenção manual, caso ocorram conflitos entre as mudanças feitas.

Quando você realiza um merge, o Git tenta combinar as alterações automaticamente. Se houver diferenças que não podem ser resolvidas automaticamente (conflitos), o Git pedirá sua ajuda para escolher qual versão manter.

## Estrutura

Esta é a estrutura base do comando <mark style="color:purple;">git</mark> <mark style="color:orange;">merge</mark> que iremos utilizar neste momento

> <mark style="color:purple;">git</mark> <mark style="color:orange;">merge</mark> <mark style="color:green;">nome-do-branch</mark>

Em que:&#x20;

* <mark style="color:purple;">**git**</mark>**&#x20;**<mark style="color:orange;">**merge**</mark>: Este é o comando principal que invoca a ferramenta de mesclagem do Git.
* <mark style="color:green;">**nome-do-branch**</mark>: Especifica o branch que você deseja mesclar com o branch atual. Esse pode ser um branch local ou remoto.

Esse comando deve ser executado no **branch de destino**, ou seja, o branch onde você quer que as alterações sejam aplicadas.

## Exemplos de Uso

* Integrar um branch no branch principal
  * <mark style="color:purple;">git</mark> <mark style="color:orange;">switch</mark> <mark style="color:green;">main</mark>\
    <mark style="color:purple;">git</mark> <mark style="color:orange;">merge</mark> <mark style="color:green;">feature-x</mark>
  * O primeiro comando garantirá que o branch atual é o `main`. No segundo comando, **se o merge ocorrer sem conflitos**, o Git criará automaticamente um commit de merge para registrar a fusão dos branches. Isso irá aplicar as alterações do `feature-x` no `main`.

O merge funciona perfeitamente quando não há conflitos. No entanto, quando eles ocorrem, é necessário resolvê-los manualmente com atenção. Na próxima seção, vamos aprender como lidar com os conflitos que podem surgir durante o processo de merge.

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`merge`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-merge/pt_BR).
{% endhint %}

