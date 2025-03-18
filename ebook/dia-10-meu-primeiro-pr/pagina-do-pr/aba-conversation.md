# Aba Conversation

A aba Conversation de um Pull Request (PR) no GitHub é onde você, como pessoa autora do PR, pode acompanhar a discussão sobre suas alterações, responder a feedbacks e monitorar o progresso do merge. A seguir, detalhamos as principais seções e ações disponíveis para quem abriu o PR.

<figure><img src="../../.gitbook/assets/86 PR recém criado.png" alt=""><figcaption></figcaption></figure>

## Descrição

A seção **Descrição** contém informações detalhadas sobre o PR e serve como ponto de partida para a revisão e a discussão das mudanças propostas.

<figure><img src="../../.gitbook/assets/90 PR criado- description.png" alt=""><figcaption></figcaption></figure>

* **Última Atividade no PR:** Mostra a última ação realizada no PR, quem a realizou e quando aconteceu. A atividade pode incluir ações como:
  * Atualização na descrição
  * Mudança de status
  * Adição ou remoção de labels
  * Pedido de revisão ou aprovação.

Neste caso: aprendizCumbucaDev commented Now (aprendizCumbucaDev comentou Agora)

* **Botão `...`(Mais Opções)**: Disponibiliza ações adicionais. Entre as principais: Copy Link (Copiar Link) e Edit (Editar).&#x20;
  * ![](<../../.gitbook/assets/image (108).png>)
  * **Copy Link:** **Copy Link (Copiar Link):** Permite copiar o link do PR para compartilhamento.
  * **Edit:** Permite editar a descrição do PR.
* **Texto do PR**: O corpo do PR onde as alterações são descritas detalhadamente. Pode incluir texto formatado com Markdown, links, imagens e outras anotações para explicar o objetivo e o impacto das mudanças propostas.
* **Botão de reagir ao PR:** Pessoas usuárias podem adicionar reações em forma de emojis (👍, 👎, 😄, etc.) como forma de engajamento.

## **Histórico de Ações** <a href="#historico-de-acoes" id="historico-de-acoes"></a>

A seção **Histórico de Ações** funciona como uma linha do tempo do PR, registrando todas as interações e mudanças desde a sua abertura. Como pessoa autora do PR, essa seção permite acompanhar tudo o que aconteceu ao longo do processo de revisão.

#### Principais eventos no histórico:

* **Commits adicionados ao PR:** Cada vez que novas alterações são feitas no código e enviadas para o PR, elas aparecem aqui. Isso ajuda revisores a entenderem a evolução do trabalho.
* **Comentários de Revisores:** Feedbacks e sugestões deixados por revisores aparecem no histórico. Se um comentário estiver vinculado a uma linha específica do código, ele será destacado.
* **Seus Comentários:**
* **Resoluções de Comentários:** Quando um comentário é marcado como "resolvido", isso também é registrado no histórico, ajudando a acompanhar o progresso da revisão.
* **Alterações de Labels:** Se um rótulo (label) for adicionado ou removido do PR, essa ação será listada.
* **Mudanças de Status do PR:** Qualquer alteração no estado do PR aparece no histórico.
* **Pedidos de Revisão:** Quando você solicita que alguém revise seu PR, essa ação é registrada. Isso ajuda a manter o fluxo de trabalho organizado.
* **Aprovações e Rejeições:** Quando um revisor aprova o PR ou solicita mudanças, essa informação aparece no histórico. Caso mudanças sejam solicitadas, a pessoa autora pode ver exatamente quais pontos precisam ser ajustados.
* **Conclusão de Checks Automáticos:** Se o repositório tiver verificações automáticas configuradas, o resultado delas também será exibido no histórico. Essas verificações podem conferir diferentes aspectos do código e do projeto, garantindo que tudo esteja conforme o esperado. Sempre que novas mudanças são enviadas ao PR, os checks são executados automaticamente e indicam se houve sucesso ✅ ou se algo precisa ser corrigido ❌ antes da aprovação.

Como o seu PR foi recém criado, não haverá ainda muitas ações, mas no futuro o histórico de ações se parecerá algo como:

<figure><img src="../../.gitbook/assets/90 PR criado- histórico de atividades.png" alt=""><figcaption></figcaption></figure>

Acompanhar o **Histórico de Ações** é essencial para entender o andamento do seu PR, estando ciente de tudo que está ocorrendo nele, e tomar as ações necessárias, como responder comentários, fazer modificações e solicitar novas revisões.

## Seção de Verificação de Status

A seção de verificação de status em um Pull Request (PR) mostra se há algum requisito pendente antes que o PR possa ser aceito e integrado ao projeto. Essas verificações podem incluir testes automáticos, análise de código, aprovações de revisores ou outras regras definidas no repositório.

<figure><img src="../../.gitbook/assets/image (103).png" alt=""><figcaption></figcaption></figure>

**O que você pode ver nessa seção?**

* ✅ **Tudo certo**: Se todas as verificações foram concluídas com sucesso, o PR está pronto para ser mesclado (_merge_).
* ❌ **Problemas detectados**: Caso alguma verificação falhe, o PR pode precisar de ajustes antes de ser aprovado. Clicar no erro geralmente exibe mais detalhes sobre o problema.
* ⏳ **Aguardando verificações**: Algumas verificações podem levar tempo para serem concluídas. Enquanto isso, o status mostrará que o processo ainda está em andamento.

Essa seção ajuda a garantir que o código enviado atende aos critérios necessários antes de ser integrado ao projeto principal.

