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

# Recaptulando...

Os comandos: <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark>, <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> e <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark> são usados em conjunto para salvar uma foto do estado atual de um projeto Git. Os comandos <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> e <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> são utilizados para entender a evolução do repositório, mostrando o estado atual e o histórico de commits, respectivamente.

### Exemplos Práticos:

#### **Exemplo inicializando um repositório do zero:**

1. **Inicializar um Repositório:**
   * Você cria um novo repositório com <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark>.
   * O diretório agora contém um repositório Git vazio, pronto para rastrear arquivos.
2. **Adicionar Arquivos ao Repositório:**
   * Crie ou adicione um arquivo, por exemplo, `arquivo.txt`.
   * <pre class="language-bash"><code class="lang-bash"><strong>echo "conteúdo do arquivo" > arquivo.txt    
     </strong></code></pre>
   * O arquivo agora está "untracked" (não rastreado).
3. **Preparar o Arquivo para Commit:**
   * Você usa o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">arquivo.txt</mark>.
   * `arquivo.txt` agora está "tracked" e "staged" (preparado para o commit).
4. **Verificar o Status do Repositório:**
   * Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para ver o estado atual do diretório de trabalho e da área de stage.
5. **Fazer o Commit:**
   * Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark> <mark style="color:blue;">-m "Adicionando uma linha ao arquivo.txt"</mark>.
   * As mudanças em `arquivo.txt` são salvas no repositório, e o arquivo volta ao estado "tracked" e "committed" (rastreados e confirmados).
6. **Verificar o Histórico de Commits:**
   * Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> para ver o histórico de commits do repositório e encontra o seguinte commit
     * Adicionando uma linha ao arquivo.txt
7. **Modificar um Arquivo:**
   * Você faz uma mudança em `arquivo.txt`.
   * ```bash
     echo "mais conteúdo" >> arquivo.txt
     ```
   * `arquivo.txt` agora está "tracked" e "modified" (rastreados e modificados).
8. **Preparar o Arquivo para Novo Commit:**
   * Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">arquivo.txt</mark>..
   * `arquivo.txt` agora está "tracked" e "staged" novamente.
9. **Verificar o Status do Repositório:**
   * Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para ver o estado atual do diretório de trabalho e da área de stage.
10. **Fazer Novo Commit:**
    * Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark> <mark style="color:blue;">-m "Adicionando outra linha ao arquivo.txt"</mark>.
    * As mudanças em `arquivo.txt` são salvas no repositório, e o arquivo volta ao estado "tracked" e "committed".
11. **Verificar o Histórico de Commits:**
    * Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> para ver o histórico de commits do repositório e encontra os dois commits
      * Adicionando uma linha ao arquivo.txt
      * Adicionando outra linha ao arquivo.txt

> imagem dessa timeline

#### Exemplo utilizando um repositório já existente

1. **Clonar um Repositório:**
   * Você clona um repositório com <mark style="color:purple;">git</mark> <mark style="color:orange;">clone</mark>
   * Todos os arquivos do repositório são agora "tracked" e "committed".
2. **Modificar um Arquivo:**
   * Você faz uma mudança em `arquivo.txt`.
   * `arquivo.txt` agora está "tracked" e "modified".
3. **Preparar o Arquivo para Commit:**
   * Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">arquivo.txt</mark>.
   * `arquivo.txt` agora está "tracked" e "staged".
4. **Verificar o Status do Repositório:**
   * Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> para ver o estado atual do diretório de trabalho e da área de stage.
5. **Fazer Commit:**
   * Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark> <mark style="color:blue;">-m "Alterando arquivo.txt"</mark>.
   * As mudanças em `arquivo.txt` são salvas no repositório e o arquivo volta ao estado "tracked" e "committed".
6. **Verificar o Histórico de Commits:**
   * Você usa <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> para ver o histórico de commits do repositório e encontra o seguinte commit
     * Alterando arquivo.txt

> imagem dessa timeline

### Conceitos

* Estados de um arquivo:
  * **Committed:** Tracked e sem mudanças - salvo.
  * **Modified:** Tracked e com mudanças.
  * **Staged:** Tracked, com mudanças prontas para commit.
* **git commit** salva suas mudanças como uma "foto" (_snapshot_) do momento atual do projeto, podendo incluir várias alterações de uma vez.
* **git add** é usado para escolher quais mudanças serão incluídas na "foto" (snapshot).
* As alterações são salvas localmente, permitindo que você trabalhe de forma independente.
* Git usa "snapshots" completos em vez de apenas diferenças, oferecendo mais segurança e um histórico claro do projeto.
* **git log**: Mostra o histórico de commits do repositório, exibindo detalhes como o autor, a data, a mensagem do commit e o identificador único (hash) do commit. É útil para navegar pelo histórico de commits do projeto e entender as mudanças ao longo do tempo.
* **git status**: Exibe o estado atual do diretório de trabalho e da área de stage, mostrando quais arquivos foram modificados, quais estão prontos para serem confirmados (staged) e quais não estão sendo rastreados pelo Git.
