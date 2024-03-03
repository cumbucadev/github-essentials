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

# 🛠️ Sistemas Centralizados x Distribuídos

### **Sistemas Centralizados**

A primeira solução de Sistemas de Controle de Versão criada foi com uma arquitetura centralizada, com um único repositório central onde todo o histórico de alterações e versões do código era armazenado.















Os usuários fazem check-in (envio de alterações) e check-out (obtenção de uma cópia atualizada) do código desse repositório central.

1. **Repositório Centralizado**: É o ponto central onde todo o código-fonte e histórico de versões são armazenados. Todos os desenvolvedores trabalham diretamente com este repositório para obter versões atualizadas do código e para enviar suas alterações.
2. **Checkout e Check-in**: Os desenvolvedores "checam" (checkout) uma cópia do código do repositório central para trabalhar localmente em suas máquinas. Após fazerem suas alterações, eles "checam" (check-in) suas modificações de volta para o repositório central.
3. **Controle de Concorrência**: Os sistemas centralizados gerenciam as mudanças concorrentes feitas por múltiplos desenvolvedores. Se dois desenvolvedores tentarem modificar o mesmo arquivo ao mesmo tempo, o sistema de controle de versão pode detectar e gerenciar essas conflitos.
4. **Histórico de Versões**: Um aspecto fundamental dos sistemas de controle de versão é a capacidade de acompanhar o histórico de alterações em um arquivo ao longo do tempo. Isso permite que os desenvolvedores voltem a versões anteriores do código, se necessário.
5. **Ramos (Branches)**: Muitos sistemas centralizados permitem que os desenvolvedores criem ramos (branches) para trabalhar em funcionalidades ou correções de bugs separadas do código principal. Os ramos podem ser mesclados (merged) de volta ao ramo principal quando estiverem prontos.



<figure><img src="../../.gitbook/assets/image (7).png" alt="" width="375"><figcaption></figcaption></figure>



Exemplos de sistemas centralizados de controle de versão incluem o Subversion (SVN) e o Microsoft Team Foundation Version Control (TFVC).

Embora os sistemas centralizados tenham sido amplamente utilizados no passado, muitas equipes estão migrando para sistemas de controle de versão distribuídos, como o Git, devido à sua flexibilidade, desempenho e recursos avançados de ramificação e mesclagem.



### **Sistemas Distribuídos**&#x20;

Também chamados de DVCS ()

Esses sistemas não dependem de um repositório central. Cada cópia do repositório contém todo o histórico de alterações, o que significa que os desenvolvedores podem trabalhar localmente e, em seguida, sincronizar suas alterações com os outros repositórios. Exemplos populares incluem Git, Mercurial e Bazaar.



Os sistemas distribuídos de controle de versão de código são uma evolução dos sistemas centralizados e oferecem algumas vantagens distintas.&#x20;

Aqui estão algumas características-chave dos sistemas descentralizados de controle de versão:

1. **Modelo de Repositório Distribuído**: Em sistemas descentralizados, cada desenvolvedor possui uma cópia completa do repositório, incluindo todo o histórico de versões. Isso significa que cada desenvolvedor tem acesso a todo o histórico do projeto e pode trabalhar offline, sem depender de uma conexão com o servidor central.
2. **Branching e Merging Flexíveis**: Os sistemas descentralizados de controle de versão, como o Git, oferecem recursos avançados de branching e merging. Os desenvolvedores podem criar facilmente ramos (branches) para trabalhar em novas funcionalidades ou correções de bugs sem interferir no ramo principal do projeto. Os merges são geralmente mais simples e eficientes, permitindo uma integração contínua e sem problemas das alterações.
3. **Segurança e Backup**: Como cada desenvolvedor possui uma cópia completa do repositório, os sistemas descentralizados oferecem uma camada adicional de segurança e backup. Se o servidor central falhar, os desenvolvedores ainda têm acesso a todo o histórico e podem restaurar o projeto a partir de suas cópias locais.
4. **Colaboração Distribuída**: Os sistemas descentralizados facilitam a colaboração entre equipes distribuídas geograficamente. Os desenvolvedores podem trabalhar em seus próprios ramos e mesclar suas alterações de forma independente, sem depender de uma conexão de rede constante.
5. **Flexibilidade**: Os sistemas descentralizados oferecem mais flexibilidade em relação à estrutura do repositório e aos fluxos de trabalho de desenvolvimento. Os desenvolvedores podem adotar o modelo de desenvolvimento que melhor se adapta às necessidades do projeto.



<figure><img src="../../.gitbook/assets/image (8).png" alt="" width="375"><figcaption></figcaption></figure>



Em resumo, os sistemas descentralizados de controle de versão oferecem mais flexibilidade, segurança e eficiência em comparação com os sistemas centralizados. Isso os torna uma escolha popular para projetos de desenvolvimento de software em uma ampla gama de cenários.



O Git é o sistema de controle de versão descentralizado mais popular e amplamente utilizado, mas também existem outras opções, como Mercurial e Bazaar.



