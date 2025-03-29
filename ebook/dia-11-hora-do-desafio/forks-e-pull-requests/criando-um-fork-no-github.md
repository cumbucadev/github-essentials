# Criando um Fork no GitHub

A primeira etapa para começar a contribuir com um projeto open source é criar um fork do repositório desejado. Vamos fazer isso com o repositório `cumbucadev/PRimeiro-fork`, que foi criado especificamente para fins didáticos. Aqui, você pode experimentar sem medo!

## Passo 1: Acessar o Repositório

Para começar, acesse a página do repositório `cumbucadev/PRimeiro-fork` no GitHub: [https://github.com/cumbucadev/PRimeiro-fork](https://github.com/cumbucadev/PRimeiro-fork).

<figure><img src="../../.gitbook/assets/162 fork.png" alt=""><figcaption></figcaption></figure>

### Passo 2: Criar o Fork

Na página do repositório, clique no botão **Fork**, localizado no canto superior direito.

<figure><img src="../../.gitbook/assets/163 fork 2.png" alt=""><figcaption></figcaption></figure>

## Passo 3: Confirmar a Criação do Fork

Após clicar em **Fork**, uma nova página será aberta para a criação do seu fork. Todas as informações já estarão preenchidas automaticamente, então basta clicar no botão **Create fork**.

<figure><img src="../../.gitbook/assets/164 fork 3.png" alt=""><figcaption></figcaption></figure>

## Passo 4: Seu Fork Está Pronto!

Agora, será feito o redirecionamento para a página do novo repositório forkado. Algumas diferenças em relação a um repositório comum podem ser notadas:

* Há um link abaixo do nome do repositório que indica a origem do fork\
  `forked from` [`cumbucadev/PRimeiro-fork`](https://github.com/cumbucadev/PRimeiro-fork)
* Acima da lista de arquivos, existe um novo elemento que chamaremos de **Barra de Sincronização com o Upstream**.

<figure><img src="../../.gitbook/assets/165 fork 4.png" alt=""><figcaption></figcaption></figure>

## Barra de Sincronização com o Upstream

Essa barra tem um papel fundamental na manutenção do fork atualizado em relação ao repositório original. No momento, vamos apenas observar o estado atual dela, mas falaremos mais sobre suas funcionalidades posteriormente.

<figure><img src="../../.gitbook/assets/166 fork 5.png" alt=""><figcaption></figcaption></figure>

Na barra, encontramos a mensagem:

> **This branch is up to date with cumbucadev/PRimeiro-fork:main.**\
> Este branch está atualizado com cumbucadev/PRimeiro-fork:main.

Isso significa que o fork está atualizado e não há mudanças novas no repositório original que precisem ser incorporadas.

### O Botão Contribute

O botão **Contribute** ("Contribuir") é útil para sugerir alterações ao repositório original. Ou seja, para quando você pretende contribuir com o repositório original.

Atualmente, vemos a seguinte mensagem:

> **This branch is not ahead of the upstream cumbucadev/PRimeiro-fork:main. No new commits yet. Enjoy your day!**
>
> Este branch não está à frente do upstream cumbucadev/PRimeiro-fork:main. Nenhum novo commit ainda. Aproveite o seu dia!"

Essa mensagem indica que o fork ainda não tem commits próprios que o diferenciem do repositório original. Ou seja, nenhuma modificação foi feita no fork até o momento.

<figure><img src="../../.gitbook/assets/167 fork 6.png" alt="" width="375"><figcaption></figcaption></figure>

### O Botão Sync Fork

O botão **Sync Fork** ("Sincronizar Fork") permite atualizar o fork com as mudanças mais recentes feitas no repositório original (upstream). Se houver novas alterações no upstream, o fork pode ficar "desatualizado", e esse botão permite sincronizá-lo novamente.

> **This branch is not behind the upstream cumbucadev/PRimeiro-fork:main. No new commits to fetch. Enjoy your day!**
>
> Este branch não está atrás do upstream cumbucadev/PRimeiro-fork:main. Nenhum novo commit para buscar. Aproveite o seu dia!

Isso significa que o fork já contém todas as atualizações do upstream e não há nada novo para buscar. Se, no futuro, o upstream receber commits novos, essa mensagem mudará, e o botão **Sync Fork** permitirá atualizar seu repositório.

<figure><img src="../../.gitbook/assets/168 fork 7.png" alt="" width="375"><figcaption></figcaption></figure>

Analisando as informações da **Barra de Sincronização com o Upstream**, concluímos que tanto o fork quanto o repositório original estão exatamente no mesmo estado. Não há commits no upstream que ainda não tenham sido incorporados ao fork, nem commits no fork que ainda não tenham sido enviados ao upstream.

***

{% hint style="info" %}
Para mais detalhes, consulte [Documentação Oficial](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) do GitHub.
{% endhint %}

Agora que temos um fork, o próximo passo será cloná-lo localmente para que possamos começar a trabalhar nele. Vamos ver como fazer isso na próxima seção!
