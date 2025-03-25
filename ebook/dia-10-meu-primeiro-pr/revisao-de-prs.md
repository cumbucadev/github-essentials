# Revisão de PR

Criar um Pull Request (PR) é apenas o primeiro passo para integrar suas mudanças ao projeto. A revisão de PRs é uma parte essencial desse processo, garantindo qualidade, alinhamento com as práticas do time e melhoria contínua do código.

{% hint style="warning" %}
É importante ressaltar que, por se tratar de um curso introdutório, vamos explorar a revisão de Pull Requests apenas da perspectiva de quem a solicitou, sem abordar o processo do ponto de vista de quem revisa.
{% endhint %}

## Resultado de uma Revisão

Cada pessoa revisora fará uma avaliação do seu código, podendo ter resultados diferentes de acordo com os níveis de feedback:

* 💬 **Apenas Comentários:** A revisão traz observações gerais sobre o as alterações sem aprovar ou rejeitar as mudanças. Pode incluir sugestões de melhorias, dúvidas ou pontos para discussão.
* ✅ **Aprovação:** As mudanças propostas foram consideradas adequadas para serem mescladas ao repositório. Pode incluir pequenos comentários ou sugestões opcionais.
* ❌ **Solicitação de Alterações:** Foram encontrados problemas que precisam ser corrigidos antes que o PR possa ser aceito. Geralmente inclui feedback detalhado sobre o que deve ser ajustado nos comentários.

{% hint style="info" %}
Para mais detalhes: [Documentação Oficial do GitHub](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/about-pull-request-reviews).
{% endhint %}

É importante entender o feedback de cada pessoa revisora para avançar no processo de revisão. É possível que diferentes revisores tenham opiniões distintas, então é fundamental avaliar cada comentário e decidir como proceder.

## Fluxo de Revisão

Agora, vamos explorar como um fluxo de revisão de PR acontece, quais são suas etapas e como você pode interagir em cada uma delas.

### 1. **Solicitar Revisão de PR**

A revisão começa quando há uma solicitação de revisão. Isso pode ocorrer simplesmente ao abrir um PR sem marcar ninguém como pessoa revisora ou ao selecionar pessoas específicas. A abordagem dependerá das regras e boas práticas do projeto.

