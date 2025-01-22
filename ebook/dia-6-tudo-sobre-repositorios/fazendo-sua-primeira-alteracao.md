# Primeira Alteração no GitHub

Agora, vamos fazer a primeira edição no seu novo repositório.

Como, por enquanto, o único arquivo no repositório é o próprio `README.md`, vamos começar por ele. Nossa primeira modificação será adicionar a frase: `Praticando Git + GitHub`, para deixar claro o propósito deste repositório.

## Edição do Arquivo

Para começar a editar o arquivo README.md, clique no ícone de lápis no canto superior direito da exibição automática do conteúdo.

<figure><img src="../.gitbook/assets/Editar README.png" alt="Interface do GitHub mostrando o repositório &#x27;hello-world&#x27;. Há uma parte destacada em roxo indicando o ícone de lápis para edição do arquivo README.md"><figcaption><p>Botão de edição do README</p></figcaption></figure>



Isso lhe levará para uma página de edição do arquivo.

<figure><img src="../.gitbook/assets/Editar README página.png" alt="Interface do GitHub mostrando o editor do arquivo README.md do repositório &#x27;hello-world&#x27;. O usuário está editando a descrição inicial do projeto, que é o primeiro repositório criado na plataforma"><figcaption><p>Tela de edição do arquivo README</p></figcaption></figure>

Agora, basta adicionar a frase desejada diretamente no arquivo:

<figure><img src="../.gitbook/assets/Editar README página depois.png" alt="Interface do GitHub mostrando o editor do arquivo README.md do repositório &#x27;hello-world&#x27;. O usuário está editando a descrição inicial do projeto, agora tem-se adicionada a frase &#x60;Praticando Git + GitHub&#x60;, após o texto &#x60;Meu primeiro repositório no GitHub.&#x60;"><figcaption><p>Tela de edição do arquivo README com a nova alteração</p></figcaption></figure>

Agora, basta adicionar a frase desejada diretamente no arquivo. Este processo é similar ao que fazemos ao editar um arquivo no nosso computador com um editor de texto. A diferença é que a edição está acontecendo no GitHub, não localmente no seu computador.

## Adição do Arquivo

Em seguida, clique no botão "Commit Changes".

Depois de fazer a modificação, clique no botão **"Commit Changes"**.

Por trás dos panos, ao clicar nesse botão, o GitHub executa o comando equivalente a `git add README.md`, que coloca o arquivo na área de staging, preparando-o para o commit.

## Commit e Push da Alteração

Na tela seguinte:

* Preencha o campo "Commit message" com: `Atualizando o README.md`.
* Preencha o campo "Extended Description" com: `Adicionando o objetivo do repositório.`
* Selecione a opção `Commit directly to the main branch`.

<figure><img src="../.gitbook/assets/Commit Dialog.png" alt="Janela de commit do GitHub: A imagem mostra uma janela modal típica do GitHub usada para confirmar alterações antes de enviá-las para o repositório. Mensagem de commit: Há um campo para inserir a mensagem de commit, que descreve brevemente as alterações realizadas. Descrição estendida: Um campo adicional permite adicionar uma descrição mais detalhada das mudanças. Opções de commit: O usuário pode escolher entre commitar diretamente na branch principal (main) ou criar uma nova branch e iniciar um pull request."><figcaption><p>Janela de confirmação de commit</p></figcaption></figure>

Por fim, clique novamente em **"Commit Changes"**. Isso irá criar um commit de fato, como se você tivesse rodado o comando `git commit -m "Adicionando o objetivo do repositório"`. Além disso, o GitHub também fará automaticamente o **push** da alteração para a branch principal, já que selecionamos a opção "_Commit directly to the main branch_".

Agora, a sua modificação foi registrada na branch principal do repositório.

## Verificando a Alteração

Logo você já perceberá que o arquivo foi atualizado.

<figure><img src="../.gitbook/assets/README depois alt.png" alt="Tela de detalhes do arquivo README. Mostra conteúdo do arquivo README.md do repositório &#x27;hello-world&#x27;. O usuário está visualizando a descrição inicial do projeto, que é o primeiro repositório criado na plataforma. O texto indica que o usuário está praticando as ferramentas Git e GitHub."><figcaption><p>Página do arquivo README</p></figcaption></figure>

E ao voltar à página principal do repositório, também verá que a sua alteração já foi aplicada e está visível lá.

<figure><img src="../.gitbook/assets/Repo depois alt.png" alt="Página principal do repositório hello-world mostrando o README atualizado."><figcaption><p>Página principal do repositório - aba code.</p></figcaption></figure>

## Atenção ⚠️

### Boas Práticas de Fluxo de Trabalho

Embora esse processo seja uma forma prática de fazer alterações diretamente pelo GitHub, **não é recomendado para o dia a dia**, especialmente em projetos maiores ou quando for necessário alterar vários arquivos. O ideal é **evitar fazer commits diretamente na branch principal (main)**. Este fluxo foi usado aqui apenas para fins didáticos.

Em situações reais, as alterações devem ser feitas utilizando **branches** e **pull requests**, um processo que veremos mais adiante. Isso ajuda a manter o fluxo de trabalho mais organizado e seguro, especialmente quando se trabalha em equipe.
