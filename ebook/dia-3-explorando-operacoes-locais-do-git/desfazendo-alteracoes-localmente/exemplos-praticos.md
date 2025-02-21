# Exemplos Práticos

* [Antes do Commit](exemplos-praticos.md#antes-do-commit)
  * [Exemplo 1. Desfazer Alterações Não Adicionadas à Área de Staging](exemplos-praticos.md#exemplo-1.-desfazer-alteracoes-nao-adicionadas-a-area-de-staging)
  * [Exemplo 2. Remover Arquivos da Área de Staging](exemplos-praticos.md#exemplo-2.-remover-arquivos-da-area-de-staging)
* [Desfazendo Commits](exemplos-praticos.md#desfazendo-commits)
  * [Exemplo 3. Reverter um Commit Específico](exemplos-praticos.md#exemplo-3.-reverter-um-commit-especifico)
  * [Exemplo 4. Desfazendo os Dois Últimos Commits](exemplos-praticos.md#exemplo-4.-desfazendo-os-dois-ultimos-commits)
* [Alterando o Último Commit](exemplos-praticos.md#alterando-o-ultimo-commit)
  * [Exemplo 5. Modificar o Último Commit](exemplos-praticos.md#exemplo-5.-modificar-o-ultimo-commit)

## **Antes do Commit**

### **Exemplo 1. Desfazer Alterações Não Adicionadas à Área de Staging**

#### **Passo 1: Criar ou modificar um arquivo**

🔹 **Linux/macOS**

```bash
echo "Alteração" > arquivo.txt
```

🔹 **Windows (CMD/PowerShell)**

```bash
echo Alteração > arquivo.txt
```

#### **Passo 2: Verificar o estado atual do repositório**

Verifique os arquivos modificados que ainda não foram adicionados à área de staging.

```bash
git status
```

Saída esperada:

```sh
Modifications not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
  modified:   arquivo.txt
```

#### **Passo 3: Desfazer as alterações no arquivo**

Para restaurar o arquivo para seu estado original, utilize o comando:

```bash
git restore arquivo.txt
```

#### **Passo 4: Verificar novamente o estado do repositório**

Após desfazer as alterações, verifique novamente o estado do repositório.

```bash
git status
```

Saída esperada:

```sh
Nothing to commit, working tree clean
```

### **Exemplo 2. Remover Arquivos da Área de Staging**

#### **Passo 1: Criar ou modificar um arquivo**

🔹 **Linux/macOS**

```bash
echo "Alteração" > arquivo.txt
```

🔹 **Windows (CMD/PowerShell)**

```bash
echo Alteração > arquivo.txt
```

#### **Passo 2: Adicionar o arquivo à área de staging**

Adicione o arquivo à área de staging para prepará-lo para o commit.

```bash
git add arquivo.txt
```

#### **Passo 3: Verificar o estado da área de staging**

Verifique os arquivos que foram adicionados à área de staging.

```bash
git status
```

Saída esperada:

```sh
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
  new file:   arquivo.txt
```

#### **Passo 4: Remover o arquivo da área de staging**

Remova o arquivo da área de staging, mas sem apagar o arquivo do seu diretório de trabalho.

```bash
git reset HEAD arquivo.txt
```

#### **Passo 5: Verificar novamente o estado da área de staging**

Após remover o arquivo da área de staging, verifique o estado novamente.

```bash
git status
```

Saída esperada:

```sh
Modifications not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
  modified:   arquivo.txt
```

## Desfazendo Commits

### Exemplo 3. Reverter um Commit Específico

#### Passo 1: Criar um repositório de exemplo (se ainda não tiver um)

```sh
git init meu-repo
cd meu-repo
```

#### Passo 2: Fazer o commit de um arquivo novo

🔹 **Linux/macOS**

```sh
echo "Primeira versão" > arquivo.txt
git add arquivo.txt
git commit -m "Adicionando arquivo inicial"
```

🔹 **Windows (CMD/PowerShell)**

```sh
echo Primeira versão > arquivo.txt
git add arquivo.txt
git commit -m "Adicionando arquivo inicial"
```

#### Passo 3: Fazer mais três commits adicionando linhas ao mesmo arquivo

Adicione mais uma linha ao arquivo e faça o commit. Faça isso um total de três vez.

🔹 **Linux/macOS**

```sh
echo "Alteração 1" >> arquivo.txt
git add arquivo.txt
git commit -m "Alteração 1 no arquivo"

echo "Alteração 2" >> arquivo.txt
git add arquivo.txt
git commit -m "Alteração 2 no arquivo"

echo "Alteração 3" >> arquivo.txt
git add arquivo.txt
git commit -m "Alteração 3 no arquivo"
```

🔹 **Windows (CMD/PowerShell)**

```powershell
echo Alteração 1 >> arquivo.txt
git add arquivo.txt
git commit -m "Alteração 1 no arquivo"

echo Alteração 2 >> arquivo.txt
git add arquivo.txt
git commit -m "Alteração 2 no arquivo"

echo Alteração 3 >> arquivo.txt
git add arquivo.txt
git commit -m "Alteração 3 no arquivo"
```

#### Passo 4: Listar o histórico de commits

```sh
git log --oneline
```

Saída esperada:

```sh
a1b2c3 Alteração 3 no arquivo
d4e5f6 Alteração 2 no arquivo
g7h8i9 Alteração 1 no arquivo
j0k1l2 Adicionando arquivo inicial
```

#### Passo 5: Reverter um commit específico

Suponha que queremos desfazer "Alteração 2 no arquivo". Pegue o hash correspondente e execute o comando:

```sh
git revert d4e5f6
```

O Git abrirá um editor para confirmar a mensagem do commit de reversão. Salve e saia do editor.

#### Passo 6: Verificar o status do repositório

```sh
git status
```

Saída esperada:

```sh
No changes to commit, working tree clean
```

#### Passo 7: Verificar o histórico novamente

```sh
git log --oneline
```

Saída esperada:

```sh
x1y2z3 Revert "Alteração 2 no arquivo"
a1b2c3 Alteração 3 no arquivo
d4e5f6 Alteração 2 no arquivo
g7h8i9 Alteração 1 no arquivo
j0k1l2 Adicionando arquivo inicial
```

#### Passo 8: Verificar o conteúdo do arquivo

🔹 Linux/macOS

```sh
cat arquivo.txt
```

🔹 **Windows (CMD/PowerShell)**

```powershell
type arquivo.txt
```

Saída esperada:

```sh
Primeira versão
Alteração 1
Alteração 3
```

### Exemplo 4. Desfazendo os Dois Últimos Commits

#### Passo 1: Criar um repositório e entrar nele

```sh
git init outro-repo
cd outro-repo
```

#### Passo 2: Fazer o commit de um arquivo novo

🔹 **Linux/macOS**

```sh
echo "Versão inicial" > documento.txt
git add documento.txt
git commit -m "Versão inicial do documento"
```

🔹 **Windows (CMD/PowerShell)**

```sh
echo Versão inicial > documento.txt
git add documento.txt
git commit -m "Versão inicial do documento"
```

#### Passo 3: Fazer mais três commits adicionando linhas ao mesmo arquivo

Adicione mais uma linha ao arquivo e faça o commit. Faça isso um total de três vez.

🔹 **Linux/macOS**

```sh
echo "Mudança 1" >> documento.txt
git add documento.txt
git commit -m "Mudança 1 no documento"

echo "Mudança 2" >> documento.txt
git add documento.txt
git commit -m "Mudança 2 no documento"

echo "Mudança 3" >> documento.txt
git add documento.txt
git commit -m "Mudança 3 no arquivo"
```

🔹 **Windows (CMD/PowerShell)**

```sh
echo Mudança 1 >> documento.txt
git add documento.txt
git commit -m "Mudança 1 no documento"

echo Mudança 2 >> documento.txt
git add documento.txt
git commit -m "Mudança 2 no documento"

echo Mudança 3 >> documento.txt
git add documento.txt
git commit -m "Mudança 3 no documento"
```

#### Passo 4: Listar os commits

```sh
git log --oneline
```

Saída esperada:

```sh
z9y8x7 Mudança 3 no documento
w6v5u4 Mudança 2 no documento
t3s2r1 Mudança 1 no documento
q0p9o8 Versão inicial do documento
```

#### Passo 4: Desfazer os últimos 2 commits, mantendo as alterações

```sh
git reset --soft HEAD~2
```

Agora, as alterações feitas nesses commits ainda estão na área de staging, prontas para serem ajustadas.

#### Passo 5: Verificar o status do repositório

```sh
git status
```

Saída esperada:

```sh
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   documento.txt
```

#### Passo 6: Verificar novamente o histórico

```sh
git log --oneline
```

Saída esperada:

```sh
t3s2r1 Mudança 1 no documento
q0p9o8 Versão inicial do documento
```

Agora os commits desfeitos não estarão mais no histórico.

#### Passo 7: Verificar o conteúdo do arquivo

🔹 Linux/macOS

```sh
cat documento.txt
```

🔹 **Windows (CMD/PowerShell)**

```powershell
type documento.txt
```

Saída esperada:

```sh
Versão inicial
Mudança 1
Mudança 2
Mudança 3
```

A saída mostra que as linhas referentes às mudanças 2 e 3 ainda estão no arquivo, mesmo que os commits tenham sido desfeitos no Passo 4 com `git reset --soft HEAD~2`. Isso acontece porque o reset foi feito com a opção `--soft`, que remove os commits, mas mantém as alterações no arquivo e na área de staging.

#### Passo 8: Verificar o git diff do staged

```sh
git diff --staged
```

Saída esperada:

```sh
--- a/documento.txt
+++ b/documento.txt
@@ -1,2 +1,4 @@
 Versão inicial
 Mudança 1
+Mudança 2
+Mudança 3
(END)
```

O <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark> <mark style="color:green;">--staged</mark> mostra as mudanças que estão na área de staging, ou seja, prontas para serem commitadas novamente.&#x20;

A saída mostra que as linhas "Mudança 2" e "Mudança 3" foram adicionadas (`+` indica adição). Isso confirma que, apesar de os commits terem sido removidos do histórico, as alterações continuam armazenadas e podem ser reaproveitadas em um novo commit, editadas ou descartadas conforme necessário.

Resumindo, os commits foram apagados, mas as mudanças feitas neles continuam disponíveis para serem reutilizadas.

## Alterando o Último Commit

### Exemplo 5. Modificar o Último Commit

#### Passo 1: Criar um repositório e entrar nele

```sh
git init mais-um-repo
cd mais-um-repo
```

#### Passo 2: Fazer o commit de um arquivo novo

🔹 **Linux/macOS**

```sh
echo "Meu texto maneiro" > texto.txt
git add texto.txt
git commit -m "Adicionando texto.txt"
```

🔹 **Windows (CMD/PowerShell)**

```sh
echo Meu texto maneiro > texto.txt
git add texto.txt
git commit -m "Adicionando texto.txt"
```

#### **Passo 3:** Verificar o histórico de commits

```sh
git log
```

```sh
commit 4adbb23d9c7cbdc548e0cf87fd3385c4c3b83f86 (HEAD -> main)
Author: Cumbuca Dev <cumbucadev@gmail.com>
Date:   Fri Feb 21 09:29:00 2025 -0300

    Adicionando texto.txt
```

#### **Passo 4: Criar outro arquivo e esquecê-lo no commit**

Agora, criamos outro arquivo, mas esquecemos de adicioná-lo no commit anterior.

🔹 **Linux/macOS**

```sh
echo "Conteúdo importante" > esquecido.txt
```

🔹 **Windows (CMD/PowerShell)**

```sh
echo Conteúdo importante > esquecido.txt
```

#### **Passo 4: Adicionar o novo arquivo e modificar o último commit**

Agora, adicionamos o novo arquivo e modificamos o último commit para incluí-lo.

```sh
git add esquecido.txt
git commit --amend -m "Adicionando texto.txt e arquivo esquecido"
```

Saída esperada (algo como):

```sh
[main 15b10cf] Adicionando texto.txt e arquivo esquecido
 Date: Fri Feb 21 09:29:00 2025 -0300
 2 files changed, 2 insertions(+)
 create mode 100644 esquecido.txt
 create mode 100644 texto.txt
```

**Passo 5: Verificar o histórico de commits**

Para confirmar que a mensagem foi alterada e o novo arquivo foi incluído no commit, execute:

```sh
git log
```

Saída esperada (algo como):

```sh
commit 15b10cf054dbe24a8fc00422d82304b2528b3acb (HEAD -> main)
Author: Cumbuca Dev <cumbucadev@gmail.com>
Date:   Fri Feb 21 09:29:00 2025 -0300

    Adicionando texto.txt e arquivo esquecido
```

#### **Passo 6: Verificar os arquivos no commit**

Podemos verificar quais arquivos estão incluídos no commit alterado com o seguinte comando:

```sh
git show --name-only
```

Saída esperada:

```sh
ccommit 15b10cf054dbe24a8fc00422d82304b2528b3acb (HEAD -> main)
Author: Cumbuca Dev <cumbucadev@gmail.com>
Date:   Fri Feb 21 09:29:00 2025 -0300

    Adicionando texto.txt e arquivo esquecido

esquecido.txt
texto.txt
```

Agora o commit foi modificado para incluir o arquivo esquecido e tem uma mensagem atualizada.
