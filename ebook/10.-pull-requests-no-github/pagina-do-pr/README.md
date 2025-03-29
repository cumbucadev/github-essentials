# Página do PR

Agora que você criou seu primeiro PR, vamos explorar os principais componentes da página de exibição e entender como interagir com eles. Abaixo, abordamos as seções mais importantes da interface para que você possa navegar de maneira mais eficiente.

<figure><img src="../../.gitbook/assets/86 PR recém criado.png" alt=""><figcaption><p>PR <a href="https://github.com/aprendizCumbucaDev/hello-world/pull/2">https://github.com/aprendizCumbucaDev/hello-world/pull/2</a></p></figcaption></figure>

## Cabeçalho

A seção de **Cabeçalho** contém as informações essenciais sobre o PR, fornecendo uma visão geral rápida e permitindo interações básicas com o PR.

<figure><img src="../../.gitbook/assets/88 Pg PR- cabeçalho.png" alt=""><figcaption><p>Cabeçalho do PR PR <a href="https://github.com/aprendizCumbucaDev/hello-world/pull/2">https://github.com/aprendizCumbucaDev/hello-world/pull/2</a></p></figcaption></figure>

* **Título do PR**: Indica a mudança que será feita no repositório. Neste caso: `Adicionando GIF de boas-vindas ao README.md`.
* **Número do PR**: Aparece ao lado do título, indicando o número único da issue dentro do repositório. Neste caso: `#2`.
* **Estado do PR**: Exibe se o PR está:
  * Ope&#x6E;**:** PR aberto e aguardando revisão ou mesclagem.
  * Merge&#x64;**:** PR já mesclado ao branch de destino.
  * Close&#x64;**:** PR fechado sem mesclagem.
  * Neste caso: `Open`.
*   **Resumo da Solicitação:** Descreve rapidamente a intenção do PR no seguinte formato:

    > `<pessoa-autora> wants to merge <número-de-commits> commit into <branch-destino> from <branch-origem>`

    * Neste caso: `aprendizCumbucaDev wants to merge 1 commit into main from issue-1`.
    * **Pessoa Autora do PR**: O nome da conta de usuário de que abriu o PR. Neste caso: `aprendizCumbucaDev`.
    * **Número de commits**: Exibe o total de commits incluídos no PR. Neste caso: `1 commit`.&#x20;
    * **Branches envolvidos**:
      * Base (branch destino): branch onde as mudanças serão aplicadas. Neste caso: `main`.
      * Origem: branch que contém as alterações propostas. Neste caso: `issue-1`.
* **Botão Edit**: Permite editar o título do PR, caso seja necessário atualizar ou corrigir informações. Bem como o branch destino (base).
* **Botão de Cópia**: Permite copiar o nome da branch de origem para compartilhá-lo facilmente.
* **Botão Code**: Não é relevante para nosso contexto no momento.&#x20;

{% hint style="success" %}
**Curiosidade!**

Talvez você tenha se perguntado por que o número do PR é `#2` ao invés de `#1`, uma vez que ele foi o primeiro PR do repositório. Isso acontece porque o GitHub gera automaticamente um número sequencial para cada novo issue ou PR criado no repositório. Como as issues e os PRs compartilham a mesma numeração, o primeiro PR criado pode não necessariamente ser o `#1`. No caso em questão, como já existia uma issue aberta anteriormente (#1), o primeiro PR recebeu o número `#2`.

Isso ocorre porque, internamente, issues e pull requests fazem parte do mesmo sistema de rastreamento no GitHub, sendo numerados na ordem em que são abertos. Assim, se a issue `#1` já existia, o próximo item aberto—mesmo sendo um PR—receberá o número `#2`.
{% endhint %}

***

Em seguida, vamos explorar cada uma das quatro abas presentes na página de um PR: **Conversation, Commits, Checks** e **Files changed.**

<figure><img src="../../.gitbook/assets/89 Pg PR- abas.png" alt=""><figcaption></figcaption></figure>
