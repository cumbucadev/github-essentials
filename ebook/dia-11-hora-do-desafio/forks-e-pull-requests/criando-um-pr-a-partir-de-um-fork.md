# Criando um PR a partir de um Fork

Quando você contribui para um repositório no GitHub sem permissões de escrita, o processo envolve a criação de um **fork** – uma cópia do repositório no seu próprio perfil, como vimos anteriormente. A partir desse fork, você pode criar um branch, fazer suas alterações e, depois, propor que essas mudanças sejam incorporadas ao repositório original por meio de um **Pull Request (PR)**.

Neste guia, vamos explorar o passo a passo para criar um PR a partir de um fork, garantindo que suas contribuições sejam enviadas corretamente para revisão e possível aprovação. O processo é muito parecido com o que vimos anteriormente em [criando-um-pr-no-github.md](../../dia-10-meu-primeiro-pr/criando-um-pr-no-github.md "mention").

## Acessar a Página de Criação de Pull Request <a href="#criando-sua-primeira-issue" id="criando-sua-primeira-issue"></a>

Se o painel que indica que o branch **aprendizCumbucaDev** recebeu alterações recentemente (por exemplo, com a mensagem _"aprendizCumbucaDev had recent pushes X minutes ago"_) ainda estiver visível, você pode iniciar um pull request rapidamente clicando no botão **Compare & pull request** (Comparar e pull request).

Se esse painel não estiver visível, outra opção é acessar diretamente a página do branch **aprendizCumbucaDev**. Para isso, clique no botão **Contribute** e, em seguida, selecione **Open pull request** (Abrir pull request).

Ambas as opções levam à mesma tela, onde você poderá revisar as alterações antes de criar o pull request.

<figure><img src="../../.gitbook/assets/184 PR fork - upstream.png" alt=""><figcaption></figcaption></figure>

## Criar de Pull Request <a href="#criando-sua-primeira-issue" id="criando-sua-primeira-issue"></a>

Após clicar em um dos botões, a navegação será redirecionada para a página de criação do pull request. Nessa etapa, é importante revisar as mudanças, preencher os campos necessários e garantir que tudo esteja correto antes de enviar.

<figure><img src="../../.gitbook/assets/ebook images (1500 x 2000 px) (3).png" alt=""><figcaption></figcaption></figure>

### 1. Certifique-se de que os repositórios e branches de origem e destino estão corretos

* O repositório e branch de **origem** devem ser:&#x20;
  * `aprendizCumbucaDev/PRimeiro-fork aprendizCumbucaDev`&#x20;
* O repositório e branch de **destino** devem ser:&#x20;
  * `cumbucadev/PRimeiro-fork main`:&#x20;
* Assim, a configuração correta será:
  * > **cumbucadev/PRimeiro-fork main ← aprendizCumbucaDev/PRimeiro-fork aprendizCumbucaDev**&#x20;

<figure><img src="../../.gitbook/assets/185 PR fork - upstream 2.png" alt=""><figcaption></figcaption></figure>

Isso garante que as alterações feitas no branch **aprendizCumbucaDev** do fork `aprendizCumbucaDev/PRimeiro-fork` serão enviadas para o branch **main** do repositório original `cumbucadev/PRimeiro-fork`.

### 2. Confira o Título

Como o pull request tem apenas um commit, o GitHub já preencheu o título com a mensagem deste commit. Certifique-se de que ele esteja claro e descritivo.

<figure><img src="../../.gitbook/assets/186 PR fork - upstream 3.png" alt=""><figcaption></figcaption></figure>

Neste caso, podemos prosseguir mantendo o título como `Adiciona nova frase ao arquivo GARFO.md`.

### 3. Preencha a Descrição

Na caixa de descrição, forneça um resumo das alterações e a motivação para elas.

<figure><img src="../../.gitbook/assets/187 PR fork - upstream 4.png" alt=""><figcaption></figcaption></figure>

Neste casp, preencha-a com:

```markdown
# Adiciona nova frase ao arquivo GARFO.md

* **Descrição**: Adiciona a frase `Nem vem de garfo que hoje é dia de sopa.` ao arquivo **GARFO.md**.
* **Motivação**: Praticar fluxo de trabalho de **forks e pull requests**.
```

<figure><img src="../../.gitbook/assets/188 PR fork - upstream 5.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Não será necessário adicionar o número da issue, pois este repositório é utilizado apenas para fins didáticos e não requer criação de issues.
{% endhint %}

Também faça uma pré-visualização da descrição formatada para garantir que tudo está sendo exibido corretamente.

<figure><img src="../../.gitbook/assets/189 PR fork - upstream 6.png" alt=""><figcaption></figcaption></figure>

### 4. Revise as modificações

Antes de criar o PR, revise as mudanças para garantir que tudo está correto.

<figure><img src="../../.gitbook/assets/190 PR fork - upstream 7.png" alt=""><figcaption></figcaption></figure>

### 5. Crie o pull request

Após preencher todas as informações e revisar as mudanças, clique em **Create pull request** para enviar.

<figure><img src="../../.gitbook/assets/image.png" alt="" width="375"><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/8 PR fork - upstream 3.png" alt=""><figcaption></figcaption></figure>

Parabéns, o seu primeiro pull request a partir de um fork foi criado com sucesso!

***

{% hint style="info" %}
Para mais detalhes sobre criação de pull request a partir de um fork, consulte a [Documentação Oficial](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork) do GitHub.
{% endhint %}

A seguir, vamos aprender sobre a sincronização de forks. Em seguida, abordaremos a revisão, mesclagem e as etapas pós-mesclagem do seu PR.
