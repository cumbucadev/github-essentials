---
description: >-
  O comando git branch permite criar, listar e excluir branches no Git,
  facilitando o desenvolvimento paralelo e a organização do código.
---

# git branch

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">branch</mark> é usado para gerenciar branches no Git, permitindo a criação de novas ramificações, listagem das existentes e remoção de branches que não são mais necessários.

## **Suas Três Funcionalidades**

### **Criar um novo branch**

Quando você deseja desenvolver uma nova funcionalidade ou corrigir um bug sem interferir no código principal, você pode criar um novo branch usando <mark style="color:purple;">git</mark> <mark style="color:orange;">branch</mark>.

O branch criado começa com todo o conteúdo do branch atual. Ou seja, o novo branch será uma cópia exata do estado atual do branch de onde foi criado, incluindo arquivos e alterações não comitadas.

### **Listar branches existentes**

Para visualizar todos os branches disponíveis no repositório, o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">branch</mark> pode ser usado sem argumentos.

### **Excluir um branch**

Quando um branch não é mais necessário, ele pode ser removido para manter o repositório organizado.

## **Estrutura**

O formato base do comando <mark style="color:purple;">git</mark> <mark style="color:orange;">branch</mark> é:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">branch</mark> <mark style="color:blue;">\[opções]</mark> <mark style="color:green;">\[nome-do-branch]</mark>

## **Exemplos de uso**

* Criar um novo branch:
  * <mark style="color:purple;">git</mark> <mark style="color:orange;">branch</mark> <mark style="color:green;">feature-x</mark>
  * Cria um novo branch chamado `feature-x`, mas não muda para ele automaticamente. Permanece no mesmo branch que já estava.
* Listar branches existentes:
  * <mark style="color:purple;">git</mark> <mark style="color:orange;">branch</mark>
  * Exibe todos os branches locais, destacando o branch atual com um `*`.
* Excluir um branch local:
  * <mark style="color:purple;">git</mark> <mark style="color:orange;">branch</mark> <mark style="color:blue;">-d</mark> <mark style="color:green;">feature-x</mark>
  * Remove o branch `feature-x` se ele já foi mesclado (_merged_). Ou seja, o branch somente será deletado se todas as alterações feitas já foram integradas ao branch principal.
  * Caso o branch ainda tenha alterações não mescladas e você queira removê-lo de qualquer forma, utilize o comando:
    * <mark style="color:purple;">git</mark> <mark style="color:orange;">branch</mark> <mark style="color:blue;">-D</mark> <mark style="color:green;">feature-x</mark>
    * Isso **força** a exclusão do branch, descartando qualquer alteração que ainda não tenha sido integrada ao branch principal.

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">branch</mark> é essencial para um fluxo de trabalho eficiente no Git, permitindo que diferentes funcionalidades sejam desenvolvidas separadamente sem afetar o código principal.



{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`branch`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-branch/pt_BR).
{% endhint %}