### Diferenças

As diferenças principais entre os sistemas centralizados e descentralizados de controle de versão de código estão relacionadas à arquitetura, à forma como lidam com ramificação e mesclagem, à disponibilidade offline e à gestão de repositórios. Aqui estão as diferenças principais:



1. **Arquitetura**:
   * Centralizado: Em um sistema centralizado, há um único repositório central que armazena todas as versões do código. Os desenvolvedores interagem diretamente com esse repositório central.
   * Descentralizado: Em um sistema descentralizado, cada desenvolvedor tem uma cópia completa do repositório, incluindo todo o histórico de versões. Não há necessidade de um repositório central.
2. **Ramificação e Mesclagem**:
   * Centralizado: Os sistemas centralizados de controle de versão geralmente têm suporte limitado para ramificação e mesclagem. As operações de ramificação e mesclagem podem ser mais complicadas e propensas a erros.
   * Descentralizado: Os sistemas descentralizados, como o Git, oferecem recursos avançados de ramificação e mesclagem. Os desenvolvedores podem criar ramos facilmente e mesclar suas alterações de forma eficiente.
3. **Disponibilidade Offline**:
   * Centralizado: Em um sistema centralizado, os desenvolvedores precisam de acesso contínuo ao servidor central para realizar operações de controle de versão.
   * Descentralizado: Os sistemas descentralizados permitem que os desenvolvedores trabalhem offline, pois têm uma cópia completa do repositório em suas máquinas locais. Eles podem realizar operações de controle de versão localmente e sincronizar suas alterações mais tarde.
4. **Gestão de Repositórios**:
   * Centralizado: Em sistemas centralizados, a gestão do repositório é centralizada e controlada por uma única entidade. Os desenvolvedores dependem do servidor central para todas as operações.
   * Descentralizado: Em sistemas descentralizados, cada desenvolvedor pode gerenciar seu próprio repositório localmente. Isso oferece mais autonomia e flexibilidade aos desenvolvedores.

Em resumo, os sistemas descentralizados de controle de versão, como o Git, oferecem maior flexibilidade, eficiência e segurança em comparação com os sistemas centralizados. Eles se tornaram a escolha preferida para muitos projetos de desenvolvimento de software devido às suas características avançadas de ramificação e mesclagem, disponibilidade offline e gestão descentralizada de repositórios.



### Fluxos de Trabalho

As diferenças nos fluxos de trabalho entre sistemas centralizados e descentralizados de controle de versão geralmente refletem suas arquiteturas e funcionalidades específicas. Aqui estão algumas diferenças comuns nos fluxos de trabalho:

1. **Fluxo de Trabalho Centralizado**:
   * **Checkout e Check-in**: Os desenvolvedores normalmente realizam um "checkout" de uma versão do código do repositório central para trabalhar localmente. Depois de fazerem as alterações necessárias, eles realizam um "check-in" das suas modificações de volta ao repositório central.
   * **Branches Centrais**: Os branches em um sistema centralizado geralmente são usados de forma limitada e muitas vezes são criados apenas para grandes funcionalidades ou releases.
   * **Atualização Frequente**: Os desenvolvedores precisam se atualizar regularmente para garantir que estão trabalhando com a versão mais recente do código no repositório central.
   * **Dependência do Servidor Central**: Todos os desenvolvedores dependem do servidor central para realizar operações de controle de versão, o que pode resultar em gargalos de desempenho e disponibilidade.
2. **Fluxo de Trabalho Descentralizado**:
   * **Branches Locais**: Os desenvolvedores frequentemente criam branches locais para trabalhar em funcionalidades específicas ou correções de bugs. Eles têm mais liberdade para experimentar e testar ideias em seus próprios ambientes locais.
   * **Ramificação e Mesclagem Flexíveis**: Os sistemas descentralizados, como o Git, facilitam a criação, mesclagem e exclusão de branches. Isso permite fluxos de trabalho mais complexos e flexíveis.
   * **Trabalho Offline**: Os desenvolvedores podem trabalhar offline em suas cópias locais do repositório e sincronizar suas alterações posteriormente, o que é útil em situações onde a conectividade de rede é limitada ou intermitente.
   * **Repositórios Remotos**: Além do repositório local, os desenvolvedores também podem trabalhar com repositórios remotos, o que facilita a colaboração e a distribuição do código entre equipes e locais geograficamente dispersos.

Em resumo, os fluxos de trabalho em sistemas centralizados tendem a ser mais lineares e dependem fortemente do servidor central, enquanto os sistemas descentralizados oferecem maior flexibilidade, autonomia e recursos avançados de ramificação e mesclagem, permitindo uma colaboração mais eficaz e adaptável.



{% embed url="https://faun.pub/centralized-vs-distributed-version-control-systems-a135091299f0" %}

{% embed url="https://www.linkedin.com/pulse/centralized-version-control-systems-cvcs-distributed-dvcs-marathe" %}

