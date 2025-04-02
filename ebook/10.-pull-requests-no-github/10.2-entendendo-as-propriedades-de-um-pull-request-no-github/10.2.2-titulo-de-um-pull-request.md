# Título

O título do Pull Request (PR) é um resumo curto que explica o que está sendo mudado no código. Ele aparece no topo do PR e ajuda quem revisa a entender rapidamente qual é a proposta da alteração. Um bom título facilita a comunicação e evita confusões, especialmente em projetos com várias pessoas colaborando.

## **Boas Práticas**

### **1. Clareza e Objetividade**

O título deve indicar o que está sendo alterado sem ser muito genérico.

### **2. Evite Títulos Vagos**

Não use algo genérico como _"Correção"_ ou _"Ajustes"_.

### **3. Mantenha Curto, mas Informativo**

Para ajudar a ter uma noção, algo entre 40 e 70 caracteres funciona bem.

### **4. Siga o Padrão**

Ao contribuir para um repositório de outra pessoa ou organização, é importante seguir as regras do projeto para que sua contribuição seja bem recebida. Muitos repositórios possuem um arquivo chamado `CONTRIBUTING.md`, onde estão descritas boas práticas e regras para contribuições, incluindo orientações sobre como nomear PRs. Antes de abrir um PR, vale a pena conferir esse arquivo e também olhar PRs já abertos para entender o padrão seguido no projeto. Se houver um modelo específico para o título, como `[BugFix] Corrige erro X`, use esse formato para manter a consistência.

Além disso, alguns repositórios configuram um **template de PR**, que aparece automaticamente no campo de descrição ao criar um novo PR. Esse template pode conter instruções sobre o que incluir na descrição, checklists para garantir que tudo foi testado e até exemplos de formatos para o título. Sempre preencha todas as informações solicitadas no template e siga o formato indicado, pois isso ajuda a manter um padrão no projeto e facilita a revisão do seu PR.&#x20;

### **Exemplo de Bons Títulos** ✅

* "Adiciona validação de e-mail no formulário de cadastro"
* "Corrige erro de cálculo no carrinho de compras (#1234)"
* "Melhora performance do endpoint `/api/orders` ao otimizar queries"

### **Contra-exemplos: Exemplo de Títulos Ruins** ❌

* &#x20;_"Ajustes"_ → Muito vago, não diz nada sobre o que foi alterado.
* _"Melhorias no código"_ → Melhorias em que parte? O que foi feito?
* _"Arrumando bug"_ → Qual bug? Onde?
* _"funcionalidade nova adicionada"_ → Qual _funcionalidade_?

***

Seguir boas práticas ao escrever títulos de PRs faz toda a diferença no dia a dia do desenvolvimento. Com um título claro e direto, a revisão acontece de forma mais rápida e eficiente, já que quem está analisando o código entende de imediato o que está sendo alterado. Isso também facilita a colaboração, principalmente em projetos com muitas pessoas contribuindo ao mesmo tempo. Além disso, manter um padrão organizado ajuda a manter o histórico do projeto mais compreensível, evitando confusões e retrabalho no futuro.
