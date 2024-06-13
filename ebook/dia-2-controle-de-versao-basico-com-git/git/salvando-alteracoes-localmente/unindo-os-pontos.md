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

Os comandos: <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark>, <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> e <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark> são usados em conjunto para salvar uma foto do estado atual de um projeto Git. Os comandos <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> e <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> são utilizados para entender a evolução do repositório, mostrando o estado atual e o histórico de commits, respectivamente.

## Conceitos

### Estados de um arquivo

* **tracked** (rastreado): um arquivo que já foi preparado ou confirmado;
  * Estados de um arquivo **tracked**:
    * **Committed:** Tracked e sem mudanças - salvo.
    * **Modified:** Tracked e com mudanças.
    * **Staged:** Tracked, com mudanças prontas para commit.
* **untracked**  (não rastreado): um arquivo que não foi preparado nem confirmado; ou
* **ignored** (ignorado): um arquivo que o Git foi forçado a ignorar.

### Fazendo Alterações

* **git add** é usado para selecionar quais mudanças serão incluídas no próximo commit. Ele prepara as alterações para serem registradas no histórico do projeto.
* **git commit** após utilizar o <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> para preparar as mudanças, o <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark> salva essas alterações no repositório como uma "foto" do estado atual do projeto. Isso permite que você mantenha um registro claro do progresso do seu trabalho.
* As alterações são salvas localmente, permitindo que você trabalhe de forma independente.
* Git usa "snapshots" completos em vez de apenas diferenças, oferecendo mais segurança e um histórico claro do projeto.

### Visualização e Inspeção

São operações que podem ser executadas a qualquer momento e que auxiliam a entender o estado atual e o histórico do seu repositório

* **git status** exibe o estado atual do diretório de trabalho e da área de stage, mostrando quais arquivos foram modificados, quais estão prontos para serem confirmados (staged) e quais não estão sendo rastreados pelo Git.
* **git log** mostra o histórico de commits do repositório, exibindo detalhes como o autor, a data, a mensagem do commit e o identificador único (hash) do commit. É útil para navegar pelo histórico de commits do projeto e entender as mudanças ao longo do tempo.
* **git diff** exibe as diferenças entre as alterações feitas nos arquivos em relação ao último commit. É útil para visualizar as mudanças antes de prepará-las para um commit

### Gerenciamento de arquivos ignorados

* **.gitignore** é um arquivo usado pelo Git para determinar quais arquivos e diretórios devem ser ignorados, ou seja, não rastreados pelo Git. Isso é útil para evitar incluir no controle de versão arquivos temporários, arquivos de compilação ou arquivos contendo informações sensíveis.&#x20;

## Exemplo Prático:

#### **Inicializar um Repositório**

* Você cria um novo repositório com <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark>.
* O diretório agora contém um repositório Git vazio, pronto para rastrear arquivos.

#### **Criar um Arquivo**

* Você cria um arquivo, por exemplo, `arquivo.txt`.
* <pre class="language-bash"><code class="lang-bash"><strong>echo "conteúdo do arquivo" > arquivo.txt
  </strong></code></pre>
* O arquivo agora está "untracked" (não rastreado).

#### **Verificar Diferenças para o Último Commit**

* Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark> para ver as diferenças entre o estado atual e o último commit.
* Nada é mostrado, pois `arquivo.txt` é um arquivo novo e ainda não foi rastreado pelo Git. Além de não existir commits anteriores.

#### **Verificar o Status do Repositório**

* Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para ver o estado atual do diretório de trabalho e da área de stage.

```
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	arquivo.txt

nothing added to commit but untracked files present (use "git add" to track)
```

#### **Preparar o Arquivo para Commit**

* Você usa o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">arquivo.txt</mark>.
* `arquivo.txt` agora está "tracked" e "staged" (preparado para o commit).

#### **Verificar o Status do Repositório**

* Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para ver o estado atual do diretório de trabalho e da área de stage.

```bash
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   arquivo.txt
```

#### **Fazer o Commit**

* Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark> <mark style="color:blue;">-m "Adicionando uma linha ao arquivo.txt"</mark>.
* As mudanças em `arquivo.txt` são salvas no repositório, e o arquivo volta ao estado "tracked" e "committed" (rastreados e confirmados).

#### **Verificar o Histórico de Commits**

* Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> para ver o histórico de commits do repositório e encontra o seguinte commit

```
commit 59188653f06c2611125b91ac0d5d54ca2b427f62 (HEAD -> main)
Author: Cumbuca Dev <cumbucadev@gmail.com>
Date:   Wed Jun 12 22:03:33 2024 +0200

    Adicionando uma linha ao arquivo.txt
```

#### **Modificar um Arquivo**

* Você faz uma mudança em `arquivo.txt`.
* ```bash
  echo "mais conteúdo" >> arquivo.txt
  ```
* `arquivo.txt` agora está "tracked" e "modified" (rastreados e modificados).

#### **Verificar o Status do Repositório**

* Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para ver o estado atual do diretório de trabalho e da área de stage.

```
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

#### **Verificar Diferenças para o Último Commit**

* Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark> para ver as diferenças entre o estado atual e o último commit.

```
diff --git a/arquivo.txt b/arquivo.txt
index 9bbb6ca..cf44cf3 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1,2 @@
 conteúdo do arquivo
+mais conteúdo
```

#### **Preparar o Arquivo para Novo Commit**

* Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">arquivo.txt</mark>.
* `arquivo.txt` agora está "tracked" e "staged" novamente.

#### **Verificar o Status do Repositório**

* Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para ver o estado atual do diretório de trabalho e da área de stage.

```
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   arquivo.txt
```

#### **Fazer Novo Commit**

* Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark> <mark style="color:blue;">-m "Adicionando outra linha ao arquivo.txt"</mark>.
* As mudanças em `arquivo.txt` são salvas no repositório, e o arquivo volta ao estado "tracked" e "committed".

#### **Verificar o Histórico de Commits**

* Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> para ver o histórico de commits do repositório e encontra os dois commits

```
commit 7d0ec1760719c5cbba7dd8ac1009a6ea748ac1e0
Author: Cumbuca Dev <cumbucadev@gmail.com>
Date:   Wed Jun 12 22:08:01 2024 +0200

    Adicionando outra linha ao arquivo.txt

commit 59188653f06c2611125b91ac0d5d54ca2b427f62
Author: Cumbuca Dev <cumbucadev@gmail.com>
Date:   Wed Jun 12 22:03:33 2024 +0200

    Adicionando uma linha ao arquivo.txt

```

#### **Verificar o Status do Repositório**

* Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para ver o estado atual do diretório de trabalho e da área de stage.

```
On branch main
nothing to commit, working tree clean
```

> imagem dessa timeline
