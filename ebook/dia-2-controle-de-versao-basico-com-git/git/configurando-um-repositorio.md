---
description: >-
  Nesta seção, exploraremos como configurar o Git para suas necessidades. Você
  aprenderá como usar o comando git config para personalizar seu ambiente de
  desenvolvimento.
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

# Configurando um Repositório

## git config

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">config</mark> é usado para configurar o Git no seu computador. Neste contexto, entenda configurar como customizar ou personalizar o Git de acordo com suas preferências.

Existem duas maneiras de configurar o Git no seu computador:

1. **Configuração Global**: Essas configurações se aplicam a todos os seus projetos Git no sistema. Elas são armazenadas no arquivo `.gitconfig` no diretório do usuário. No Windows, você pode encontrá-lo em `C:\Users\maria`, no macOS em `/Users/maria`, e no Linux em `/home/maria`, onde "_maria_" é o nome do usuário neste exemplo. \
   Configurações globais são úteis para definir preferências pessoais que se aplicam a todos os seus projetos.
2. **Configuração Local**: Essas configurações são específicas para um projeto Git individual. Elas são armazenadas no arquivo `.git/config` dentro do diretório do projeto. Configurações locais sobrescrevem as configurações globais quando ambas são definidas, permitindo personalização por projeto.

Você pode escolher entre aplicar uma configuração globalmente para todos os seus projetos ou/e localmente para um projeto específico, oferecendo flexibilidade na personalização das configurações do Git de acordo com suas necessidades.

> imagem: configs globais vs locais. Onde o arquivo fica localizado e a que se aplica

### Estrutura

O formato base do comando <mark style="color:purple;">git</mark> <mark style="color:orange;">config</mark> é:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">config</mark> <mark style="color:blue;">\[opções]</mark> <mark style="color:green;">chave</mark> <mark style="color:green;">valor</mark>

Em que:

* <mark style="color:blue;">**\[opções]**</mark>** (opcional):** define o escopo do comando ou fornecem outros modificadores. O escopo pode ser, por exemplo,`--global` para aplicar a configuração a nível global ou `--local` para aplicar a configuração apenas ao repositório atual.
* <mark style="color:green;">**chave**</mark>: se refere ao nome da configuração que você deseja definir ou modificar.\
  Exemplos: user.name, user.email, core.editor.
* <mark style="color:green;">**valor**</mark>: se refere ao valor que você deseja atribuir à chave.\
  Exemplos: "Seu Nome", "seu.email@exemplo.com", "nome-do-editor".

### Exemplos de Uso

#### Exemplos de Configurações

Essas são algumas das propriedades que podem ser configuradas:

1. `user.name`: Define o nome de usuário associado aos commits.\
   É como você se identifica nos commits, então outros sabem quem fez as alterações.\
   Exemplo definindo nome do usuário global como `maria`:  \
   <mark style="color:purple;">git</mark> <mark style="color:orange;">config</mark> <mark style="color:blue;">--global</mark> <mark style="color:green;">user.name "Maria"</mark>
2. `user.email`: Define o email associado aos commits.\
   É o seu endereço de email associado aos commits para que outros possam contatá-lo se necessário.\
   Exemplo definindo email do usuário global como `maria@exemplo.com`:  \
   <mark style="color:purple;">git</mark> <mark style="color:orange;">config</mark> <mark style="color:blue;">--global</mark> <mark style="color:green;">user.email "maria@exemplo.com"</mark>&#x20;
3. `core.editor`: Define o editor de texto usado para mensagens de commit.\
   É o programa que você usa para escrever mensagens de commit.\
   Exemplo definindo o editor de texto padrão global como o Visual Studio Code: \
   <mark style="color:purple;">git</mark> <mark style="color:orange;">config</mark> <mark style="color:blue;">--global</mark> <mark style="color:green;">core.editor "code --wait"</mark>
4. `color.ui`: Ativa ou desativa a coloração na saída do Git. \
   Deixa as mensagens do Git mais coloridas para que você possa identificar informações mais facilmente.\
   Exemplo ativando globalmente a coloração na saída do Git: \
   <mark style="color:purple;">git</mark> <mark style="color:orange;">config</mark> <mark style="color:blue;">--global</mark> <mark style="color:green;">color.ui true</mark>
5. `alias.*`: Define atalhos personalizados para comandos Git. \
   São atalhos personalizados para que você possa digitar menos ao usar certos comandos Git.\
   Exemplo criando um atalho global `"ci"` para o comando 'commit':  \
   <mark style="color:purple;">git</mark> <mark style="color:orange;">config</mark> <mark style="color:blue;">--global</mark> <mark style="color:green;">alias.ci commit</mark>
6. `init.defaultBranch`: Define o nome padrão do branch inicial.\
   Define o nome padrão do branch inicial quando você cria um novo repositório.\
   Exemplo definindo o nome padrão do branch inicial como 'dev' para um projeto específico:\
   <mark style="color:purple;">git</mark> <mark style="color:orange;">config</mark> <mark style="color:blue;">--local</mark> <mark style="color:green;">init.defaultBranch main</mark>

#### Exemplo Configurando Dois Emails

Configurar diferentes e-mails no Git pode ser super útil, especialmente quando você tem uma conta pessoal e outra da empresa. Vamos ver como essa configuração global e local pode fazer a diferença no seu dia a dia!

Imagine que você trabalha em vários projetos, tanto pessoais quanto profissionais. Usar a configuração global do Git permite que você configure um e-mail padrão que será usado em todos os repositórios. Isso é ótimo para simplificar as coisas, mas e se você quiser separar suas identidades? É aqui que a configuração local entra em cena, e é super fácil de fazer!

Vamos começar com a configuração global. Digamos que você queira usar seu e-mail pessoal como padrão. Basta abrir o terminal e digitar:

```sh
git config --global user.email "seu-email@pessoal.com"
```

Agora, todos os seus commits em qualquer repositório vão usar este e-mail. Mas o que acontece quando você está trabalhando em um projeto da empresa e precisa usar seu e-mail corporativo? Sem problemas! Você pode configurar um e-mail específico apenas para esse projeto.

Aqui está como fazer isso. Vá para o diretório do seu projeto da empresa:

```sh
cd ~/workspace/projeto-da-empresa
git config user.email "seu-email@empresa.com"
```

Pronto! Agora, todos os commits feitos nesse repositório usarão seu e-mail corporativo.&#x20;

Por exemplo este commit será associado ao e-mail "seu-email@empresa.com":

```sh
cd ~/workspace/projeto-da-empresa
git commit -m "Implementação da nova funcionalidade"
```

E este ao e-mail "seu-email@pessoal.com":

```sh
cd ~/workspace/projeto-pessoal
git commit -m "Adicionado novo recurso ao blog pessoal"
```

Assim, você mantém suas identidades digitais separadas e claras, tanto no ambiente pessoal quanto no profissional. Configurar esses e-mails é fácil e faz toda a diferença na organização do seu trabalho.



{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`config`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-config).
{% endhint %}
