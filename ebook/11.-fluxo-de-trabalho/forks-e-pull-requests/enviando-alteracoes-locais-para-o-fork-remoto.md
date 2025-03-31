# Enviando Alterações Locais para o Fork Remoto

Até o momento, nenhuma alteração foi enviada ao fork no GitHub. Seguiremos um processo semelhante ao da seção [enviando-alteracoes-para-o-repositorio-remoto.md](../../9.-git-remoto/github-interagindo-com-o-repositorio-remoto-hello-world/enviando-alteracoes-para-o-repositorio-remoto.md "mention") para enviá-las.

## Passo a Passo

Agora, é hora de enviar as modificações para o repositório remoto. Para isso, utilizaremos o seguinte comando:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">push</mark> <mark style="color:green;">origin</mark> <mark style="color:green;">aprendizCumbucaDev</mark>

Em que:

* <mark style="color:purple;">git</mark>: Comando que usamos para interagir com o Git.
* <mark style="color:orange;">push</mark>: Sub-comando para enviar as alterações do seu computador para o repositório remoto.
* <mark style="color:green;">origin</mark>: Nome padrão que o Git dá ao repositório remoto.
* <mark style="color:green;">aprendizCumbucaDev</mark>: Nome da branch que estamos enviando para o GitHub.

```bash
git push origin aprendizCumbucaDev
```

Saída esperada (algo como):

```bash
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 10 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 381 bytes | 381.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'aprendizCumbucaDev' on GitHub by visiting:
remote:      https://github.com/aprendizCumbucaDev/PRimeiro-fork/pull/new/aprendizCumbucaDev
remote:
To github.com:aprendizCumbucaDev/PRimeiro-fork.git
 * [new branch]      aprendizCumbucaDev -> aprendizCumbucaDev
```

#### O que acontece depois de rodar esse comando?

1. O Git cria o branch `aprendizCumbucaDev` no fork remoto (caso ele ainda não exista).
2. As alterações que você fez e commitou localmente serão enviadas para esse branch no GitHub.

## Verificando o Fork Remoto

Acesse novamente a página do repositório do fork ou recarregue-a. Agora, você verá um novo painel indicando que a branch `aprendizCumbucaDev` recebeu alterações recentemente (exemplo: _"aprendizCumbucaDev had recent pushes X minutes ago"_).

Vamos alterar para o branch novo criado, para visualizar as modificações enviadas. Clique no botão de seleção de branch para alterar o branch atual e selecione `aprendizCumbucaDev`.

<figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/179_ Fork - Mudanças remotas.png" alt=""><figcaption></figcaption></figure>

Clique no arquivo **GARFO.md**, na lista de arquivos, para abrí-lo.

<figure><img src="../../.gitbook/assets/180_ Fork - Mudanças remotas 2.png" alt=""><figcaption></figcaption></figure>

E lá está a nova linha adicionada!

<figure><img src="../../.gitbook/assets/181_ Fork - Mudanças remotas 3.png" alt=""><figcaption></figcaption></figure>

Ainda no branch `aprendizCumbucaDev`, perceba alguns pontos:

* A **Barra de Sincronização com o Upstream** agora mostra um novo estado:

> **This branch is 1 commit ahead of cumbucadev/PRimeiro-fork:main.**
>
> Este branch está 1 commit à frente de cumbucadev/PRimeiro-fork:main.

* A janela de diálogo do **Botão Contribute** está diferente. Agora, existe um botão **Create pull request** (Criar pull request) e a mensagem diz:

> **This branch is 1 commit ahead of cumbucadev/PRimeiro-fork:main.**
>
> **Open a pull request to contribute your changes upstream.**
>
> Este branch está 1 commit à frente de cumbucadev/PRimeiro-fork:main. Abra um pull request para contribuir com suas alterações no repositório original.

<figure><img src="../../.gitbook/assets/182_ Fork - Mudanças remotas 4.png" alt=""><figcaption></figcaption></figure>

Note que, se voltarmos o branch **main**, o estado permanece exatamente o mesmo de quando criamos o **fork**:

> **This branch is up to date with cumbucadev/PRimeiro-fork:main.** Este branch está atualizado com cumbucadev/PRimeiro-fork:main.

Bem como a janela de diálogo do **Botão Contribute** não se alterou. Não há botão e a mensagem permanece a mesma:

> **This branch is not ahead of the upstream cumbucadev/PRimeiro-fork:main. No new commits yet. Enjoy your day!**
>
> Este branch não está à frente do upstream cumbucadev/PRimeiro-fork:main. Nenhum novo commit ainda. Aproveite o seu dia!"

<figure><img src="../../.gitbook/assets/183_ Fork - Mudanças remotas 5.png" alt=""><figcaption></figcaption></figure>

Isso ocorre porque a modificação foi enviada para o branch **aprendizCumbucaDev** e não para o **main**.&#x20;

***

Nas próximas seções, vamos aprender como sugerir alterações diretamente do branch `aprendizCumbucaDev` do fork para o branch `main` do repositório original. Além disso, abordaremos como atualizar o branch `main` do fork após a mesclagem. Se você estiver se sentindo um pouco confuso, não se preocupe — ao final do processo, o fluxo de trabalho ficará bem mais claro.
