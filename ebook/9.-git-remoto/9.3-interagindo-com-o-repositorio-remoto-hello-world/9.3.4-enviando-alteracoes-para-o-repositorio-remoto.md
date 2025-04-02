# Enviando Alterações para o Repositório Remoto

Até o momento, nenhuma alteração foi enviada ao repositório remoto no GitHub. Você pode verificar isso acessando seu repositório, onde o número de branches e commits permanecerá inalterado.

<figure><img src="../../.gitbook/assets/66_ Repo before push.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/67_ Commits before push.png" alt=""><figcaption></figcaption></figure>

## Enviando as Modificações

Agora, é hora de enviar as modificações para o repositório remoto. Para isso, utilizaremos o seguinte comando:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">push</mark> <mark style="color:green;">origin</mark> <mark style="color:green;">issue-1</mark>

Em que:

* <mark style="color:purple;">git</mark>: Comando que usamos para interagir com o Git.
* <mark style="color:orange;">push</mark>: Sub-comando para enviar as alterações do seu computador para o repositório remoto.
* <mark style="color:green;">origin</mark>: Nome padrão que o Git dá ao repositório remoto.
* <mark style="color:green;">issue-1</mark>: Nome da branch que estamos enviando para o GitHub.

```bash
git push origin issue-1
```

Saída esperada (algo como):

```bash
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 10 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 626 bytes | 626.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'issue-1' on GitHub by visiting:
remote:      https://github.com/aprendizCumbucaDev/hello-world/pull/new/issue-1
remote:
To github.com:aprendizCumbucaDev/hello-world.git
 * [new branch]      issue-1 -> issue-1
branch 'issue-1' set up to track 'origin/issue-1'
```

#### O que acontece depois de rodar esse comando?

1. O Git cria o branch `issue-1` no repositório remoto (caso ele ainda não exista).
2. As alterações que você fez e comitou localmente serão enviadas para esse branch no GitHub.

## Verificando o Repositório Remoto Central

Acesse novamente a página do repositório no GitHub ou recarregue-a. Agora, você verá um novo painel indicando que a branch `issue-1` recebeu alterações recentemente (exemplo: _"issue-1 had recent pushes X minutes ago"_). Falaremos mais sobre isso no próximo capítulo.

Além disso, perceba que o número de branches agora aumentou, passando de 1 para 2.

<figure><img src="../../.gitbook/assets/69_ Repo após push.png" alt=""><figcaption></figcaption></figure>

Para visualizar as modificações, clique no botão de seleção de branch para alterar o branch atual.

<figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/70_ Repo após push 2.png" alt=""><figcaption></figcaption></figure>

Escolha a opção `issue-1.`

<figure><img src="../../.gitbook/assets/71_ Repo após push 3.png" alt=""><figcaption></figcaption></figure>

Agora você está vendo a versão do seu repositório no branch `issue-1`. Veja qual foi o último commit registrado e principalmente, claro, veja que o seu GIF já está no README.md!

<figure><img src="../../.gitbook/assets/72_ Repo após push 4 (1).png" alt=""><figcaption></figcaption></figure>

***

No próximo capítulo, veremos o processo recomendado para mesclar essas alterações à branch principal do repositório central.

