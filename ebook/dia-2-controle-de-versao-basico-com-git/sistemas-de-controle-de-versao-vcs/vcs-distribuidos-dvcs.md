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

# VCS Distribuídos (DVCS)

### **Sistemas Distribuídos**&#x20;

Os Sistemas de Controle de Versão Distribuídos (DVCS - _Distributed Version Control Systems_) são uma evolução dos sistemas centralizados. Neles, cada pessoa colaboradora faz a cópia do repositório central integralmente, obtendo assim o histórico completo do projeto em seu próprio computador.&#x20;

<figure><img src="../../.gitbook/assets/ebook images.png" alt=""><figcaption><p>Relembrando: Repositório Central = "Grande Pasta" que contém os arquivos, versões e metadados</p></figcaption></figure>

Diferentemente dos sistemas centralizados, onde apenas a versão mais recente é disponibilizada, neste modelo, cada cópia (clone) contém não apenas os arquivos do projeto, mas também todos os metadados associados ao repositório original.



<figure><img src="../../.gitbook/assets/15.png" alt=""><figcaption><p>Cada "Clone" faz uma cópia integral de todos os arquivos existentes</p></figcaption></figure>

A estrutura distribuída foi criada para endereçar a maior parte dos problemas percebidos nos sistemas centralizados.

### Motivação: endereçar problemas dos sistemas centralizados

**Um único ponto de falha coloca em risco os dados**

No sistema centralizado, caso algo venha a acontecer com o servidor e o repositório central for comprometido, isso resulta em uma perda definitiva do código.

Já no sistema distribuído, como cada pessoa colaboradora possui uma cópia completa do repositório em seu computador, tendo acesso a todo o histórico, é possível restaurar o projeto a partir de suas cópias locais.

**Necessidade de conexão com o servidor**

As pessoas dependem do acesso contínuo ao servidor central para realizar operações de controle de versão no sistema centralizado. Se o servidor ficar inacessível, por exemplo, todas as atividades de trabalho ficam interrompidas.

No sistema distribuído, entretanto, não há essa dependência de conexão com o servidor. Isso significa que a maior parte do desenvolvimento pode ser realizada _offline_. Apenas as operações de enviar (_**push**_) e receber (_**pull**_) modificações que ficam restringidas a necessidade de uma conexão.

As pessoas colaboradoras têm acesso ao histórico completo do projeto em seus próprios computadores, permitindo que façam alterações diretamente em seus repositórios locais. Isso possibilita que realizem suas modificações como um conjunto de alterações, adiando o envio para quando estiverem online novamente.

**Conexão lenta atrasa o desenvolvimento**

Em sistemas centralizados, os usuários enfrentam dificuldades ao realizar mudanças devido à comunicação necessária com o servidor remoto, o que torna o processo mais lento, especialmente em conexões de rede lentas.&#x20;

Por outro lado, em sistemas distribuídos, os usuários podem fazer alterações de forma ágil e autônoma em seus repositórios locais, permitindo trabalhar sem depender constantemente do servidor remoto, realizando suas modificações como um conjunto de alterações, adiando o envio para quando estiverem online novamente.

**Poucos momentos estáveis para enviar mudanças (push)**

// todo



O Git é o sistema de controle de versão descentralizado mais popular e amplamente utilizado, mas também existem outras opções, como Mercurial e Bazaar.











***



<figure><img src="../../.gitbook/assets/ajuste.png" alt=""><figcaption><p>Mapa do Funcionamento de um Sistema de Controle de Versão Distribuído</p></figcaption></figure>



Em resumo, os sistemas descentralizados de controle de versão oferecem mais flexibilidade, segurança e eficiência em comparação com os sistemas centralizados. Isso os torna uma escolha frequente para projetos de desenvolvimento de software em uma ampla gama de cenários.



As vantagens são:



