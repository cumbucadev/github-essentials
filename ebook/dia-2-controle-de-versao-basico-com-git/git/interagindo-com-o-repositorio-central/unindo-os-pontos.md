---
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Unindo os Pontos

## Conceitos

* **git clone** é usado para criar uma cópia local de um repositório remoto. Ele baixa todo o histórico de commits e os arquivos do repositório para sua máquina local, permitindo que você comece a trabalhar com uma versão do projeto que pode ser modificada e atualizada.
* **git fetch** é utilizado para baixar todas as alterações feitas no repositório remoto para o seu repositório local. Ele traz as atualizações do repositório remoto, mas não as aplica automaticamente aos seus arquivos locais.
* **git push** envia as alterações locais que você fez no seu repositório para um repositório remoto. Isso é útil quando você deseja compartilhar suas alterações com outros colaboradores ou atualizar o repositório remoto com o seu trabalho.
* **git pull:** é uma combinação de <mark style="color:purple;">git</mark> <mark style="color:orange;">fetch</mark> e <mark style="color:purple;">git</mark> <mark style="color:orange;">merge</mark>. Ele baixa as alterações do repositório remoto para o seu repositório local e, em seguida, as mescla automaticamente com seus arquivos locais. Isso é útil quando você deseja atualizar seu repositório local com as últimas alterações do repositório remoto.

## Exemplo Prático

### Clonar um Repositório

Você clona um repositório com o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">clone</mark>.

```bash
$ git clone https://github.com/exemplo/repo.git
Cloning into 'repo'...
remote: Enumerating objects: 10, done.
remote: Counting objects: 100% (10/10), done.
remote: Compressing objects: 100% (8/8), done.
remote: Total 10 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (10/10), done.
```

Este comando cria uma cópia local do repositório remoto. As mensagens indicam o progresso do clone, incluindo a contagem e compressão de objetos.

### Verificar o Status

Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para ver o estado atual do diretório de trabalho e da área de stage.

```bash
$ cd repo
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

Mostra que o repositório local está atualizado com o repositório remoto, e que não há mudanças a serem commitadas.

### Modificar um Arquivo

Modifique um arquivo chamado `arquivo.txt`.

```bash
$ echo "Nova linha de conteúdo" >> arquivo.txt
```

Este comando adiciona uma nova linha ao arquivo `arquivo.txt`.

### Verificar Diferenças

Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark> para ver as diferenças.

```bash
$ git diff
diff --git a/arquivo.txt b/arquivo.txt
index e69de29..d95f3ad 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -0,0 +1 @@
+Nova linha de conteúdo
```

Mostra as diferenças entre o estado atual do arquivo e o último commit. Indica que `arquivo.txt` teve uma linha adicionada.

### Verificar o Status

Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para ver o estado atual do diretório de trabalho e da área de stage.

```bash
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

Indica que `arquivo.txt` foi modificado, mas ainda não foi adicionado à área de stage.

### Adicionar o Arquivo

Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">arquivo.txt</mark> para adicionar o arquivo ao stage.

```bash
git add arquivo.txt
```

Adiciona `arquivo.txt` à área de stage, preparando-o para o commit.

### Verificar o Status

Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para ver o estado atual do diretório de trabalho e da área de stage.

```bash
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   arquivo.txt
```

Mostra que `arquivo.txt` está preparado para ser commitado.

### Fazer Commit

Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark> <mark style="color:blue;">-m "Adiciona nova linha em arquivo.txt"</mark> para salvar as mudanças.

```bash
$ git commit -m "Adiciona nova linha em arquivo.txt"
[main 1a2b3c4] Adiciona nova linha em arquivo.txt
 1 file changed, 1 insertion(+)
```

Cria um novo commit com a mensagem descritiva "Adiciona nova linha em arquivo.txt", indicando que 1 arquivo foi alterado com 1 inserção.

### Verificar o Status

Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para verificar o estado após o commit.

```bash
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

Indica que o repositório local está 1 commit à frente do repositório remoto, e não há mudanças no diretório de trabalho.

### Ver Histórico de Commits com git log

Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> para ver o histórico de commits.

<pre class="language-bash"><code class="lang-bash">$ git log
commit 1a2b3c4d5e6f7g8h9i0j1k2l3m4n5o6p7q8r9s (HEAD -> main)
Author: Seu Nome &#x3C;seu.email@example.com>
Date:   Wed Jun 13 12:34:56 2024 -0300

    Alterando arquivo.txt

<strong>commit 0a1b2c3d4e5f6g7h8i9j0k1l2m3n4o5p6q7r8s9 (origin/main)
</strong>Author: Outro Desenvolvedor &#x3C;outro.email@example.com>
Date:   Wed Jun 13 11:00:00 2024 -0300

    Commit anterior feito por outra pessoa
</code></pre>

Exibe o histórico de commits, mostrando detalhes como o autor, data, e a mensagem do commit.

### Fazer Push

Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">push</mark> para enviar as mudanças para o repositório remoto.

```bash
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 400 bytes | 400.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/exemplo/repo.git
   e69de29..1a2b3c4  main -> main
```

Envia o commit local para o repositório remoto, atualizando-o com as mudanças locais.

### Verificar o Status

Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para verificar o estado após o push.

```bash
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

Mostra que o branch local está atualizado com o branch remoto e não há mudanças no diretório de trabalho.

