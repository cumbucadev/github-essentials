# Clonando um Repositório do GitHub

Quando você cria um repositório no GitHub, ele existe apenas como um **repositório remoto** na plataforma. Para trabalhar no código de forma eficiente, é essencial ter uma **cópia local** no seu computador, permitindo que você faça edições, testes e commits antes de enviá-las de volta para o GitHub.

Isso significa que, neste momento, o seu projeto **hello-world** só existe no GitHub — ele ainda não está no seu computador.

Agora, vamos ao primeiro passo do nosso novo fluxo de trabalho: **clonar o repositório** para o seu computador.

## Passo a Passo

### Copiar URL do Repositório

Acesse a página principal do projeto no GitHub e clique no botão **Code**.

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt="" width="147"><figcaption><p>Botão code.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/50 Clone repo 1 (1).png" alt=""><figcaption><p>Página principal do repositório após o clique no botão code.</p></figcaption></figure>

Na janela de diálogo que irá se abrir, clique em **SSH.**

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/51 Clone repo 2 (1).png" alt=""><figcaption></figcaption></figure>

Em seguida, clique no botão de copiar que aparecerá ao lado da URL do repositório.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1).png" alt="" width="108"><figcaption><p>Botão "copiar".</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/68 Clone repo 3.png" alt=""><figcaption><p>Copiar link do repositório remoto</p></figcaption></figure>

Agora, a URL para o seu repositório remoto **hello-world** está copiada. Iremos utilizá-la no terminal para clonar o projeto localmente a seguir.

### Clonar o Repositório Localmente

Agora execute no terminal o seguinte comando - substituindo `<URL-COPIADA>` pelo valor correspondente.

```bash
git clone <URL-COPIADA>
```

Exemplo:

```bash
git clone git@github.com:aprendizCumbucaDev/hello-world.git
▶ Cloning into 'hello-world'...
remote: Enumerating objects: 6, done.
remote: Counting objects: 100% (6/6), done.
remote: Compressing objects: 100% (4/4), done.
Receiving objects: 100% (6/6), done.
remote: Total 6 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
```

Para verificar se o projeto foi clonado com sucesso, use o comando `dir` (no Windows) ou `ls` (no Linux/macOS) para listar os arquivos do diretório atual. Você deverá ver a pasta **hello-world** na lista.

O próximo passo será começar a fazer edições no repositório local.
