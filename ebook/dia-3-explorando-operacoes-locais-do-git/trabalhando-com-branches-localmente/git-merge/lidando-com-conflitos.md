# Lidando com Conflitos

## Conflito

Um **conflito no Git** ocorre quando ele não consegue mesclar automaticamente as alterações feitas em dois branches diferentes. Isso acontece quando ambos modificam a mesma parte do código e o Git não sabe qual alteração deve ser mantida.

Conflitos são comuns quando várias pessoas colaboram em um projeto. Por exemplo:

* Duas pessoas editam as mesmas linhas de um arquivo.
* Alguém exclui um arquivo enquanto outra pessoa faz alterações nele.
* Arquivos são movidos ou renomeados em diferentes branches.

O Git precisa da sua intervenção para resolver essas situações e decidir qual versão do código será mantida.

#### Situações em que um conflito pode ocorrer:

* **Alterações no mesmo trecho do código**: Quando o mesmo trecho de um arquivo é alterado em ambos os branches.
* **Alterações conflitantes**: Quando um arquivo foi removido em um branch e modificado no outro.
* **Mudanças na estrutura de diretórios**: Quando há conflitos na estrutura de diretórios, como arquivos movidos ou renomeados em ambos os branches.

#### Situações em que o Git consegue resolver sozinho:

* **Alterações em arquivos diferentes**: Quando as mudanças são feitas em arquivos diferentes, o Git pode mesclar automaticamente.
* **Alterações em partes diferentes do mesmo arquivo**: Quando as alterações acontecem em áreas separadas de um arquivo, o Git pode combinar automaticamente.
* **Arquivos adicionados em apenas um branch**: Se um arquivo foi adicionado em um branch, mas não existe no outro, o Git pode integrá-lo automaticamente.

### Por que o Git não Consegue Resolver o Conflito Sozinho?

O Git não pode decidir qual versão do código é a correta porque ele não entende a intenção e o contexto por trás das mudanças. Imagine um exemplo em que duas pessoas editaram a primeira linha de um mesmo arquivo:

* Alice alterou um texto para **"Boas vindas ao nosso sistema!"**
* Bob alterou o mesmo texto para **"Olá! Esperamos que goste do nosso produto."**

O Git não pode simplesmente escolher uma versão sem interferência humana, porque não sabe qual das mensagens é mais apropriada. Essa decisão precisa ser feita por uma pessoa, analisando o contexto.

## O Processo de Merge

Quando você executa o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">merge</mark>, o Git tenta combinar as alterações de dois branches. O processo de mesclagem pode resultar em três tipos de cenário:

1. **O Git não consegue iniciar o merge:** Caso haja mudanças no diretório de trabalho ou na área de staging do projeto atual, o merge não é iniciado.
2. **O merge ocorre sem conflitos**: O Git consegue combinar **todas** as mudanças automaticamente.
3. **O merge é interrompido por presença de conflito(s)**: O Git não consegue resolver automaticamente **uma ou mais** diferenças entre os branches e precisa da sua intervenção para resolver o conflito.

A seguir, vamos detalhar cada um desses casos.

## O Git não Consegue Iniciar o Merge

A inicialização do merge pode falhar se existirem mudanças no diretório de trabalho ou na área de staging do projeto atual.&#x20;

O Git não pode iniciar o merge, pois essas mudanças pendentes podem ser gravadas pelos commits que estão passando pelo processo de merge. Quando esse tipo de erro acontece, é por causa de conflitos com mudanças locais pendentes, não conflitos com outros desenvolvedores. A falha da inicialização do merge vai fazer com que a mensagem de erro a seguir seja exibida:

```sh
error: Entry '<...>' not uptodate. Cannot merge. (Changes in working directory)
```

Você precisará comitar ou descartar as suas mudanças locais para ter sucesso ao executar o merge novamente.

## Merge sem Conflito

