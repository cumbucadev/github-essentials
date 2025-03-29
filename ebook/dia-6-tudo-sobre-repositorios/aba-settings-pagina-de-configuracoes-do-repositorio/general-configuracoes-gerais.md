# General: Configurações Gerais

A seção **General** é uma das áreas mais importantes para configurar os aspectos básicos do seu repositório no GitHub. Aqui, você pode ajustar o nome, a estrutura e funcionalidades que afetam o comportamento e a aparência do repositório. Além disso, também é onde você pode realizar ações críticas, como alterar a visibilidade ou até mesmo excluir o repositório.

É importante estar atento às implicações de cada configuração, já que algumas alterações podem afetar diretamente como os colaboradores e usuários interagem com o repositório. Vamos explorar as principais configurações que você encontrará nesta seção.

<figure><img src="../../.gitbook/assets/31 Settings General (3).png" alt=""><figcaption><p>Seção General da aba Settings de um repositório</p></figcaption></figure>

## General

### Repository name

Permite alterar o nome do repositório. Tenha cuidado ao mudar, pois isso pode afetar links já compartilhados e integrações existentes. O GitHub possui um sistema de redirecionamento que evita a quebra de links, mas é sempre recomendado atualizar documentações e integrações para evitar dependência desse redirecionamento.

Exemplo: Se um repositório chamado `meu-site` for renomeado para `site-novo`, qualquer pessoa ou sistema que tentava acessá-lo pelo nome antigo será automaticamente redirecionado para o novo nome. No entanto, links em documentações e configurações externas devem ser atualizados manualmente.

[Saiba mais sobre esta funcionalidade](https://docs.github.com/pt/repositories/creating-and-managing-repositories/renaming-a-repository)

### Template repository

Transforma o repositório em um modelo que pode ser usado para gerar novos repositórios com a mesma estrutura de diretórios e arquivos. Isso é útil quando você deseja criar vários projetos semelhantes com uma base inicial padronizada.

[Saiba mais sobre esta funcionalidade](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-template-repository)

## Default branch

Define o nome do branch principal do repositório, que será a base para commits e pull requests. Por padrão, ele se chama **main**, mas pode ser alterado conforme necessário.

[Saiba mais sobre esta funcionalidade](https://docs.github.com/pt/repositories/configuring-branches-and-merges-in-your-repository/managing-branches-in-your-repository/changing-the-default-branch).

## Social preview

Permite carregar uma imagem personalizada que será exibida quando o repositório for compartilhado em redes sociais. Isso ajuda a destacar o projeto visualmente.

Exemplo:

* Se o repositório for um projeto de site, você pode adicionar uma captura de tela da interface.
* Se for uma biblioteca, um logo pode ser uma boa opção.

[Saiba mais sobre esta funcionalidade](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/customizing-your-repositorys-social-media-preview)

## Features

Essa seção permite ativar ou desativar algumas funcionalidades extras do repositório.

### Wikis

Ativa uma área para criar documentações dentro do próprio repositório, facilitando o registro de informações importantes.

**Por que usar uma Wiki se já temos a documentação no código?**

* A Wiki pode ser mais acessível para pessoas que não têm familiaridade com Markdown ou edição de arquivos no repositório.
* Pode ser usada para armazenar informações que não precisam estar no código, como guias de contribuição ou explicações detalhadas.
* **Restrict editing to collaborators only**: Se ativado, apenas colaboradores do repositório poderão editar a Wiki. Caso contrário, qualquer pessoa poderá contribuir.

[Saiba mais sobre esta funcionalidade](https://docs.github.com/en/communities/documenting-your-project-with-wikis/about-wikis)

### Issues

Habilita um sistema de rastreamento de tarefas e bugs. Isso permite que usuários relatem problemas e sugiram melhorias de forma organizada.

Se você encontrar um erro no projeto ou tiver uma sugestão, pode abrir uma _Issue_ para comunicar isso aos mantenedores. As _Issues_ podem ser usadas para discutir novas funcionalidades ou corrigir problemas antes de serem resolvidos. Cada _Issue_ tem um número único e pode ser fechada quando resolvida.

**Issue templates**: Você pode criar modelos de _Issues_ para guiar os usuários ao reportar um problema ou sugerir uma melhoria.

[Saiba mais sobre esta funcionalidade](https://docs.github.com/en/issues/tracking-your-work-with-issues/about-issues)

### Sponsorships

Adiciona um botão de patrocínio ao repositório. Ele pode direcionar para o **GitHub Sponsors** ou outros métodos externos para doações financeiras, ajudando a sustentar o projeto.

[Saiba mais sobre esta funcionalidade](https://docs.github.com/en/sponsors/getting-started-with-github-sponsors/about-github-sponsors)

### Discussions

Cria um espaço para debates dentro do repositório, permitindo que os membros da comunidade façam perguntas e troquem ideias sem a necessidade de abrir issues.

[Saiba mais sobre esta funcionalidade](https://docs.github.com/en/discussions/collaborating-with-your-community-using-discussions/about-discussions)

### Projects

Habilita a funcionalidade de gerenciamento de projetos dentro do repositório. Com isso, é possível criar quadros organizacionais para acompanhar tarefas e progresso do desenvolvimento.

[Saiba mais sobre esta funcionalidade](https://docs.github.com/en/issues/planning-and-tracking-with-projects/about-projects)

## Danger Zone ⚠️

Esta seção contém configurações críticas que devem ser usadas com cuidado.

<figure><img src="../../.gitbook/assets/30 Danger Zone (1).png" alt=""><figcaption><p>Danger Zone da seção General da aba Settings de um repositório</p></figcaption></figure>

### **Change repository visibility**

Altera a visibilidade do repositório entre **público** e **privado**.

[Saiba mais sobre esta funcionalidade](https://docs.github.com/pt/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/setting-repository-visibility).

### **Transfer ownership**

Permite transferir o repositório para outra pessoa ou organização.

[Saiba mais sobre esta funcionalidade](https://docs.github.com/pt/repositories/creating-and-managing-repositories/transferring-a-repository).

### **Archive this repository**

Arquiva o repositório, tornando-o somente leitura.

[Saiba mais sobre esta funcionalidade](https://docs.github.com/pt/repositories/archiving-a-github-repository).

### **Delete this repository**

Exclui permanentemente o repositório. Essa ação não pode ser desfeita.

[Saiba mais sobre esta funcionalidade](https://docs.github.com/pt/repositories/creating-and-managing-repositories/deleting-a-repository).
