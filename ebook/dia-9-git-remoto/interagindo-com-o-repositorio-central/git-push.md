# git push

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">push</mark> é usado para enviar suas mudanças locais para o repositório remoto central. É a maneira de compartilhar seu trabalho com outros colaboradores e garantir que suas contribuições sejam incorporadas ao projeto principal.

Quando você executa <mark style="color:purple;">git</mark> <mark style="color:orange;">push</mark>, o Git pega todos os commits que você fez e salvou em seu repositório local e os envia para o repositório remoto central. O repositório remoto central então é atualizado com seus commits, tornando suas mudanças disponíveis para outros colaboradores que também estão trabalhando no projeto.

### Estrutura

Esta é a estrutura base do comando <mark style="color:purple;">git</mark> <mark style="color:orange;">push</mark> que iremos utilizar neste momento

> <mark style="color:purple;">git</mark> <mark style="color:orange;">push</mark> <mark style="color:green;">repositório-remoto</mark> <mark style="color:green;">branch</mark>

Em que:

* <mark style="color:purple;">git</mark>: Comando que usamos para interagir com o Git.
* <mark style="color:orange;">push</mark>: Sub-comando para enviar as alterações do seu computador para o repositório remoto.
*   <mark style="color:green;">repositório-remoto</mark>: É o nome do repositório remoto para onde você deseja enviar suas mudanças. No Git, o primeiro repositório remoto configurado em um projeto recebe, por padrão, o nome `origin`. Isso ocorre automaticamente ao clonar um repositório.

    Para simplificar, considere que, por enquanto, o repositório remoto será sempre chamado de `origin`.
* <mark style="color:green;">branch</mark>: O nome do branch no repositório remoto que você deseja enviar.

### **Exemplo de uso**

Depois de fazer algumas mudanças, adicionar arquivos e criar commits em seu repositório local, você quer compartilhar essas atualizações com a equipe. Aqui está o fluxo completo:

* Fazer Mudanças
  * Você modifica um ou mais arquivos no seu projeto. Por exemplo, vamos modificar o arquivo `README.md`
  *   Original

      ```html
      # Projeto Incrível
      ```
  *   Modificado

      ```html
      # Projeto Incrível

      Boas vindas ao meu projeto incrível!
      ```
* Adicionar Arquivos:
  * Você escolhe quais mudanças incluir no próximo commit usando  <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark>
  * <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">README.md</mark>
* Criar Commits:
  * Você salva essas mudanças em um commit. Podem ser feitos um ou mais commits
  * <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark> <mark style="color:blue;">-m "Adicionando mensagem de boas-vindas ao README.md"</mark>
* Enviar Commits:
  *   Finalmente, você envia todos os commits para o repositório remoto central usando:

      <mark style="color:purple;">git</mark> <mark style="color:orange;">push</mark> <mark style="color:green;">origin main</mark>

O que acontece quando você executa o <mark style="color:purple;">git</mark> <mark style="color:orange;">push</mark> <mark style="color:green;">origin main</mark>:

1. **Conectar ao Remoto**: O Git se conecta ao repositório remoto central.
2. **Enviar Commits**: Ele envia todos os seus commits locais para o branch `main` do repositório remoto central.
3. **Atualizar o Remoto**: O branch `main` do repositório remoto é atualizado com seus novos commits, tornando-os acessíveis para outros colaboradores.

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`push`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-push/pt_BR).
{% endhint %}
