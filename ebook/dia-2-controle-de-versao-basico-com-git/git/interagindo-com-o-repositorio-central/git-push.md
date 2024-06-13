# git push

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">push</mark> é usado para enviar suas mudanças locais para o repositório remoto central. É a maneira de compartilhar seu trabalho com outros colaboradores e garantir que suas contribuições sejam incorporadas ao projeto principal. Aqui está uma explicação simples de como ele funciona:

Quando você executa <mark style="color:purple;">git</mark> <mark style="color:orange;">push</mark>, o Git pega todos os commits que você fez e salvou em seu repositório local e os envia para o repositório remoto central. O repositório remoto central então é atualizado com seus commits, tornando suas mudanças disponíveis para outros colaboradores que também estão trabalhando no projeto.

### Estrutura

Esta é a estrutura base do comando <mark style="color:purple;">git</mark> <mark style="color:orange;">push</mark> que iremos utilizar neste momento

> <mark style="color:purple;">git</mark> <mark style="color:orange;">push</mark>

### **Exemplo de uso**

Depois de fazer algumas mudanças, adicionar arquivos e criar commits em seu repositório local, você quer compartilhar essas atualizações com a equipe. Aqui está o fluxo completo:

1. **Fazer Mudanças:**
   *   Você modifica um ou mais arquivos no seu projeto. Por exemplo, vamos modificar um arquivo chamado `index.html`:\
       \
       Original

       ```html
       <h1>Bem-vindo ao meu projeto</h1>
       ```

       \
       Modificado

       ```html
       <h1>Bem-vindo ao nosso projeto incrível</h1>
       ```
2. **Adicionar Arquivos:**
   *   Você escolhe quais mudanças incluir no próximo commit usando  <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark>:

       > <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">index.html</mark>
3. **Criar Commits:**
   *   Você salva essas mudanças em um commit. Podem ser feitos um ou mais commits:

       > <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark> <mark style="color:blue;">-m "Atualizar a mensagem de boas-vindas em index.html"</mark>
4. **Enviar Commits:**
   *   Finalmente, você envia todos os commits para o repositório remoto central usando:

       > <mark style="color:purple;">git</mark> <mark style="color:orange;">push</mark>

O que acontece quando você executa o <mark style="color:purple;">git</mark> <mark style="color:orange;">push</mark>:

1. **Conectar ao Remoto:** Git se conecta ao repositório remoto central.
2. **Enviar Commits:** Ele envia todos os seus commits locais para o repositório remoto central.
3. **Atualizar o Remoto:** O repositório remoto é atualizado com seus novos commits, tornando-os acessíveis para outros colaboradores.

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`push`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-push/pt\_BR).
{% endhint %}
