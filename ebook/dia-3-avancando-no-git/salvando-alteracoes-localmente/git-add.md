---
description: >-
  Os comandos: git add, git status e git commit são usados em conjunto para
  salvar uma foto do estado atual de um projeto Git.
---

# git add

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> é usado para preparar mudanças feitas nos arquivos do seu projeto para serem incluídas no próximo commit.

## **Como Funciona**

1.  **Modificar arquivos**

    Primeiro, você faz alterações nos arquivos do seu projeto. Essas mudanças podem incluir a edição de arquivos existentes, a adição de novos arquivos ou a exclusão de arquivos.&#x20;
2. **Adicionar à Área de Preparação**\
   Quando você está satisfeito com as alterações e deseja incluí-las no próximo commit, você usa o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> para mover essas mudanças para a área de preparação (_staging area_).\
   \
   Exemplo:  Se você editou um arquivo chamado `index.html`, você usaria <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">index.html</mark> para preparar essas alterações.

## **Estrutura**

O formato base do comando <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> é:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">arquivo</mark>

## **Exemplos de uso**

* Adicionar um arquivo específico:
  * <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">index.html</mark>
  * Prepara as mudanças feitas em `index.html` para o próximo commit.
* Adicionar uma pasta específica:
  * <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">images/</mark>
  * Prepara todas as mudanças feitas dentro da pasta `images/` para o próximo commit.
* Adicionar vários arquivos de uma vez:
  * <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">index.html style.css script.js</mark>
  * Prepara as mudanças feitas em `index.html`, `style.css` e `script.js` para o próximo commit.
* Adicionar todos os arquivos modificados
  * <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">.</mark>
  * Prepara todas as mudanças feitas em todos os arquivos do diretório atual e seus subdiretórios para o próximo commit.

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> não altera o repositório de maneira significativa; ele apenas move as mudanças para a área de preparação (_staging area_). Isso informa ao Git que você deseja incluir essas alterações no próximo commit. No entanto, as mudanças não são realmente registradas no repositório até que você execute o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark>.&#x20;

Portanto, <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> é uma etapa intermediária que permite que você **revise** e **selecione** as mudanças antes de salvá-las permanentemente no repositório.

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`add`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-add/pt_BR).
{% endhint %}
