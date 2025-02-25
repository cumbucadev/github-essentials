# Exemplo Prático

## Passo a Passo

### 1. **Inicializar um Repositório Vazio**

Crie uma pasta no seu computador chamada de `meu-repo` .

```sh
mkdir meu-repo
```

Confira que a pasta foi criada com sucesso. A pasta `meu-repo` deve estar listada no resultado do comando.

**🔹 Linux/macOS**

```sh
ls -la
```

**🔹 Windows (CMD/PowerShell)**

```powershell
dir /a
```

Entre na pasta recém criada.

```sh
cd meu-repo
```

Inicialize essa pasta como um repositório com o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark>.

```sh
git init
▶ Initialized empty Git repository in /.../meu-repo/.git/
```

Confira que a pasta oculta `.git` foi criada. A pasta `.git` deve estar listada no resultado do comando.

**🔹 Linux/macOS**

```sh
ls -la
```

🔹 Windows (CMD/PowerShell)

```powershell
dir /a
```

***

<figure><img src="../../.gitbook/assets/36 exemplo inicializando repo.png" alt=""><figcaption><p>Inicializando um repositório vazio</p></figcaption></figure>

### **2. Verificar o Status do Repositório**

Execute o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para verificar o estado atual do diretório de trabalho e da área de stage.

```sh
git status
▶ On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
```

O resultado deve mostrar que não consta nada para ser commitado, nada na área de stage e não há nada que não está sendo rastreado.

### **3. Verificar o Histórico de Commits**

Execute o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> para verificar o histórico de commits do repositório

```sh
git log
▶ fatal: your current branch 'main' does not have any commits yet
```

Um erro será mostrado, uma vez que nenhum commit foi realizado ainda neste repositório.

### **4. Criar um Arquivo**

Crie um arquivo chamada `arquivo.txt` contendo a palavra "cumbuca". Você pode fazer isso via comando de terminal ou via um editor de texto. Este é o comando para criar via terminal.

```sh
echo cumbuca > arquivo.txt
```

Liste os arquivos na sua pasta novamente. O arquivo `arquivo.txt` deve estar listada no resultado do comando.

**🔹 Linux/macOS**

```sh
ls -la
```

**🔹 Windows (CMD/PowerShell)**

```powershell
dir /a
```

Verifique o conteúdo do arquivo. O resultado deve ser `cumbuca`.

**🔹 Linux/macOS**

```sh
cat arquivo.txt
▶ cumbuca
```

**🔹 Windows (CMD/PowerShell)**

```shell
type arquivo.txt
▶ cumbuca
```

### **5. Verificar o Status do Repositório**

Execute o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para verificar o estado atual do diretório de trabalho e da área de stage.

```sh
git status
▶ On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	arquivo.txt

nothing added to commit but untracked files present (use "git add" to track)
```

Perceba que o arquivo `arquivo.txt` agora deverá estar sinalizado como "**untracked**" (não rastreado).

### **6. Verificar Diferenças para o Último Commit**

Execute o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark> para ver as diferenças entre o estado atual e o último commit.

```sh
git diff
```

```
```

Nada será mostrado, pois o `arquivo.txt` é um arquivo novo e ainda não foi rastreado pelo Git. Além de não existir commits anteriores.

### **7. Preparar o Arquivo para Commit**

Execute o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">arquivo.txt</mark> para adicionar o arquivo à área de stage.

```sh
git add arquivo.txt
```

### **8. Verificar o Status do Repositório**

Execute o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para verificar o estado atual do diretório de trabalho e da área de stage.

```bash
git status
▶ On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   arquivo.txt
```

O arquivo `arquivo.txt` deve constar na área de stage agora, pronto para ser commitado. O seu estado atual é "tracked" e "staged" (rastreado e em área de preparação).

### **9. Fazer o Commit**

Use o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark> <mark style="color:blue;">-m "Adicionando arquivo arquivo.txt"</mark> para salvar a sua alteração.

```sh
git commit -m "Adicionando arquivo arquivo.txt"
▶ [main (root-commit) fc34c35] Adicionando arquivo arquivo.txt
 1 file changed, 1 insertion(+)
 create mode 100644 arquivo.txt
```

