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

A estrutura distribuída foi criada para endereçar a maior parte dos problemas presentes nos sistemas centralizados.



**Um único ponto de falha coloca em risco os dados**

Caso algo acontecer com o servidor e o repositório central for pedido, no caso dos sistemas centralizados, isso resultaria em uma perda definitiva do código.&#x20;

Já no sistema distribuído, como cada desenvolvedor possui uma cópia completa do repositório em seus computadores, os desenvolvedores ainda têm acesso a todo o histórico e podem restaurar o projeto a partir de suas cópias locais.



**Necessidade de conexão com o servidor**

Em um sistema centralizado, as pessoas precisam de acesso contínuo ao servidor central para realizar operações de controle de versão. Caso o servidor venha a cair, por exemplo, ninguém mais consegue trabalhar.

Já nos sistemas distribuído, não há a dependência de conexão o servidor. Isso significa que a maior parte do desenvolvimento pode ser realizada _offline_. Apenas as operações de enviar (push) e receber (pull) modificações que ficam restringidas a necessidade de uma conexão.

Os colaboradores possuem todo i histórico de execução do projeto em seus próprios computadores, o que significa que podem fazer alterações diretamente em seus repositórios.&#x20;

Desta forma, permite que os membros da equipe fazem as suas modificações como um único conjunto de alterações. Deixando para enviar essas alterações quando tiver uma conexão novamente

**Conexão lenta atrasa o desenvolvimento**

// todo

**Poucos momentos estáveis para enviar (push) mudanças**

// todo



O Git é o sistema de controle de versão descentralizado mais popular e amplamente utilizado, mas também existem outras opções, como Mercurial e Bazaar.











***



<figure><img src="../../.gitbook/assets/ajuste.png" alt=""><figcaption><p>Mapa do Funcionamento de um Sistema de Controle de Versão Distribuído</p></figcaption></figure>



Em resumo, os sistemas descentralizados de controle de versão oferecem mais flexibilidade, segurança e eficiência em comparação com os sistemas centralizados. Isso os torna uma escolha frequente para projetos de desenvolvimento de software em uma ampla gama de cenários.



As vantagens são:



