# Labels em PRs

Como já vimos anteriormente, labels são marcadores categorizados usados no GitHub para **organizar e classificar Issues e Pull Requests**. Elas ajudam a identificar rapidamente o status, prioridade e tipo de cada item, tornando a colaboração mais eficiente, especialmente em projetos de código aberto.

## **Labels em Issues vs. Labels em Pull Requests**

As labels podem ser aplicadas tanto em Issues quanto em Pull Requests, mas possuem finalidades distintas, uma vez que:

* **Issues** representam tarefas a serem realizadas.
* **Pull Requests** indicam trabalho em andamento ou concluído.

### **Labels em Issues**

Nas Issues, as labels ajudam a **classificar e organizar problemas e sugestões antes que alguém trabalhe neles**. Algumas categorias comuns incluem:

* **Tipo** – bug (erro), feature request (solicitação de funcionalidade), documentação (documentação).
* **Dificuldade** – good first issue (boa primeira issue), help wanted (ajuda necessária).
* **Área do código** – frontend (frontend), backend (backend), API (API).
* **Status** – triaged (triado), needs discussion (precisa de discussão).
* **Prioridade** – high priority (alta prioridade), low priority (baixa prioridade).

**Exemplo:** Uma Issue pode ter as labels `bug` (indicando um problema) e `high priority` (mostrando que precisa ser resolvida rapidamente).

### **Labels em Pull Requests**

Nos Pull Requests, as labels ajudam a **acompanhar o progresso da implementação e garantir que a alteração seja revisada corretamente**. Algumas categorias comuns incluem:

* **Tipo de mudança** – bug fix (correção de bug), enhancement (melhoria), documentation (documentação).
* **Status do PR** – in progress (em andamento), needs review (precisa de revisão), ready to merge (pronto para mesclar).
* **Impacto** – breaking change (mudança quebradora), critical change (mudança crítica).
* **Requisitos especiais** – needs tests (precisa de testes), needs more info (precisa de mais informações).

**Exemplo:** Se um PR corrige um bug, ele pode ter a label `bug fix` (indicando que resolve um problema) e `needs review` (para mostrar que necessita de avaliação antes da mesclagem).

***

Em resumo, Labels em Issues organizam o **que precisa ser feito**, enquanto labels em PRs organizam **o que está sendo feito**. Isso melhora o fluxo de trabalho, especialmente em projetos grandes.

## Boas Práticas

### **1. Defina um conjunto fixo de labels**

Evite criar variações desnecessárias. Um conjunto padronizado melhora a organização e facilita o entendimento para todos os contribuidores.

### **2. Use nomenclaturas claras e objetivas**

Escolha nomes intuitivos e curtos, evitando abreviações confusas. Exemplo: `bug` é mais compreensível do que `defeito-rep`.

### **3. Mantenha um equilíbrio na quantidade de labels por item**

Não exagere no uso de labels em uma única Issue ou PR. O excesso pode dificultar a visualização do que realmente importa.

### **4. Utilize cores de forma estratégica**

Cores ajudam a categorizar labels visualmente. Por exemplo:

* Vermelho para **prioridade alta**
* Verde para **melhorias**
* Amarelo para **mudanças críticas**

### **5. Documente o uso das labels**

Inclua uma seção sobre labels no `README.md` ou `CONTRIBUTING.md` do repositório. Isso ajuda novos contribuidores a entenderem seu propósito e uso correto.

### **6. Siga as diretrizes do projeto ao contribuir para repositórios externos**

Se estiver contribuindo para um projeto de terceiros, siga o padrão de labels já estabelecido para manter a consistência.

## Gerenciamento de Labels

O gerenciamento de labels ocorre no mesmo local e da mesma forma mencionados em [gerenciando-labels.md](../dia-8-minha-primeira-issue/labels/gerenciando-labels.md "mention"). Isso acontece porque, no GitHub, labels não são exclusivas para Issues ou Pull Requests; na verdade, elas fazem parte de um único conjunto de labels do repositório. Isso significa que qualquer label criada, na prática, pode ser aplicada tanto a Issues quanto a PRs.

Por convenção, uma equipe pode decidir utilizar determinadas labels exclusivamente para Issues ou PRs, a fim de manter uma organização mais clara. No entanto, se essa prática for adotada, é essencial documentá-la para garantir que todos os colaboradores entendam o uso correto de cada label.

## **Como Adicionar uma Label a um PR**

1. Acesse o repositório no GitHub.
2. Navegue até a aba **Pull Requests** e abra o PR desejado.
3. No menu lateral direito, clique na engrenagem (⚙️) ao lado da palavra **Labels**.
4. Selecione uma ou mais labels na lista.
5. A label será automaticamente adicionada ao PR.

**Dica:** Caso não veja a opção de adicionar labels, verifique se você tem as permissões adequadas no repositório.

## **Como Remover uma Label de um PR**

1. Acesse o repositório no GitHub.
2. Navegue até a aba **Pull Requests** e abra o PR desejado.
3. No menu lateral direito, clique na engrenagem (⚙️) ao lado da palavra **Labels**.
4. Desmarque a label que deseja remover.
5. A label será removida imediatamente do PR.

Remover labels desatualizadas pode ajudar a manter o fluxo de trabalho organizado.

## **Sua vez!**

Agora que você aprendeu como adicionar e remover labels em PRs, que tal praticar?

1. Acesse o PR que você criou anteriormente.
2. No menu lateral direito, clique na engrenagem ao lado da palavra **Labels**.\
   ![](<../.gitbook/assets/image (4) (2).png>)
3. Selecione a label **documentation (documentação)**.\
   ![](<../.gitbook/assets/image (3) (2).png>)
4. Verifique se a label foi adicionada corretamente ao seu PR.\
   ![](<../.gitbook/assets/image (5) (2).png>)

***

O uso correto de labels no GitHub melhora a organização e colaboração no projeto. Seguindo as boas práticas e mantendo um conjunto claro de labels, o time consegue trabalhar de forma mais eficiente e estruturada.
