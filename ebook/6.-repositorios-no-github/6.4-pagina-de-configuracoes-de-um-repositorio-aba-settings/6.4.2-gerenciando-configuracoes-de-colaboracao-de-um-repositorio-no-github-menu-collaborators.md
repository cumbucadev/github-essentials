# Collaborators: Configurações de Colaboração

Nesta seção, você pode gerenciar quem tem acesso ao repositório e definir as permissões de cada pessoa. Para adicionar ou remover colaboradores, você precisa ter permissão de **Admin**.

## Como acessar a seção Collaborators&#x20;

### **Via aba Settings do repositório**

* Acesse a aba **Settings** do seu repositório no GitHub.
* Na barra de navegação lateral, clique no segundo item, chamado **Collaborators**.

### **Via link direto**

Outra opção é você acessar as configurações de colaboração do repositório diretamente utilizando o seguinte formato de URL:

> https://github.com/CONTA\_GITHUB/SEU\_REPOSITORIO/settings/access

Substitua `CONTA_GITHUB` pelo nome da sua conta no GitHub e `SEU_REPOSITORIO` pelo nome do seu repositório.\
\
Por exemplo:

> [https://github.com/aprendizCumbucaDev/hello-world/settings/access](https://github.com/aprendizCumbucaDev/hello-world/settings/access)

<figure><img src="../../.gitbook/assets/32- Settings Collaborators.png" alt=""><figcaption><p>Seção Collaborators da aba Settings de um repositório</p></figcaption></figure>

## Como Adicionar Pessoas Colaboradoras

1. Vá até a seção de configurações **Collaborators** do seu repositório.
2. Clique no botão **Add people**.
3. Digite o nome de pessoa usuária ou e-mail de quem deseja adicionar.

<figure><img src="../../.gitbook/assets/33 Add Colaborador 1.png" alt=""><figcaption><p>Diálogo de convite para colaboração em repositório</p></figcaption></figure>

5. Clique em **Add \<conta da pessoa usuária>**

<figure><img src="../../.gitbook/assets/34 Add Colaborador 2.png" alt=""><figcaption><p>Diálogo de convite para colaboração em repositório com pessoa usuária selecionada</p></figcaption></figure>

6. A pessoa colaboradora receberá um convite para aceitar o acesso ao repositório.

[Saiba mais sobre esta funcionalidade](https://docs.github.com/pt/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository).

## Gerenciando Permissões

Dependendo das configurações do repositório e das suas próprias permissões, pode ou não ser possível definir o nível de acesso ao convidar uma pessoa.

**Se a opção aparecer**, você poderá escolher um dos níveis de permissão disponíveis (explicados abaixo).

<figure><img src="../../.gitbook/assets/35- Add Colaborador 3 (1).png" alt=""><figcaption><p>Diálogo de convite para colação, etapa de seleção do nível de permissão</p></figcaption></figure>

**Se a opção não aparecer**, significa que o repositório já tem configurações predefinidas ou que sua conta não tem permissão para ajustá-las. Nesse caso, o GitHub atribuirá automaticamente um nível de permissão padrão com base nas configurações do repositório.

### Níveis de Permissão

Cada colaborador pode ter um nível de permissão diferente, de acordo com o que pode ou não fazer no repositório:

* **Read** → Pode visualizar o código, issues e pull requests, mas não pode modificar nada.
* **Triage** → Pode gerenciar issues e pull requests, ajudando na organização do repositório.
* **Write** → Pode contribuir com código e gerenciar issues e pull requests.
* **Maintain** → Pode gerenciar o repositório (configurações, branches, etc.), mas sem permissões administrativas.
* **Admin** → Tem controle total sobre o repositório, podendo alterá-lo completamente, inclusive excluí-lo.

Em **repositórios públicos**, qualquer pessoa pode visualizar o código, mas permissões adicionais podem ser necessárias para edição e colaboração.

Em **repositórios privados**, definir permissões corretamente é essencial para garantir o acesso adequado.

Se você está começando, geralmente terá permissão **Read** ou **Write**. Apenas os responsáveis pelo projeto devem ter permissão **Admin** para evitar mudanças acidentais.

[Saiba mais sobre esta funcionalidade](https://docs.github.com/en/organizations/managing-access-to-your-organizations-repositories/repository-roles-for-an-organization)