Este é o caso descrito na seção anterior. Quando não há conflito, o Git consegue realizar o merge automaticamente e já cria um commit para você. Esse commit de merge é criado automaticamente, sem a necessidade de intervenção manual. A mensagem exibida será algo assim:

```bash
$ git merge nova-feature
Updating a1b2c3d..d4e5f6g
Fast-forward
 file1.txt |  2 +-
 file2.txt |  8 +++++---
 2 files changed, 5 insertions(+), 5 deletions(-)
```

Isso indica que o Git realizou um **merge**, onde as mudanças foram integradas sem conflitos. Ao inspecionar o log de commits, você conseguirá ver o novo commit realizado:

Ao verificar o histórico de commits, você verá o merge registrado.

```
$ git log --oneline --graph
*   d4e5f6g Merge branch 'nova-feature'
|\  
| * b2c3d4e Adiciona funcionalidade X
| * a1b2c3d Corrige bug na tela de login
|/
*   z1x2c3v Versão anterior do projeto
```

## Merge com Conflito

Quando um ou mais conflitos ocorrem durante o merge, o Git não pode decidir automaticamente qual versão do código deve ser mantida e marca o(s) conflito(s) para que você resolva manualmente.&#x20;

O Git interrompe o processo de merge e solicita que você edite os arquivos conflitantes. Você verá uma mensagem como essa:

```bash
$ git merge nova-feature
Auto-merging arquivo1.txt
CONFLICT (content): Merge conflict in arquivo1.txt.txt
Auto-merging arquivo2.txt
CONFLICT (content): Merge conflict in arquivo2.txt
Automatic merge failed; fix conflicts and then commit the result.
```

Essa mensagem indica que o merge automático falhou pois ocorreram conflitos nos arquivos `arquivo1.txt` e `arquivo2.txt`.

Diante deste cenário, você possui duas opção de como prosseguir:

1. **Cancelamento do merge**: Se você decidir que não deseja continuar o merge, é possível abortá-lo.
2. **Resolução dos conflitos:** explicar

### Cancelamento do Merge

Se você deseja cancelar o merge completamente e voltar ao estado anterior, use o comando:

```bash
$ git merge --abort
```

Esse comando desfaz todas as mudanças feitas durante o merge e retorna o repositório ao estado anterior à tentativa de mesclagem.

### **Resolução dos Conflitos**

O outro cenário possível é quando você deseja seguir em frente com o merge e irá resolver os conflitos manualmente.

Ao executar <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> você poderá consultar novamente quais os arquivos que possuem conflitos.

\*colocar um exeplo de git status aqui

Após identificar os arquivos com conflitos, você deve abri-los no seu editor de texto. O Git terá adicionado marcadores especiais para apontar as partes conflitantes do código, desta forma:

```
<<<<<<< HEAD
Código do branch atual.
=======
Código do branch que você está mesclando.
>>>>>>> nome-do-branch
```

* O trecho entre `<<<<<<< HEAD` e `=======` representa o código do seu branch atual.
* O trecho entre `=======` e `>>>>>>> nome-do-branch` mostra o código do branch que você está tentando mesclar.

Você precisa editar cada arquivo manualmente para escolher qual parte do código manter ou, se necessário, combinar as duas versões.&#x20;

Após editar o arquivo, remova os marcadores (`<<<<<<<`, `=======`, `>>>>>>>`) e salve as mudanças.

Ao resolver o conflito, use o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> para informar ao Git que o conflito foi resolvido em cada um dos arquivos:

```bash
$ git add arquivo1.txt arquivo2.txt
```

Ao resolver todos os conflitos, você pode finalizar a mesclagem realizando o commit de merge:

```bash
$ git commit -m "Merge branch 'nova-feature'"
```

Este commit irá incluir **todas** as mudanças do merge—tanto as resolvidas manualmente quanto as mescladas automaticamente.



{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades em como lidar com conflitos durante o comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`merge`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-merge/pt_BR).
{% endhint %}
