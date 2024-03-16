---
description: >-
  O quê são sistemas de controle de versão centralizados e distribuídos e quais
  são as suas diferenças
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

# VCS Centralizados

O Git, sistema de controle de versão que iremos utilizar nesse curso, é um sistema distribuído (_Distributed Version Control System_ - DVCS). Para entender a motivação de como foi criada de sua arquitetura e funcionamento, vale a pena entender primeiro como era feito antes dele.

### **O quê são (não sei nome melhor)**

A primeira solução para Sistemas de Controle de Versão consistiu em uma arquitetura **centralizada**, com um único repositório central onde todo o histórico de alterações e versões do código era armazenado.

Pense nesse repositório central como uma pasta gigante que contém todos os documentos do seu projeto. Não só a versão mais recente, mas também todas as versões anteriores e informações sobre cada uma delas. É como se fosse uma pasta que guarda toda a linha do tempo do seu projeto.

<figure><img src="../../.gitbook/assets/PAS TINHA.png" alt=""><figcaption></figcaption></figure>

Agora, você pode estar se perguntando como várias pessoas poderiam trabalhar nesse projeto ao mesmo tempo. Bem, o repositório central normalmente fica em um outro computador (servidor), para que mais pessoas possam acessá-lo. Caso contrário, todos teriam que compartilhar o mesmo computador.

<figure><img src="../../.gitbook/assets/PASTINHASDASDAA (2).png" alt=""><figcaption></figcaption></figure>

Cada pessoa que quer trabalhar no projeto precisa fazer uma cópia da versão mais recente para seu próprio computador, fazer suas mudanças e, em seguida, enviar de volta para o repositório central que está no servidor.

IMAGEM

Vamos entender como seria o fluxo de trabalho com um exemplo.

### Exemplo de Fluxo de Trabalho

Duas pessoas, X e Y, querem criar um blog. A pessoa X cria uma estrutura inicial do blog em seu computador e envia essa versão para o repositório central.

> <mark style="color:purple;">**imagem**</mark>

A pessoa Y se anima e quer também participar, criando o seu primeiro blog post. Para isso, Y precisa ter acesso à versão criada por X, que já está no repositório central no momento. Y precisa fazer um "_**checkout**_", que nada mais é que fazer uma cópia da última versão do projeto que está no repositório central para a sua máquina local.

> <mark style="color:purple;">**imagem**</mark>

Agora, Y tem acesso, em seu computador, ao projeto em sua versão mais atual. Y escreve seu primeiro blog post e precisa enviar as mudanças de volta para o repositório central, para que X também possa ver o seu belo trabalho. Y faz um "_**check-in**_" do seu código, ou seja, enviar uma cópia da sua versão para o repositório central

> <mark style="color:purple;">**imagem**</mark>

Tudo pronto! Temos no repositório central a versão mais recente do blog, com o post de Y. A versão inicial de X também está lá, guardada caso alguém precise consultá-la, ver diferenças, e assim por diante.

> <mark style="color:purple;">**imagem**</mark>

Mas, e se X também estiver empolgado e não conseguir esperar por Y? Ao mesmo tempo que Y, X começa a escrever seu próprio post. Quando X tenta enviar seu código para o repositório central, percebe que Y já enviou antes a sua versão.

> <mark style="color:purple;">**imagem**</mark>

E para piorar, X e Y modificaram o mesmo arquivo! E agora?

> <mark style="color:purple;">**imagem**</mark>

Bom, é aí que entra em jogo umas das principais funcionalidades de um sistema de controle de versão: o auxílio no Gerenciamento de Conflitos. O sistema lida com as mudanças feitas por diferentes colaboradores no mesmo arquivo, evitando conflitos e garantindo uma integração suave das alterações. Isso é feito por meio de um processo chamado 'mesclagem', que combina o trabalho de todos de forma harmoniosa e mantém a consistência do projeto.

Dessa forma, X consegue tranquilamente enviar suas modificações sem comprometer em nada as mudanças feitas por Y.

> <mark style="color:purple;">**imagem**</mark>

### Bleh (não sei que nome dar para seção)

1. **Repositório Centralizado**: É o ponto central onde todo o código-fonte e histórico de versões são armazenados. Todos os desenvolvedores trabalham diretamente com este repositório para obter versões atualizadas do código e para enviar suas alterações.
2. **Checkout e Check-in**: Os desenvolvedores "checam" (checkout) uma cópia do código do repositório central para trabalhar localmente em suas máquinas. Após fazerem suas alterações, eles "checam" (check-in) suas modificações de volta para o repositório central.
3. **Auxílio no Gerenciamento de Conflitos**: Os sistemas centralizados gerenciam as mudanças concorrentes feitas por múltiplos desenvolvedores. Se dois desenvolvedores tentarem modificar o mesmo arquivo ao mesmo tempo, o sistema de controle de versão pode detectar e gerenciar essas conflitos.
4. **Histórico de Versões**: Um aspecto fundamental dos sistemas de controle de versão é a capacidade de acompanhar o histórico de alterações em um arquivo ao longo do tempo. Isso permite que os desenvolvedores voltem a versões anteriores do código, se necessário.



<figure><img src="../../.gitbook/assets/image (7).png" alt="" width="375"><figcaption></figcaption></figure>

Exemplos de sistemas centralizados de controle de versão incluem o Subversion (SVN) e o Microsoft Team Foundation Version Control (TFVC). Embora os sistemas centralizados tenham sido amplamente utilizados no passado, muitas equipes estão migrando para sistemas de controle de versão distribuídos, como o Git, devido à sua flexibilidade, desempenho e recursos avançados que iremos começar a desvendar aos poucos daqui para frente.

