# Exemplo Prático

## **Cenário**

Teremos um repositório Git com um branch principal chamado `main` e um branch `nova-feature`. Ambos os branches modificam três arquivos:

* `arquivo1.txt` → **Conflito** (alterado em ambos os branches na mesma linha).
* `arquivo2.txt` → **Conflito** (alterado em ambos os branches na mesma linha).
* `arquivo3.txt` → **Sem conflito** (alterado apenas no branch `nova-feature`).

## Passo a Passo

### **Passo 1: Crie o Repositório e os Arquivos**

#### 🔹 Linux/macOS

```sh
git init merge-exemplo
cd merge-exemplo
echo "Versão inicial do arquivo 1" > arquivo1.txt
echo "Versão inicial do arquivo 2" > arquivo2.txt
echo "Versão inicial do arquivo 3" > arquivo3.txt
```

#### 🔹 Windows (CMD/PowerShell)

```sh
git init merge-exemplo
cd merge-exemplo
echo Versão inicial do arquivo 1 > arquivo1.txt
echo Versão inicial do arquivo 2 > arquivo2.txt
echo Versão inicial do arquivo 3 > arquivo3.txt
```

Agora, adicione os arquivos e faça o primeiro commit:

```sh
git add arquivo1.txt arquivo2.txt arquivo3.txt
git commit -m "Commit inicial com três arquivos"
```

### **Passo 2: Crie e Modifique o Branch `nova-feature`**

Crie o branch `nova-feature` e faça alterações nele:

```sh
git switch -c nova-feature
```

Altere os arquivos:

#### 🔹 Linux/macOS

```sh
echo "Alteração no branch nova-feature" > arquivo1.txt
echo "Alteração no branch nova-feature" > arquivo2.txt
echo "Nova linha no arquivo 3" >> arquivo3.txt
```

#### 🔹 Windows (CMD/PowerShell)

```sh
echo Alteração no branch nova-feature > arquivo1.txt
echo Alteração no branch nova-feature > arquivo2.txt
echo Nova linha no arquivo 3 >> arquivo3.txt
```

Adicione os arquivos alterados e faço o commit:

```sh
git add arquivo1.txt arquivo2.txt arquivo3.txt
git commit -m "Modificações no branch nova-feature"
```

### **Passo 3: Modifique o Branch `main`**

Volte para o branch `main` e faça outras alterações nos mesmos arquivos:

```sh
git switch main
```

Altere os arquivos:

#### 🔹 Linux/macOS

```sh
echo "Alteração no branch main" > arquivo1.txt
echo "Alteração no branch main" > arquivo2.txt
```

#### 🔹 Windows (CMD/PowerShell)

```sh
echo Alteração no branch main > arquivo1.txt
echo Alteração no branch main > arquivo2.txt
```

Adicione os arquivos alterados e faço o commit:

```sh
git add arquivo1.txt arquivo2.txt
git commit -m "Modificações no branch main"
```

### **Passo 4: Inicie o Merge**

Agora, tente mesclar o branch `nova-feature` no `main`:

```sh
git merge nova-feature
```

O Git responderá com um erro porque há conflitos:

```sh
Auto-merging arquivo3.txt
Merge made by the 'recursive' strategy.
Auto-merging arquivo1.txt
CONFLICT (content): Merge conflict in arquivo1.txt
Auto-merging arquivo2.txt
CONFLICT (content): Merge conflict in arquivo2.txt
Automatic merge failed; fix conflicts and then commit the result.
```

📌 O Git **mesclará automaticamente** o `arquivo3.txt`, mas os arquivos `arquivo1.txt` e `arquivo2.txt` precisarão ser resolvidos manualmente.

### **Passo 5: Verifique os Conflitos**

Rode o comando:

```sh
git status
```

Saída:

```
On branch main
You have unmerged paths.
  (fix conflicts and run "git commit")

Unmerged paths:
  (use "git add <file>..." to mark resolution)
	both modified:   arquivo1.txt
	both modified:   arquivo2.txt

Changes not staged for commit:
	modified:   arquivo3.txt
```

