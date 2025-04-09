---
description: O quê são, para que servem e quais são suas principais funcionalidades.
layout:
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

# 2.1 Introdução a sistemas de controle de versão

## Motivação

Você consegue se lembrar — ou imaginar — como era pedir para alguém revisar um documento antes do surgimento de ferramentas como Google Docs ou Microsoft Word Online?

<div align="center" data-full-width="true"><figure><img src="../../.gitbook/assets/tweet-1014533073021620224.png" alt="" width="375"><figcaption><p><a href="https://twitter.com/anttrindade/status/1014533073021620224?s=20">https://twitter.com/anttrindade/status/1014533073021620224</a></p></figcaption></figure></div>

A colaboração em documentos muitas vezes exigia o envio de versões por e-mail ou compartilhamento físico de arquivos em dispositivos de armazenamento, como pen drives. Isso tornava o processo lento, sujeito a confusões com múltiplas versões e erros de sincronização.

E se fosse preciso voltar a uma versão anterior? Era necessário abrir cada arquivo antigo, um por um, até encontrar o certo.

Escrever em grupo também era um desafio. Uma estratégia comum era cada pessoa usar uma cor diferente para identificar suas contribuições. Os arquivos iam e voltavam, acumulando edições e, muitas vezes, problemas. Um pouco rudimentar, não acha?

<figure><img src="../../.gitbook/assets/image (13) (1) (1) (1).png" alt=""><figcaption><p>Como os Maias e Incas trabalhavam antigamente (risos!)</p></figcaption></figure>

Ferramentas colaborativas como Google Docs surgiram para resolver esses problemas. Elas permitem escrever, revisar e acompanhar alterações em tempo real, com várias pessoas ao mesmo tempo.

<figure><img src="../../.gitbook/assets/Screenshot 2024-03-16 at 16.58.32.png" alt=""><figcaption></figcaption></figure>

Além disso, mantêm um histórico completo de versões, mostrando quem alterou o quê e quando, e permitindo reverter mudanças com facilidade.

<figure><img src="../../.gitbook/assets/Histórico de Versão GDocs.png" alt=""><figcaption></figcaption></figure>

Curiosamente, os mesmos desafios enfrentados na escrita de documentos também aconteciam no desenvolvimento de software antes dos sistemas de controle de versão.

## Sistemas de controle de versão

Sistemas de controle de versão (Version Control Systems — VCS) são ferramentas que acompanham todas as alterações feitas em um conjunto de arquivos ao longo do tempo. Embora possam ser usados para diversos tipos de arquivos, seu uso mais comum é no desenvolvimento de software.

Eles permitem que várias pessoas trabalhem simultaneamente no mesmo projeto, facilitando a colaboração, o rastreamento de mudanças, a identificação de erros e a reversão de alterações quando necessário.

Esses sistemas são fundamentais para o trabalho em equipe, pois ajudam a manter a integridade do código, evitam conflitos e aumentam a produtividade no desenvolvimento.

### Funcionalidades

As principais funcionalidades oferecidas por sistemas de controle de versão incluem:

* **Reversão de alterações:** Permite voltar para versões anteriores do código, útil para desfazer alterações problemáticas.
* **Colaboração:** Facilita o trabalho em equipe, permitindo que vários pessoas contribuam para o mesmo projeto simultaneamente de maneira organizada.
* **Auditoria e rastreamento de alterações:** Registrar quem fez o quê, quando e por quê.
* **Ramificação e mesclagem:** Permite criar “cópias” do projeto para testar novas ideias ou corrigir problemas sem afetar o código principal, podendo depois mesclar tudo novamente. Posteriormente, as ramificações podem ser mescladas de volta ao código principal.

### Tipos &#x20;

Existem dois tipos principais de sistemas de controle de versão: os **centralizados** e os **distribuídos**.

Os sistemas centralizados foram os primeiros a surgir e marcaram o início do uso colaborativo no controle de versões. Já os distribuídos vieram depois, como uma evolução dos centralizados, trazendo mais flexibilidade e autonomia para o trabalho em equipe.

***

Nas próximas seções, vamos entender como cada tipo de sistema de controle de versão funciona e quais as principais diferenças entre eles.
