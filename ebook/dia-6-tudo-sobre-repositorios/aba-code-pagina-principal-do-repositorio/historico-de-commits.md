# Histórico de Commits

Após realizar sua primeira alteração no repositório, é hora de explorar o histórico de mudanças. No GitHub, você pode acompanhar o histórico de commits organizados em ordem cronológica, do mais recente ao mais antigo. Esse recurso, semelhante ao comando `git log` no terminal, é essencial para entender a evolução do projeto, identificar quem contribuiu e analisar o que foi modificado ao longo do tempo.

## **Como Acessar o Histórico de Commits**

Você pode acessar o histórico de commits de duas maneiras:

### **Via Página Principal do Repositório**

No cabeçalho da lista de arquivos, clique no número de commits (ex: 2 commits) para abrir a página de histórico.

<figure><img src="../../.gitbook/assets/Botão para Histórico de Commits.png" alt=""><figcaption></figcaption></figure>

### Via Link

Acesse diretamente através do link:&#x20;

* https://github.com/`usuário`/`nomeDoRepositório`/commits
* Exemplo: [https://github.com/aprendizCumbucaDev/hello-world/commits/](https://github.com/aprendizCumbucaDev/hello-world/commits/)

## Página de Histórico de Commits

Na página de histórico, os commits são listados em ordem cronológica. A interface exibe uma linha do tempo das alterações do repositório.

<figure><img src="../../.gitbook/assets/Histórico de Commits.png" alt=""><figcaption><p>Página de Histórico de Commits</p></figcaption></figure>

### Filtros Disponíveis

No topo da página, você encontra opções para filtrar os commits:

<figure><img src="../../.gitbook/assets/Histórico de Commits - Filtros.png" alt=""><figcaption><p>Filtros de Commits</p></figcaption></figure>

#### **Branch**

Filtra os commits de uma branch específica. Isso é útil para ver o histórico de uma linha de desenvolvimento separadamente.

Equivalente no Git:&#x20;

```bash
git log <nome-da-branch> 
```

Exemplo:

```bash
git log main
```

_Exibe apenas os commits feitos na branch `main`._

#### **Autor**

Mostra os commits realizados por um autor específico. Isso é útil para revisar alterações feitas por um colaborador.

Equivalente no Git:

```bash
git log --author="email-do-usuário"
```

Exemplo:

```bash
git log --author="aprendiz.cumbucadev@gmail.com"
```

Exibe apenas os _commits_ realizados pelo autor com o e-mail `aprendiz.cumbucadev@gmail.com`.

#### **Data**

Permite visualizar commits dentro de um intervalo de tempo definido. Esse filtro é ideal para analisar alterações feitas em um período específico.

Equivalente no Git:

```bash
git log --since AAAA-MM-DD --until AAAA-MM-DD
```

Exemplo:

```bash
git log --since 2025-01-10 --until 2025-01-16
```

_Retorna apenas commits efetuados entre 10 de janeiro de 2025 e 16 de janeiro de 2025._

***

Esses filtros ajudam a localizar informações específicas no histórico de commits, tornando a navegação e a análise mais eficientes.

### Informações de cada commit

Cada commit listado exibe:

* **Título do Commit**: Uma descrição breve da alteração, equivalente à mensagem fornecida no comando `git commit -m "mensagem"`.
* **Autoria e Data**: O nome de usuário de quem realizou o commit e o momento exato da alteração.
* **Hash do Commit**: Um identificador único gerado pelo Git para cada commit. Esse hash é essencial para comandos como `git checkout` e `git revert`.

<figure><img src="../../.gitbook/assets/Histórico de Commits - linha.png" alt=""><figcaption><p>Um commit</p></figcaption></figure>

### Interações com um commit

<figure><img src="../../.gitbook/assets/Histórico de Commits - linha açoes.png" alt=""><figcaption><p>Informações de um Commit</p></figcaption></figure>

* **Expandir Descrição**: Caso o commit tenha uma descrição longa, você pode expandi-la clicando no botão de expansão dos três pontinhos: `...`
* **Copiar Hash do Commit**: Use o botão de cópia ao lado do hash para copiar o identificador único.
* **Acessar Página do Commit**: Clique no título ou no hash do commit para acessar a página específica daquele commit.

## Página do Commit

Na página do commit, você verá detalhes sobre as alterações, com a mesma estrutura do comando `git diff` no terminal. Nela, você encontrará uma lista dos arquivos que foram modificados, adicionados ou removidos, com as alterações detalhadas linha por linha. Linhas adicionadas aparecem destacadas em verde com um sinal de `+`, enquanto as linhas removidas são exibidas em vermelho com um sinal de `-`.&#x20;

<figure><img src="../../.gitbook/assets/Detalhe de um Commit.png" alt=""><figcaption><p>Página do Commit</p></figcaption></figure>

Se o commit contém arquivos no formato Markdown, você pode clicar no botão de documento no canto superior direito para visualizar o arquivo já formatado diretamente no GitHub.

<figure><img src="../../.gitbook/assets/Detalhe de um Commit - view rendered md (1).png" alt=""><figcaption><p>Visualização de Markdown Formatado na Página do Commit</p></figcaption></figure>

## Explorando o Repositório em um Ponto Específico

Na página de histórico de commits, ao final de cada linha, você encontrará um botão com o ícone `< >`. Clicando nele, você será levado a uma visualização do repositório exatamente como ele estava no momento daquele commit. Isso permite que você explore a versão do repositório naquele ponto específico no tempo, facilitando a análise das mudanças realizadas até ali.

<figure><img src="../../.gitbook/assets/Histórico de Commits - navegar commit específico.png" alt=""><figcaption><p>Navegar pelo Repositório em um Ponto Específico</p></figcaption></figure>

Ao clicar no botão, o GitHub ajusta a visualização para refletir o estado do repositório naquele commit. No canto da página, a branch será alterada para o hash do commit, indicando que você está visualizando uma versão específica do projeto.

<figure><img src="../../.gitbook/assets/Repo em um commit específico.png" alt=""><figcaption><p>Repositório no Ponto do Commit <code>e140d96</code></p></figcaption></figure>

Perceba que neste ponto, ainda não havia sido aplicada a modificação recém feita no README. Isso ocorre porque estamos no ponto em que apenas o primeiro commit havia sido feito. O segundo ainda não existia nesse momento.

Este mesmo comportamento pode ser obtido no terminal através do comando `git checkout <hash-do-commit>`. Neste caso, o exato comando seria `git checkout e140d96` .

Essa funcionalidade é fundamental para investigar implementações passadas, identificar problemas em commits anteriores e comparar versões ou alterações no repositório.
