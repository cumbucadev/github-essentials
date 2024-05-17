---
description: //todo
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

# Salvando Alterações

#### Add

este comando adiciona um arquivo alterado a uma staging area, ou seja, o prepara para ser vinculado a um commit;&#x20;

[Documentação Oficial](https://git-scm.com/docs/git-add/pt\_BR)

#### Commit

este comando move os arquivos da state area para um repositório local;

[Documentação Oficial](https://git-scm.com/docs/git-commit/pt\_BR)

#### Status

#### Log



#### Push

este comando envia arquivos de um repositório local para um repositório remoto. No GitHub, por exemplo;

[Documentação Oficial](https://git-scm.com/docs/git-push/pt\_BR)

#### Pull

ao contrário do push, este comando traz um arquivo do repositório remoto para o repositório local.

[Documentação Oficial](https://git-scm.com/docs/git-pull/pt\_BR)

#### Merge

este comando serve para unir arquivos alterados ao arquivo original de um projeto. Em outras palavras, é ele quem une os branchs as commits. Log este comando permite a visualização do histórico de commits de um arquivo ou usuário, ou o acesso de uma versão específica.

[Documentação Oficial](https://git-scm.com/docs/git-merge/pt\_BR)

**Checkout**

[Documentação Oficial](https://git-scm.com/docs/git-checkout/pt\_BR)







***



1. **git init**: Este comando é usado para criar um novo repositório Git. Você executa este comando uma vez no diretório raiz do seu projeto para iniciar o controle de versão.
2. **git add**: Antes de salvar suas alterações no histórico do Git, você precisa adicioná-las à área de preparação (staging area). Este comando adiciona as alterações dos arquivos ao próximo commit. Por exemplo, para adicionar todos os arquivos modificados, você pode usar `git add .`.
3. **git commit**: Depois de adicionar suas alterações à área de preparação, você as confirma ao repositório com este comando. Cada commit tem uma mensagem descritiva que indica o propósito das alterações.
4. **git status**: Este comando mostra o estado atual do seu repositório Git. Ele exibe quais arquivos foram modificados, quais estão na área de preparação e quais ainda não foram rastreados pelo Git.
5. **git log**: Visualiza o histórico de commits do seu projeto. Ele mostra todos os commits que foram feitos, juntamente com as mensagens de commit, autores e timestamps.
6. **git branch**: Git permite trabalhar com várias ramificações (branches) do código. Este comando permite criar, listar e excluir ramificações. Por exemplo, `git branch nova-ramificacao` cria uma nova ramificação chamada "nova-ramificacao".
7. **git checkout**: Este comando permite navegar entre diferentes ramificações ou revisões do seu projeto. Por exemplo, `git checkout nome-da-ramificacao` muda para a ramificação especificada.
8. **git merge**: Quando você deseja combinar as alterações de uma ramificação com outra (geralmente de uma ramificação de desenvolvimento para uma ramificação principal), você usa este comando. Por exemplo, `git merge nome-da-ramificacao` mescla as alterações da ramificação especificada na ramificação atual.
9. **git pull**: Este comando é usado para baixar as últimas alterações do repositório remoto para o seu repositório local. Ele combina os comandos `git fetch` e `git merge` em uma única etapa.
10. **git push**: Depois de fazer alterações no seu repositório local e confirmá-las, você pode enviá-las para o repositório remoto com este comando. Por exemplo, `git push origin nome-da-ramificacao` envia as alterações da ramificação local para o repositório remoto, especificamente para a ramificação especificada.

Estes são os principais comandos que você usará ao trabalhar com o Git. Praticar o uso desses comandos em um projeto real ajudará a consolidar seu entendimento do fluxo de trabalho do Git.
