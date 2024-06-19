# git fetch

## Como Funciona

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">fetch</mark> é uma ferramenta essencial no Git que permite buscar atualizações de um repositório remoto para o seu repositório local, sem integrar essas mudanças automaticamente. Isso significa que você pode ver quais atualizações foram feitas no repositório remoto e decidir quando e como aplicá-las ao seu trabalho local.

Quando você executa <mark style="color:purple;">git</mark> <mark style="color:orange;">fetch</mark>, o Git se conecta ao repositório remoto e baixa todas as atualizações mais recentes. Essas mudanças são armazenadas localmente para você revisar, mas não afetam diretamente os arquivos em que você está trabalhando no momento.

É útil quando você quer ver o que mudou no repositório remoto antes de integrar essas mudanças ao seu trabalho. Ajuda a manter o seu repositório local atualizado com as referências remotas, sem modificar o que você está trabalhando no momento.

Imagine que você e seu colega estão trabalhando no mesmo projeto. Seu colega fez algumas mudanças e as enviou para o repositório remoto. Com o <mark style="color:purple;">git</mark> <mark style="color:orange;">fetch</mark>, você pode ver essas mudanças sem afetar o que você está fazendo. É como pegar uma atualização do que está acontecendo sem misturar isso com o seu código atual.

## Estrutura

Esta é a estrutura base do comando <mark style="color:purple;">git</mark> <mark style="color:orange;">fetch</mark> que iremos utilizar neste momento

> <mark style="color:purple;">git</mark> <mark style="color:orange;">fetch</mark>

## **Exemplo de uso**

1.  **Buscar Atualizações:**

    Primeiro, você busca as atualizações do repositório remoto:

    > <mark style="color:purple;">git</mark> <mark style="color:orange;">fetch</mark>

    Isso obtém as atualizações, mas não altera seus arquivos locais imediatamente.
2.  **Revisar o que foi Atualizado:**

    Você pode querer ver as diferenças entre o seu trabalho e as atualizações que foram buscados:

    > <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark> <mark style="color:green;">HEAD..FETCH\_HEAD</mark>

    Este comando compara o estado atual do seu repositório local com o estado depois de ter feito o fetch, mostrando as diferenças entre eles.
3.  **Mesclar as Atualizações:**

    Depois de revisar, você decide aplicar essas mudanças ao seu trabalho local:

    > <mark style="color:purple;">git</mark> <mark style="color:orange;">merge</mark> <mark style="color:green;">FETCH\_HEAD</mark>

    Isso integra as mudanças buscadas com o seu branch atual.

{% hint style="warning" %}
Não se preocupe se a sintaxe dos comandos nos itens 2 e 3 parecer complicada agora. Por enquanto, basta utilizá-los conforme descrito. Mais para frente, você entenderá melhor como e por que eles funcionam. Agora, para fins didáticos, usar esses comandos sem compreender todos os detalhes está perfeitamente bem.
{% endhint %}

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`fetch`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-fetch/pt\_BR).
{% endhint %}
