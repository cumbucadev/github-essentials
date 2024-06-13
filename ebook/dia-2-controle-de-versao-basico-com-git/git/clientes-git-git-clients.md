---
description: >-
  Nesta seção, mergulharemos nas diferentes maneiras de interagir com o Git,
  seja através da Interface de Linha de Comando (CLI) ou da Interface Gráfica do
  Usuário (GUI).
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

# Clientes Git (Git Clients)

O Git é essencialmente um sistema de controle de versão. No entanto, não oferece uma maneira direta para que os usuários interagirem com ele. É necessária uma ferramenta adicional, chamada de cliente (_**Git Client**_), que provenha essa ponte entre o usuário e o Git em si.&#x20;

> Imagem: git <--> git client <--> usuário

Existem várias clientes que facilitam a comunicação entre o Git e o usuário. Alguns deles fornecem uma interface de linha de comando (CLI), enquanto outros oferecem uma interface gráfica do usuário (GUI):

<figure><img src="../../.gitbook/assets/image (16).png" alt="" width="375"><figcaption></figcaption></figure>

**Interface de Linha de Comando (Command Line Interface - CLI)**: Neste formato, os usuários interagem com o Git digitando comandos diretamente em um terminal ou prompt de comando. Aqui, os comandos são textuais e exigem que o usuário escreva para executar várias tarefas.

> Imagem: terminal de comando rodando algum comando git

**Interface Gráfica do Usuário (Graphical User Interface - GUI):** Esta abordagem é mais visual, permitindo que os usuários interajam com o Git clicando em botões, ícones e menus em um aplicativo gráfico. Aqui, as ações são realizadas de forma mais intuitiva, sem a necessidade de digitar comandos.

> Imagem: capturas de telas de diferentes clientes GUI com seus repectivos nomes/links

## Git CLI

Neste curso, utilizaremos o cliente oficial do Git: a [Git CLI](https://git-scm.com/book/en/v2/Getting-Started-The-Command-Line). A motivação por trás dessa escolha é:

1. Por ser a solução oficial, ela será sempre a mais atual e a única que fornecerá a capacidade de executar **todos** os comandos do Git. A maioria dos clientes com interfaces gráficas, por exemple, implementam apenas um subconjunto das funcionalidades do Git com o intuito de simplificar a utilização.
2. Se uma pessoa souber como utilizar a Git CLI, provavelmente também conseguirá facilmente entender como utilizar outros cliente com interfaces gráficas, enquanto o contrário nem sempre é verdadeiro.&#x20;
3. Embora a escolha do cliente seja uma questão de preferência pessoal, optar pela CLI oficial também significa que todos os usuários já terão as ferramentas de linha de comando prontas para uso, sem a necessidade de qualquer outra instalação ou configuração.

Caso, ainda sim, opte-se por utilizar um cliente com interface gráfica, aqui se encontram várias opções disponíveis:

{% embed url="https://git-scm.com/downloads/guis" %}

