# Exemplos Práticos

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

***

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

