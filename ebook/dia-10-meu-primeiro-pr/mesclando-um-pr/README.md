# Mesclando um PR

Agora que conseguimos a aprovação de todas as pessoas revisoras, é hora de mesclar a nossa sugestão de mudança com o branch principal.

## Tipos de Mesclagem

O GitHub oferece três tipos diferentes de mesclagem de um PR. Vamos utilizar um exemplo como base para entender a diferença entre eles e quando usar cada um.

Imagine que temos um site, e a última alteração feita no `main` foi "Adiciona página 'Sobre Nós'". Há um branch com uma nova feature chamado `feature-contato`. Nesse branch, foi feito um primeiro commit com a mensagem "Adiciona formulário de contato" e em seguida um segundo commit com a mensagem "Adiciona informação de endereço".

Para melhor visualizar, os logs ficariam assim:

**main**

```bash
git log --oneline
```

```bash
abcd123 Adiciona página 'Sobre Nós'
```

**feature-contato**

```bash
git log --oneline
```

```bash
6d5c4b3 Adiciona informação de endereço
7f6e5d4 Adiciona formulário de contato
```

### 1. Merge Commit (Padrão)

* Adiciona todos os commits do branch ao branch de destino e cria um commit extra para a mesclagem.
* Mantém o histórico completo das alterações.
* Ideal para manter rastreabilidade quando várias pessoas contribuem.

#### Após o Merge Commit

```bash
git log --oneline
```

```bash
9a8b7c3 Merge branch 'feature-contato' into main
6d5c4b3 Adiciona informação de endereço
7f6e5d4 Adiciona formulário de contato
abcd123 Adiciona página 'Sobre Nós'
```

#### Prós e Contras

* ✅ Mantém o histórico completo de commits.
* ✅ Facilita a rastreabilidade de mudanças.
* ❌ Pode deixar o histórico mais poluído com commits de merge.

### 2. Squash and Merge

* Junta todos os commits do PR em um único commit antes de mesclar.
* Deixa o histórico mais limpo, sem múltiplos commits pequenos.

#### Após Squash and Merge

```bash
git log --oneline
```

```bash
8f7e6d5 Adiciona página de contato com formulário e endereço
abcd123 Adiciona página 'Sobre Nós'
```

#### Prós e Contras

* ✅ Mantém o histórico mais organizado.
* ✅ Remove commits pequenos e irrelevantes.
* ❌ Perde a granularidade dos commits originais.

### 3. Rebase and Merge

* Aplica os commits do PR diretamente no branch de destino, sem um commit de mesclagem.
* O histórico fica linear, sem "commits extras" de mesclagem.

#### Após Rebase and Merge

```bash
git log --oneline
```

```bash
6d5c4b3 Adiciona informação de endereço
7f6e5d4 Adiciona formulário de contato
abcd123 Adiciona página 'Sobre Nós'
```

#### Prós e Contras

* ✅ Mantém um histórico limpo e linear.
* ✅ Evita commits de merge desnecessários.
* ❌ Pode causar problemas em branches compartilhados.

{% hint style="danger" %}
**Atenção:** Não use `Rebase and Merge` em **branches compartilhados**!

Um **branch compartilhado** é aquele onde várias pessoas colaboram ao mesmo tempo.&#x20;

Imagine que você e sua colega estão trabalhando no branch `feature-contato`.

1. **Você faz um commit e envia para o repositório remoto (`push`)**
2. **Sua colega faz um `pull` para trabalhar na mesma feature**
3. **Você decide fazer um `rebase` no branch antes de mesclar**

O `rebase` altera o histórico do branch, reescrevendo os commits. Agora, o histórico do repositório remoto está diferente do que sua colega baixou. Quando ela tentar enviar suas alterações (`push`), o Git pode rejeitar, pois os commits que ela tem localmente não correspondem mais aos do repositório remoto.

* ✅ **Rebase é seguro para branches que só você está usando.**
* 🚨 **Em branches compartilhados, prefira `Merge Commit` ou `Squash and Merge`.**
{% endhint %}

## Qual Devo Utilizar?

Se você é iniciante, o mais recomendado é utilizar **Merge Commit**, pois ele mantém o histórico completo e facilita o rastreamento das mudanças.

Caso esteja contribuindo para um projeto já estabelecido, siga as diretrizes definidas por ele. Alguns projetos podem preferir **Squash and Merge** para manter um histórico mais limpo ou **Rebase and Merge** para um histórico linear.

## Como Mesclar um PR no GitHub

1. Vá até o repositório no GitHub.
2. Acesse a aba **Pull Requests**.
3. Escolha o PR que deseja mesclar.
4. Revise o código e verifique se passou nos testes.
5. Clique no botão verde **Merge pull request** na seção **Verificação de Status** da [aba-conversation.md](../pagina-do-pr/aba-conversation.md "mention").
6. Escolha o método de mesclagem.
7. Confirme clicando em **Confirm merge**.

***

Para mais informações sobre mesclagem de PRs, acessa a [Documentação Oficial do GitHub](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/merging-a-pull-request).

Depois de entender como mesclar um PR no GitHub de forma simples e eficiente, vamos seguir adiante e explorar o passo a passo para mesclar o PR do nosso exemplo no repositório **hello-world**.