Leia mais sobre **Verificação de Status** na [Documentação Oficial do GitHub](aba-conversation.md#historico-de-acoes).

### **Botão de Merge em um Pull Request**

O botão de **Merge** é usado para finalizar um Pull Request (PR) e integrar as mudanças no projeto principal. Ele só fica disponível quando todas as verificações necessárias foram concluídas com sucesso e as permissões do repositório permitem o merge do código.

<figure><img src="../../.gitbook/assets/image (102).png" alt="" width="375"><figcaption></figcaption></figure>

Se o botão não estiver disponível, pode ser por um dos seguintes motivos:

* O PR ainda tem verificações pendentes ou falhas.
* Faltam aprovações de revisores.
* O repositório exige que o PR esteja atualizado com a versão mais recente do código antes do merge.

Falaremos sobre o merge do PR em seções futuras. Por enquanto, recomendamos que você não clique no botão de **Merge** ainda.

## Seção de Criação e Edição de Comentários

A seção de criação e edição de comentário em um Pull Request permite que você participe das discussões relacionadas às mudanças propostas. Nele, é possível contribuir com sugestões, esclarecer dúvidas, fornecer feedback ou interagir com outras pessoas colaboradoras durante o processo de revisão. O editor suporta Markdown para formatação, permite anexar arquivos e mencionar usuários com `@username`, facilitando a comunicação e a colaboração.

<figure><img src="../../.gitbook/assets/93 PR criado- criar comentário.png" alt=""><figcaption></figcaption></figure>

* **Editor de Comentários**: Campo para adicionar novos comentários, onde os usuários podem digitar suas mensagens e usar o Markdown para formatação. Também inclui botões para anexar arquivos ou mencionar outros usuários com `@username`.

Escreve seu comentário e clique em **Comment** para publicá-lo. Após a publicação, o comentário fica registrado no histórico de atividades.

<figure><img src="../../.gitbook/assets/94 PR criado- comentário.png" alt=""><figcaption></figcaption></figure>

Clique no botão **Mais Ações** (`...`) para:

* **Copiar link de compartilhamento** (_Copy Link_).
* **Editar o comentário** (_Edit_).
* **Excluir o comentário** (_Delete_).

<figure><img src="../../.gitbook/assets/image (105).png" alt="" width="375"><figcaption></figcaption></figure>

Utilize o **Botão de Reações** para reagir aos comentários que aparecem no histórico de atividades com emojis.

<figure><img src="../../.gitbook/assets/image (106).png" alt="" width="354"><figcaption></figcaption></figure>

## Botão de Fechamento <a href="#botao-de-fechamento" id="botao-de-fechamento"></a>

O botão de **Fechar Pull Request** (_Close Pull Request_) permite encerrar um PR sem mesclar as alterações ao projeto principal. Ele deve ser usado quando as mudanças propostas não são mais necessárias ou quando a abordagem escolhida precisa ser descartada.

<figure><img src="../../.gitbook/assets/image (104).png" alt="" width="375"><figcaption></figcaption></figure>

**O que acontece ao fechar um PR?**

* O PR é arquivado e marcado como **fechado**, sem ser integrado ao código principal.
* Os comentários e o histórico de alterações continuam acessíveis, mas nenhuma nova alteração pode ser enviada para esse PR.
* Caso o fechamento tenha sido um erro, o PR pode ser reaberto, desde que as permissões do repositório permitam.

**Quando usar o botão de Fechar PR?**

* Se as mudanças do PR não forem mais necessárias.
* Se houver uma abordagem melhor para resolver o problema.
* Se as alterações forem implementadas de outra forma em um PR diferente.

Fechar um PR sem mesclar deve ser uma decisão consciente, pois isso indica que as alterações propostas não farão parte do projeto.

## Barra Lateral

A barra lateral do Pull Request exibe informações importantes para acompanhar e gerenciar a revisão do código. A seguir, destacamos algumas das principais opções disponíveis.

<figure><img src="../../.gitbook/assets/PR barra lateral.png" alt=""><figcaption></figcaption></figure>

* **Reviewers**: Lista as pessoas responsáveis por revisar o PR.
  * Ao clicar no ícone de engrenagem, é possível solicitar ou remover pessoas revisoras.
  * As pessoas revisoras podem aprovar, solicitar mudanças ou deixar comentários para ajudar na melhoria do código.
* **Labels**: Etiquetas visuais que ajudam a categorizar o PR.
  * Labels podem indicar o tipo de alteração (por exemplo, _bug fix_, _feature_, _documentation_).
  * No ícone de engrenagem, é possível adicionar ou remover labels, e as mudanças são aplicadas imediatamente.
* **Notifications**: Aqui você pode configurar quais as notificações relacionadas ao PR que você receberá. As ações feitas nas notificações, como alterar preferências, são refletidas na barra lateral.
* **Links para Issues Relacionadas e Pull Requests**: Outras issues ou Pull Requests relacionados podem ser mencionadas ou vinculadas diretamente, ajudando a organizar a discussão entre várias issues.
* **Participants**: Lista todas as pessoas que interagiram com o PR, seja comentando, revisando ou reagindo.
  * Novas participações e alterações são atualizadas em tempo real.

#### **Notas**

* **Mencionar Contas Usuárias**: Mencionar contas usuárias com `@conta` no descrição do PR ou nos comentários notifica as contas usuárias mencionados, permitindo fácil colaboração e engajamento.

***

A seguir, exploraremos o processo de revisão e aprovação de Pull Requests.

