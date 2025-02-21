# Desfazendo Commits

Durante o desenvolvimento, é comum fazer commits e, em alguns momentos, perceber que algo precisa ser alterado. O Git oferece maneiras simples de desfazer commits feitos localmente, para que você possa corrigir ou ajustar as alterações antes de enviá-las para o repositório remoto.

Aqui vamos focar nas formas mais simples e seguras de desfazer commits, sem complicações, para que você possa corrigir seus erros sem afetar o histórico de forma complicada.

## Reverter um Commit Específico

Se você deseja desfazer um commit que não é o último, o Git oferece uma maneira simples de fazer isso sem complicação. A melhor maneira de reverter um commit antigo é usando o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">revert</mark>.

O <mark style="color:purple;">git</mark> <mark style="color:orange;">revert</mark> cria um novo commit que desfaz as alterações de um commit específico. Isso é útil quando você deseja desfazer algo que já foi feito, mas não quer afetar outros commits feitos depois desse.

Para reverter um commit antigo, você deve primeiro identificar o "hash" do commit que deseja desfazer. O hash é um identificador único para cada commit. Você pode visualizar o histórico de commits com o comando:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark>

Depois de encontrar o hash do commit, use o comando:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">revert</mark> <mark style="color:green;">hash-do-commit</mark>

O Git criará um novo commit que desfaz as alterações daquele commit. Assim, seu histórico de commits ficará preservado, e você ainda conseguirá corrigir o erro.

## Desfazer Últimos Commits

Se você cometeu um erro no último commit ou percebeu que não deveria ter feito aquele commit, você pode facilmente desfazê-lo. Existem duas formas principais de desfazer o último commit, dependendo do que você deseja fazer com as alterações:

### Desfazer o Último Commit, Mantendo as Alterações

Se você quer desfazer o commit, mas manter as alterações feitas nos arquivos (como se você tivesse apenas esquecido de fazer o commit), use o comando:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">reset</mark> <mark style="color:blue;">--soft</mark> <mark style="color:green;">HEAD\~1</mark>

Esse comando desfaz o último commit, mas mantém as alterações tanto na área de staging (onde ficam os arquivos prontos para o commit) quanto nos arquivos locais. Ou seja, é como se você tivesse feito o `git add`, mas ainda não tivesse feito o commit.

### Desfazer o Último Commit, Removendo as Alterações da Área de Staging

Se você já adicionou os arquivos à área de staging (usando `git add`), mas quer desfazer o commit e retirar os arquivos da área de staging, mantendo as alterações feitas nos arquivos, use:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">reset</mark> <mark style="color:green;">HEAD\~1</mark>

Esse comando desfaz o último commit e remove os arquivos da área de staging, mas as alterações ainda vão permanecer nos seus arquivos locais. Ou seja, os arquivos vão voltar para o estado "modificado", mas não estarão mais preparados para o commit.

### Desfazendo "n" Últimos Commits

Se você deseja desfazer mais de um commit, basta alterar o número após `HEAD~`. Por exemplo, para desfazer os últimos dois commits, você pode usar:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">reset</mark> <mark style="color:blue;">--soft</mark> <mark style="color:green;">HEAD\~2</mark>

Ou, se quiser também remover as mudanças da área de staging, use:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">reset</mark> <mark style="color:green;">HEAD\~2</mark>

Isso irá desfazer dois commits de uma vez, e você pode ajustar o número conforme necessário.

## Considerações Finais

* **Git Reset x Git Revert**:
  * Use o <mark style="color:purple;">git</mark> <mark style="color:orange;">reset</mark> para desfazer commits recentes, caso ainda não tenha enviado as alterações para o repositório remoto. É uma forma rápida de voltar para um estado anterior sem deixar rastros no histórico.
  * Use o <mark style="color:purple;">git</mark> <mark style="color:orange;">revert</mark> para desfazer commits antigos ou quando você precisa manter o histórico de commits intacto. Ele cria um novo commit que reverte as alterações feitas, o que é mais seguro caso você já tenha compartilhado os commits com outras pessoas.

{% hint style="info" %}
**Evite Modificar o Histórico Remoto**

Caso você já tenha enviado os commits para o repositório remoto, evite usar <mark style="color:purple;">git</mark> <mark style="color:orange;">reset</mark> para alterar o histórico. Modificar o histórico de commits pode causar problemas se outras pessoas já tiverem feito fetch ou pull dessas alterações.
{% endhint %}

Essas são as formas mais comuns e seguras de desfazer commits **locais** no Git, ideais para iniciantes que estão começando a se familiarizar com o controle de versões.&#x20;

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades dos comandos  <mark style="color:purple;">`git`</mark><mark style="color:orange;">`reset`</mark>  e <mark style="color:purple;">`git`</mark><mark style="color:orange;">`revert`</mark>, consulte as documentações oficiais:

* [documentação oficial git reset](https://git-scm.com/docs/git-reset/pt_BR)
* [documentação oficial git revert](https://git-scm.com/docs/git-revert/pt_BR)
{% endhint %}
