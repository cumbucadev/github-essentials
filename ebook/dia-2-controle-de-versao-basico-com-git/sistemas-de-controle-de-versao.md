---
description: O quê são, para que servem e quais são suas principais funcionalidades.
cover: ../.gitbook/assets/Cabeçalho (1).svg
coverY: 0
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Sistemas de Controle de Versão

Você consegue se lembrar ou imaginar como era pedir para alguém revisar um documento antes do surgimento de plataformas de edição de textos colaborativa, como Google Docs e Microsoft Word online?

<div align="center" data-full-width="true">

<figure><img src="../.gitbook/assets/tweet-1014533073021620224.png" alt="" width="375"><figcaption><p><a href="https://twitter.com/anttrindade/status/1014533073021620224?s=20">https://twitter.com/anttrindade/status/1014533073021620224</a></p></figcaption></figure>

</div>

A colaboração em documentos muitas vezes exigia o envio de versões por e-mail ou compartilhamento físico de arquivos em dispositivos de armazenamento, como pen drives. Isso tornava o processo de edição em equipe demorado e propenso a erros de versão.&#x20;

E quando você precisava voltar para uma versão anterior? O processo era bastante inconveniente, pois você era obrigado a abrir individualmente cada um dos documentos antigos até encontrar a versão correta.

Ou você lembra como era quando se precisava escrever um documento em conjunto com uma ou mais pessoas?

<figure><img src="../.gitbook/assets/image (2).png" alt="" width="375"><figcaption></figcaption></figure>

Um dos artifícios mais utilizados era cada pessoa escrever de uma cor diferente para facilmente identificar o quê foi incluído por quem e ficar reenviando os arquivos ao longo da escrita.



Ferramentas como o Google docs surgiram para facilitar estes tipos de tarefas. Com ele, fica muito fácil colaborar e revisar documentos em tempo real com muitas pessoas.



<figure><img src="../.gitbook/assets/image (3).png" alt="" width="375"><figcaption></figcaption></figure>

Essas plataformas, mantêm um histórico detalhado de revisões, permitindo que os usuários vejam quem fez quais alterações e quando. Isso é útil para rastrear o progresso do trabalho, identificar quem fez determinadas edições e reverter para versões anteriores, se necessário.

<figure><img src="../.gitbook/assets/image (5).png" alt="" width="375"><figcaption></figcaption></figure>



Exatamente os mesmo problemas citados para escrita de documentos de texto ocorrem para escrita de documentos de código.



por que

o quê é

funcionalidades



Sistemas de controle de versão (Version Control Systems - VCS) são ferramentas utilizadas no desenvolvimento de software para gerenciar e controlar as mudanças no código-fonte e na documentação de um projeto ao longo do tempo. Eles permitem que várias pessoas trabalhem simultaneamente no mesmo projeto, facilitando a colaboração, rastreamento de alterações, identificação de problemas e reversão de modificações, entre outras funcionalidades.

Existem dois tipos principais de sistemas de controle de versão: sistemas centralizados e sistemas distribuídos.

1. **Sistemas Centralizados**: Nesses sistemas, há um único repositório central onde todo o histórico de alterações e versões do código é armazenado. Os usuários fazem check-in (envio de alterações) e check-out (obtenção de uma cópia atualizada) do código desse repositório central. Exemplos incluem CVS (Concurrent Versions System) e SVN (Subversion).
2. **Sistemas Distribuídos**: Esses sistemas não dependem de um repositório central. Cada cópia do repositório contém todo o histórico de alterações, o que significa que os desenvolvedores podem trabalhar localmente e, em seguida, sincronizar suas alterações com os outros repositórios. Exemplos populares incluem Git, Mercurial e Bazaar.

As principais funcionalidades oferecidas por sistemas de controle de versão incluem:

* **Rastreamento de alterações**: Registra quem fez o que, quando e por quê em relação ao código e à documentação.
* **Ramificação e mesclagem**: Permite que os desenvolvedores criem ramificações (cópias separadas do código) para desenvolver novos recursos ou corrigir bugs sem interferir no código principal. Posteriormente, as ramificações podem ser mescladas de volta ao código principal.
* **Reversão de alterações**: Permite reverter para versões anteriores do código, útil para corrigir bugs ou desfazer alterações problemáticas.
* **Colaboração**: Facilita o trabalho em equipe, permitindo que vários desenvolvedores contribuam para o mesmo projeto simultaneamente.
* **Auditoria e rastreamento**: Fornece um histórico detalhado de todas as alterações feitas no código, facilitando a auditoria e a investigação de problemas.

Esses sistemas são essenciais para o desenvolvimento de software em equipe, pois ajudam a manter a integridade do código-fonte, facilitam a colaboração e aumentam a eficiência do desenvolvimento.

\