### **10. Verificar o Status do Repositório**

Execute o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para verificar o estado atual do diretório de trabalho e da área de stage.

```bash
git status
▶ On branch main
nothing to commit, working tree clean
```

O arquivo `arquivo.txt` foi salvo no repositório, e o arquivo voltou ao estado "tracked" e "committed" (rastreado e confirmado).

### **11. Verificar o Histórico de Commits**

Execute o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> para ver o histórico de commits do repositório.

```sh
commit fc34c35c38eb1b4ee19014b82a5572345165affc (HEAD -> main)
Author: Cumbuca Dev <cumbucadev@gmail.com>
Date:   Wed Jun 12 22:03:33 2024 +0200

    Adicionando arquivo arquivo.txt
```

Agora, o seu primeiro commit no repositório já está sendo listado.

### **12. Modificar um Arquivo**

Adicione uma nova linha ao final do arquivo `arquivo.txt` contendo a frase "dev". Você pode fazer isso via comando de terminal ou via um editor de texto. Este é o comando para criar via terminal

```sh
echo dev >> arquivo.txt
```

Verifique o conteúdo do arquivo. O resultado deve ser um texto contendo `cumbuca` na primeira linha e `dev` na segunda.

**🔹 Linux/macOS**

```sh
cat arquivo.txt
▶ cumbuca
dev
```

**🔹 Windows (CMD/PowerShell)**

```sh
type arquivo.txt
▶ cumbuca
dev
```

### **13. Verificar o Status do Repositório**

Execute o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para verificar o estado atual do diretório de trabalho e da área de stage.

```sh
git status
▶ On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

O arquivo `arquivo.txt` agora está "tracked" e "modified" (rastreado e modificado).

### **14. Verificar Diferenças para o Último Commit**

Execute o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark> para verificar as diferenças entre o estado atual e o último commit.

```sh
git diff
```

```sh
diff --git a/arquivo.txt b/arquivo.txt
index 9bbb6ca..cf44cf3 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1,2 @@
 cumbuca
+dev
```

### **15. Preparar o Arquivo para Novo Commit**

Execute o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">arquivo.txt</mark> para adicionar o arquivo novamente à área de stage.

```sh
git add arquivo.txt
```

### **16. Verificar o Status do Repositório**

Execute o comando usa <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para verificar o estado atual do diretório de trabalho e da área de stage.

```
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   arquivo.txt
```

O arquivo `arquivo.txt` agora está "tracked" e "staged" (rastreado e em área de preparação) novamente.

### **17. Fazer Novo Commit**

Execute o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark> <mark style="color:blue;">-m "Adicionando mais uma linha ao arquivo.txt"</mark> para salvar a sua alteração.

```sh
git commit -m "Adicionando mais uma linha ao arquivo.txt"
▶ [main 8af53f0] Adicionando mais uma linha ao arquivo.txt
 1 file changed, 1 insertion(+)
```

### **18. Verificar o Status do Repositório**

Execute o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para verificar o estado atual do diretório de trabalho e da área de stage.

```sh
git status
▶ On branch main
nothing to commit, working tree clean
```

O arquivo `arquivo.txt` foi salvo no repositório, e o arquivo voltou ao estado "tracked" e "committed" (rastreado e confirmado).

### **19. Verificar o Histórico de Commits**

Execute o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> para ver o histórico de commits do repositório. Você deve encontrar dois commits agora.

```sh
git log
```

```sh
commit 8af53f08777121067a34aa03269318c103493a79 (HEAD -> main)
Author: Camila Maia <cmaiacd@gmail.com>
Date:   Mon Feb 17 18:54:27 2025 -0300

    Adicionando mais uma linha ao arquivo.txt

commit fc34c35c38eb1b4ee19014b82a5572345165affc
Author: Camila Maia <cmaiacd@gmail.com>
Date:   Mon Feb 17 18:33:17 2025 -0300

    Adicionando arquivo arquivo.txt
```

### Visão Geral dos Estados do Arquivo

<figure><img src="../../.gitbook/assets/estados arquivo.txt.png" alt=""><figcaption><p>Estados do arquivo arquivo.txt</p></figcaption></figure>