### Ver Histórico de Commits com git log

Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> para ver o histórico de commits novamente.

```bash
$ git log
commit 1a2b3c4d5e6f7g8h9i0j1k2l3m4n5o6p7q8r9s (HEAD -> main, origin/main)
Author: Seu Nome <seu.email@example.com>
Date:   Wed Jun 13 12:34:56 2024 -0300

    Adiciona nova linha em arquivo.txt
```

Exibe o histórico de commits, mostrando que o commit local foi enviado para o repositório remoto.

### Buscar Mudanças Remotas (fetch)

Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">fetch</mark> para buscar as mudanças do repositório remoto.

```bash
$ git fetch
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (1/1), done.
remote: Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (2/2), done.
From https://github.com/exemplo/repo
   1a2b3c4..5e6f7g8  main       -> origin/main
```

Busca as mudanças do repositório remoto sem mesclá-las automaticamente no branch atual.

### Verificar Qual foi a Mudança

Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark> <mark style="color:green;">HEAD..FETCH\_HEAD</mark> para ver as diferenças entre o branch local e o branch remoto.

```bash
$ git diff HEAD..FETCH_HEAD
diff --git a/novo-arquivo.txt b/novo-arquivo.txt
new file mode 100644
index 0000000..e69de29
--- /dev/null
+++ b/novo-arquivo.txt
@@ -0,0 +1 @@
+Conteúdo do novo arquivo
```

Mostra as diferenças entre o último commit no branch local e as mudanças buscadas do repositório remoto.

### Mesclar Mudança

Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">merge</mark> <mark style="color:green;">FETCH\_HEAD</mark> para mesclar as mudanças do branch remoto no branch local.

```bash
$ git merge FETCH_HEAD
Updating 1a2b3c4..5e6f7g8
Fast-forward
 novo-arquivo.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 novo-arquivo.txt
```

Mescla as mudanças buscadas do branch remoto no branch local.

### Ver Histórico de Commits com git log

Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> para ver o histórico de commits novamente.

```bash
$ git log
commit 5e6f7g8h9i0j1k2l3m4n5o6p7q8r9t0u (HEAD -> main, origin/main)
Author: Outro Desenvolvedor <outro.email@example.com>
Date:   Wed Jun 13 13:00:00 2024 -0300

    Adiciona nova funcionalidade

commit 1a2b3c4d5e6f7g8h9i0j1k2l3m4n5o6p7q8r9s (HEAD -> main, origin/main)
Author: Seu Nome <seu.email@example.com>
Date:   Wed Jun 13 12:34:56 2024 -0300

    Adiciona nova linha em arquivo.txt

commit 0a1b2c3d4e5f6g7h8i9j0k1l2m3n4o5p6q7r8s9 (origin/main)
Author: Outro Desenvolvedor <outro.email@example.com>
Date:   Wed Jun 13 11:00:00 2024 -0300

    Commit anterior feito por outra pessoa
```

### Buscar e Mesclar Mudanças Remotas (pull)

Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">pull</mark> para buscar e mesclar mudanças remotas em um único comando.

```bash
$ git pull
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (2/2), done.
From https://github.com/exemplo/repo
   5e6f7g8..9h0j1k2  main       -> origin/main
Updating 5e6f7g8..9h0j1k2
Fast-forward
 outro-arquivo.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 outro-arquivo.txt
```

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">pull</mark> combina <mark style="color:purple;">git</mark> <mark style="color:orange;">fetch</mark> e <mark style="color:purple;">git</mark> <mark style="color:orange;">merge</mark>, buscando e mesclando as mudanças remotas no branch local. A mensagem mostra que o arquivo `outro-arquivo.txt` foi adicionado no branch remoto e agora foi mesclado no branch local.

### Ver Histórico de Commits com git log

Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> para ver o histórico de commits novamente.

```bash
$ git log
commit 9h0j1k2l3m4n5o6p7q8r9s0t1u2v3w4x5y6z7a8 (HEAD -> main, origin/main)
Author: Mais Outro Desenvolvedor <mais.outro.email@example.com>
Date:   Wed Jun 13 14:00:00 2024 -0300

    Adiciona outro arquivo

commit 5e6f7g8h9i0j1k2l3m4n5o6p7q8r9t0u (HEAD -> main, origin/main)
Author: Outro Desenvolvedor <outro.email@example.com>
Date:   Wed Jun 13 13:00:00 2024 -0300

    Adiciona nova funcionalidade

commit 1a2b3c4d5e6f7g8h9i0j1k2l3m4n5o6p7q8r9s (HEAD -> main, origin/main)
Author: Seu Nome <seu.email@example.com>
Date:   Wed Jun 13 12:34:56 2024 -0300

    Adiciona nova linha em arquivo.txt

commit 0a1b2c3d4e5f6g7h8i9j0k1l2m3n4o5p6q7r8s9 (origin/main)
Author: Outro Desenvolvedor <outro.email@example.com>
Date:   Wed Jun 13 11:00:00 2024 -0300

    Commit anterior feito por outra pessoa
```

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> mostra o histórico completo de commits no branch atual. Neste caso, exibe três commits: o commit mais recente adicionando `outro-arquivo.txt`, o commit anterior adicionando uma nova funcionalidade e o commit inicial adicionando uma linha a `arquivo.txt`.



> imagem dessa timeline
