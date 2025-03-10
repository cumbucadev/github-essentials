# Salvando Alterações no Controle de Versão Local

Agora, vamos ver o processo completo de como salvar alterações no seu repositório Git local a partir de um novo branch. A prática de utilizar branches específicos para tarefas e correções ajuda a manter o fluxo de trabalho organizado e facilita a integração das modificações ao projeto principal.

## Passo a Passo

### Verificar estado atual do repositório

Antes de realizar qualquer modificação, é importante verificar o estado atual \`\`do repositório.

```bash
git status
▶ On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```

O estado atual do README.md é _**tracked**_ e _**modified**, &#x75;_&#x6D;a vez que o arquivo foi modificado anteriormente com a adição do GIF de boas vindas.

### Criar um novo branch

Uma boa prática, especialmente para iniciantes, é evitar modificar diretamente o branch principal (`main`). Para cada nova tarefa ou correção, é recomendável criar um branch específico. Essa abordagem é conhecida como **feature branch**, onde cada funcionalidade ou correção é desenvolvida separadamente antes de ser integrada ao projeto principal.

Crie um novo branch chamado `issue-1` e alterne para ele.

```bash
git switch -C issue-1
▶ Switched to a new branch 'issue-1'
```

### Verificar estado atual do repositório

Ao verificar o estado do repositório, agora a primeira linha retornada deve ser `On branch issue-1` ao a invés de `On branch main`.

```bash
git status
▶ On branch issue-1
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```

O estado atual do README.md permanece _**tracked**_ e _**modified**._

### Adicionar README.md

Agora, adicione o arquivo ao **staging area**, preparando-o para o commit.

```bash
git add README.md
```

### Verificar estado atual do repositório

Verifique novamente o estado do repositório.

```bash
git status
▶ On branch issue-1
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   README.md
```

O estado do `README.md` agora é **tracked e staged**.

### Git commit

Agora, salve as alterações no histórico do Git com um commit.

```bash
git commit -m 'Adicionando GIF de boas vindas ao README.md'
▶ [issue-1 29f1d56] Adicionando GIF de boas vindas ao README.md
 1 file changed, 2 insertions(+)
```

### Verificando o log do repositório

Para confirmar que o commit foi registrado corretamente, utilize o comando:

```bash
git log
```

Saída esperada (algo como):

```bash
commit cc230b01a7df96ab1c03a4fe5bc9d61b9eaa1df4 (HEAD -> issue-1)
Author: aprendizCumbucaDev <aprendiz.cumbucadev@gmail.com>
Date:   Mon Mar 10 17:09:41 2025 -0300

    Adicionando GIF de boas vindas ao README.md

commit 2e0d77fa56b7dc2b9c830c92d132143eacadcdf0 (origin/main, origin/HEAD, main)
Author: aprendizCumbucaDev <aprendiz.cumbucadev@gmail.com>
Date:   Mon Jan 20 14:44:57 2025 -0300

    Atualizando o README.md

    Adicionando o objetivo do repositório.

commit e140d961188e52636238ea60df81bc56f065a9ed
Author: aprendizCumbucaDev <aprendiz.cumbucadev@gmail.com>
Date:   Thu Jan 9 16:58:20 2025 -0300

    Initial commit

```

Note que o seu último commit aparece apenas no branch `issue-1`, indicado por `(HEAD -> issue-1)`. Isso significa que seu novo commit está apenas no branch `issue-1`, enquanto o branch `main` local ainda está alinhado com o repositório remoto.&#x20;

{% hint style="success" %}
Quer comprovar na prática?

* Mude de volta para o branch main com <mark style="color:purple;">git</mark> <mark style="color:orange;">switch</mark> <mark style="color:green;">main</mark>.
* Confira o log com <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark>.
* Você verá que o commit mais recente ainda **não está no `main`**, apenas no `issue-1`
* Retorne ao branch `issue-1` com <mark style="color:purple;">git</mark> <mark style="color:orange;">switch</mark> <mark style="color:green;">issue-1</mark> para continuar de onde paramos.
{% endhint %}

***

Após salvar suas alterações no controle de versão local, o próximo passo é enviá-las para o repositório remoto, o que abordaremos a seguir.
