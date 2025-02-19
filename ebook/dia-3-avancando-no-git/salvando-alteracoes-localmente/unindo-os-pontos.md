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

***

Em seguida, veremos um exemplo prático de como esses comandos funcionam.