{% hint style="info" %}
Para mais detalhes: [Documentação Oficial do GitHub](https://docs.github.com/pt/enterprise-cloud@latest/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/requesting-a-pull-request-review).
{% endhint %}

### 2. **Aguardar Feedback**

Fique de olho nas notificações do GitHub e na [aba-conversation.md](pagina-do-pr/aba-conversation.md "mention") do PR para acompanhar as revisões. Caso não obtenha resposta, é possível gentilmente lembrar as pessoas revisoras mencionando-as nos comentários.

### 3. Avaliar Alterações Sugeridas

Se a revisão incluir sugestões de alterações, siga os passos abaixo:

#### 3.1 Entender as Sugestões

Se algo não estiver claro, pergunte nos comentários. Isso faz parte do processo! Muitas vezes, pode ser difícil questionar quando não se sente seguro, mas pedir esclarecimentos ajuda a todos e melhora a colaboração no projeto.

#### 3.2 Analisar se Concorda com as Sugestões

Nem sempre é necessário concordar com tudo. Às vezes, até mesmo as pessoas revisoras discordam entre si. O importante é expor o ponto de vista de maneira clara, detalhada e respeitosa. O PR é uma ferramenta poderosa justamente por proporcionar essa troca.

#### 3.3. Aplicar Alterações Sugeridas

Existem duas formas principais de aplicar sugestões:

**Editar localmente e enviar as modificações**

* No seu editor local, faça as modificações sugeridas.
*   Faça um ou mais novos commits e envia as novas mudanças para o repositório remoto através do comando <mark style="color:purple;">git</mark> <mark style="color:orange;">push</mark>.\
    Exemplo:

    ```sh
    git add arquivo.txt
    git commit -m "Corrigindo erro de digitação"
    git push origin issue-1
    ```
* Isso enviará as mudanças para o PR automaticamente.

**Usar a funcionalidade de "Commit suggestion"**

O GitHub oferece uma funcionalidade que permite que pessoas revisoras adicionem sugestões de alteração diretamente na linha do arquivo dentro de um Pull Request (PR). Essas sugestões aparecem na interface do PR e podem ser aceitas e aplicadas com apenas alguns cliques, facilitando a colaboração em equipe e tornando a revisão de código mais interativa. Além disso, essa funcionalidade evita a necessidade de edição manual dos arquivos, tornando o processo mais rápido e ajudando a manter um histórico de commits mais organizado.

<figure><img src="../.gitbook/assets/commit suggestions.png" alt=""><figcaption><p>Imagem retirada da <a href="https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/incorporating-feedback-in-your-pull-request#applying-suggested-changes">documentação oficial</a>.</p></figcaption></figure>

Quando usar?

* Quando um revisor deixou uma sugestão diretamente no código da sua Pull Request.
* Se deseja aplicar sugestões rapidamente, sem precisar editar os arquivos manualmente.

Como Aplicar uma Sugestão?

1. Acesse a [aba-files-changed.md](pagina-do-pr/aba-files-changed.md "mention") do PR.
2. Role a página até encontrar os comentários com sugestões de código -geralmente marcados com um fundo cinza e o botão **"Commit suggestion" (Fazer commit da sugestão)** ao lado.
3. Escolha como aplicar as sugestões

* Existem duas maneiras de aplicar as sugestões feitas por pessoas revisoras:
  * **Aplicação individual:** Se quiser aceitar uma sugestão por vez, criando um commit separado para cada uma. Isso pode ser útil quando as sugestões são independentes ou precisam ser revisadas separadamente.
  * **Aplicação em lote:** Permite agrupar várias sugestões e aplicá-las todas de uma vez em um único commit. Isso ajuda a manter o histórico de commits mais organizado, especialmente quando as sugestões estão relacionadas.

4. Faça um commit com a(s) sugestão(ões). &#x20;

Opção 1: Aplicando uma sugestão individualmente

* Ao lado da sugestão, clique no botão **"Commit suggestion" (Fazer commit da sugestão)**.
* No campo de mensagem do commit, escreva uma breve descrição da alteração.
* Clique em **"Commit changes" (Fazer commit das alterações)**.

<figure><img src="../.gitbook/assets/image (110).png" alt=""><figcaption><p>Imagem retirada da <a href="https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/incorporating-feedback-in-your-pull-request#applying-suggested-changes">documentação oficial</a>.</p></figcaption></figure>

Opção 2: Aplicando várias sugestões ao mesmo tempo

* Para cada sugestão que deseja incluir, clique em **"Add suggestion to batch" (Adicionar sugestão ao lote)**.
* Continue adicionando sugestões até finalizar.
* Quando estiver pronto, clique em **"Commit suggestions" (Fazer commit das sugestões)**.
* No campo de mensagem do commit, escreva um resumo das alterações aplicadas.
* Clique em **"Commit changes" (Fazer commit das alterações)**.

<figure><img src="../.gitbook/assets/image (111).png" alt=""><figcaption><p>Imagem retirada da <a href="https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/incorporating-feedback-in-your-pull-request#applying-suggested-changes">documentação oficial</a>.</p></figcaption></figure>

{% hint style="info" %}
Para mais detalhes: [Documentação Oficial do GitHub](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/incorporating-feedback-in-your-pull-request#applying-suggested-changes).
{% endhint %}

### 4. Responder Comentários

Para responder a um comentário, acesse o comentário na [aba-conversation.md](pagina-do-pr/aba-conversation.md "mention") ou na [aba-files-changed.md](pagina-do-pr/aba-files-changed.md "mention") e adicionar outro comentário abaixo dele. Responda aos comentários para manter a comunicação fluindo.&#x20;

Caso não saiba algo, fique à vontade para perguntar. O espaço de revisão deve ser um ambiente aberto para aprendizado, beneficiando tanto quem contribui quanto o projeto.

{% hint style="info" %}
Para mais detalhes: [Documentação Oficial do GitHub](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/commenting-on-a-pull-request).
{% endhint %}

### 5. Resolver Conversas

Após aplicar as sugestões ou responder adequadamente, marque as conversas como resolvidas para manter o PR organizado. No GitHub, ao lado do comentário, clique em "**Resolve conversation**". Apenas faça isso se a sugestão foi incorporada ou houve consenso de que não é necessária.

<figure><img src="../.gitbook/assets/118- PR resolve conversation (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Para mais detalhes: [Documentação Oficial do GitHub](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/commenting-on-a-pull-request#resolver-conversas).
{% endhint %}

### 6. Re-solicitar Revisão

Depois que você fizer as alterações necessárias, você poderá solicitar que o PR seja revisada novamente pela mesma pessoa revisora. Na [aba-conversation.md](pagina-do-pr/aba-conversation.md "mention"), procure **Reviewers** na barra lateral direita e clique no ícone 🔄 ao lado do nome da pessoa revisora.

<figure><img src="../.gitbook/assets/image (113).png" alt=""><figcaption><p>Imagem retirada da <a href="https://docs.github.com/pt/enterprise-cloud@latest/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/requesting-a-pull-request-review#requesting-reviews-from-collaborators-and-organization-members">documentação oficial</a>.</p></figcaption></figure>

Opcionalmente, **c**omente no PR mencionando `@nome_da_pessoa_revisora` e forneça um breve resumo das mudanças feitas desde a última revisão. Aguarde até o próximo feedback (passo 2) e, siga em diante com o fluxo.

O fluxo segue até que o PR seja aprovado ou até que haja uma decisão de que ele não faz sentido e deve ser fechado.

<figure><img src="../.gitbook/assets/Fluxo de Revisão de PR (1).png" alt=""><figcaption></figcaption></figure>

Cada projeto pode ter regras diferentes sobre a quantidade de aprovações necessárias para que o merge seja liberado. Algumas vezes, uma única aprovação é suficiente; em outros casos, pode ser necessário que todas as pessoas revisoras aprovem.

***

A seguir, vamos explorar quais são as boas práticas sugeridas ao receber revisões em seus PRs.