📌 O `arquivo3.txt` já foi mesclado automaticamente e está pronto. Os outros dois precisam ser corrigidos.

### **Passo 6: Resolva os Conflitos**

Agora você precisa corrigir os conflitos nos arquivos `arquivo1.txt` e `arquivo2.txt`.

Rode o comando:

```sh
git status
```

Saída:

```
On branch main
You have unmerged paths.
  (fix conflicts and run "git commit")

Unmerged paths:
  (use "git add <file>..." to mark resolution)
	both modified:   arquivo1.txt
	both modified:   arquivo2.txt
```

Isso significa que **ambos os arquivos foram modificados em ambos os branches na mesma parte do código**, e o Git não sabe qual versão escolher.

#### **Corrija o `arquivo1.txt`**

Se abrir `arquivo1.txt`, verá algo assim:

```
<<<<<<< HEAD
Alteração no branch main
=======
Alteração no branch nova-feature
>>>>>>> nova-feature
```

Aqui está o que essas marcações significam:

* `<<<<<<< HEAD` → Parte que veio do **branch atual (`main`)**
* `=======` → Separação entre as duas versões
* `>>>>>>> nova-feature` → Parte que veio do **branch `nova-feature`**

Agora, é preciso escolher como você quer resolver. Existem três opções:

1.  **Manter a versão do `main`**

    ```txt
    Alteração no branch main
    ```
2.  **Manter a versão do `nova-feature`**

    ```txt
    Alteração no branch nova-feature
    ```
3.  **Combinar as duas versões** (uma abordagem comum)

    ```txt
    Alteração combinada: main + nova-feature
    ```

Escolha a opção 3 e **remova os marcadores (`<<<<<<<`, `=======`, `>>>>>>>`)**.

Salve e feche o arquivo.

#### **Corrija o `arquivo2.txt`**

Abra `arquivo2.txt` e você verá algo parecido:

```
<<<<<<< HEAD
Alteração no branch main
=======
Alteração no branch nova-feature
>>>>>>> nova-feature
```

Novamente, existem três opções:

1.  **Manter a versão do `main`**

    ```txt
    Alteração no branch main
    ```
2.  **Manter a versão do `nova-feature`**

    ```txt
    Alteração no branch nova-feature
    ```
3.  **Combinar as duas versões**

    ```txt
    Alteração combinada no arquivo 2: main + nova-feature
    ```

Escolha a opção 3 e **removemos os marcadores (`<<<<<<<`, `=======`, `>>>>>>>`)**.

Salve e feche o arquivo.

Agora os arquivos corrigidos devem estar assim:

**`arquivo1.txt` (resolvido)**

```
Alteração combinada: main + nova-feature
```

**`arquivo2.txt` (resolvido)**

```
Alteração combinada no arquivo 2: main + nova-feature
```

### **Passo 7: Marque os Conflitos como Resolvidos**

Adicionamos os arquivos à área de stage para sinalizar ao Git que os arquivos não possuem mais conflitos:

```sh
git add arquivo1.txt arquivo2.txt
```

📌 O `arquivo3.txt` já está pronto, então você não precisa mexer nele.

### **Passo 8: Finalize o Merge**

Crie o commit de merge:

```sh
git commit -m "Merge do branch nova-feature"
```

Agora o merge está concluído! 🚀

### **Passo 9: Conferir o Histórico**

Rode:

```sh
git log --oneline
```

Saída esperada:

```
abc1234 Merge branch 'nova-feature'
def5678 Modificações no branch nova-feature
ghi9012 Modificações no branch main
jkl3456 Commit inicial com três arquivos
```

O commit `abc1234` representa o merge e contém:

* Os **arquivos corrigidos manualmente** (`arquivo1.txt` e `arquivo2.txt`).
* O **arquivo mesclado automaticamente** (`arquivo3.txt`).
