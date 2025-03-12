# Descrição

A descrição do Pull Request (PR) é um espaço para explicar em detalhes as mudanças feitas no código. Assim como a descrição de uma Issue, ela ajuda a equipe a entender o contexto da alteração, os problemas resolvidos e os impactos que podem ocorrer. Uma boa descrição facilita a revisão, melhora a colaboração e documenta as mudanças para o futuro.

## **Boas Práticas**

### **1. Descreva o Problema e a Solução**

Explique qual era o problema e como foi resolvido. Dê contexto suficiente para que quem revisa não precise adivinhar o que motivou a mudança.

### **2. Objetividade, mas com Completude**

Dê informações suficientes para a revisão sem entrar em detalhes desnecessários. Seja claro sobre o que mudou e por quê.

### **3. Explique a Motivação da Mudança**

Além de descrever o que foi feito, é importante explicar _por que_ a alteração foi necessária. Isso ajuda a equipe a entender o contexto e a tomar decisões melhores no futuro. Se a mudança resolve um problema específico ou melhora um fluxo, deixe isso claro na descrição.

### **4. Adicione Capturas de Telas ou GIFs**

Se a alteração impacta a interface gráfica ou muda fluxos visuais, adicionar imagens ou GIFs pode facilitar a revisão.

### **5. Explique Decisões Importantes**

Se alguma escolha no código não estiver óbvia, comente na descrição para ajudar quem está revisando.

### **6. Siga o Padrão do Repositório**

Assim como para o título do PR, é essencial seguir as diretrizes do repositório para garantir que sua contribuição seja bem recebida. Isso facilita a revisão e mantém a consistência do projeto. Antes de abrir um PR:

* Verifique se há um arquivo `CONTRIBUTING.md`, que pode conter instruções específicas.
* Observe PRs já abertos para entender como as descrições são estruturadas.
* Caso exista um template de PR, preencha todas as informações solicitadas e siga o formato indicado.

Manter um padrão no projeto agiliza a revisão, melhora a colaboração e torna o histórico de mudanças mais organizado.

### **7. Use Palavras-chave para Fechar Issues**

Ao criar um PR que resolve uma Issue, você pode usar palavras-chave para referenciá-la automaticamente. O GitHub fechará automaticamente a Issue quando o PR for mesclado. As palavras-chave disponíveis são:

* `Fixes #123` (Corrige a Issue #123)
* `Closes #456` (Encerra a Issue #456)
* `Resolves #789` (Resolve a Issue #789)

Qualquer uma dessas palavras pode ser utilizada para referenciar e fechar a Issue correspondente. Mais detalhes podem ser encontrados na [documentação oficial do GitHub](https://docs.github.com/pt/get-started/writing-on-github/working-with-advanced-formatting/using-keywords-in-issues-and-pull-requests).

### **8. Utilize Markdown**

O Markdown facilita a visualização e organização das informações na descrição do PR, tornando o conteúdo mais legível. Assim como nas Issues, a descrição do PR aceita Markdown para formatação, e é possível visualizar o preview antes de enviar.

### **Exemplos de Boas Descrições ✅**

#### **Exemplo 1: Correção de bug**

```markdown
# Corrige erro de cálculo no carrinho de compras

**Problema**: O cálculo de desconto estava incorreto para pedidos acima de R$ 100,00.
**Solução**: Ajustado o cálculo da função calcular_desconto().
**Testes**: Adicionados novos testes unitários para garantir a precisão do cálculo.
**Issue relacionada**: Fixes #123.
```

#### **Exemplo 2: Nova funcionalidade**

```markdown
# Permitir exclusão de pedidos na página de pedidos

## O que foi feito?
- Adicionado um botão "Excluir" na página de pedidos.
- Implementado um alerta de confirmação para evitar exclusões acidentais.
- Atualizada a documentação para incluir essa nova funcionalidade.

## Motivação
Antes, não havia uma forma direta de excluir pedidos, o que exigia 
ações manuais no banco de dados. Agora, essa operação pode ser feita 
com segurança e de forma intuitiva.

## Antes
[gif mostrando que não havia opção para excluir pedidos]

## Depois
[gif mostrando o novo botão e o alerta de confirmação]

Closes #123
```

### **Contra-exemplos ❌**

* Deixar a descrição vazia.
* "Correção de bug" → Qual bug? Onde? Como foi resolvido?
* "Melhorias no sistema" → Muito genérico.
* "Novo endpoint" → Qual endpoint? Para quê?

***

Uma descrição bem feita melhora a colaboração e torna o histórico do projeto mais organizado. Seguir boas práticas faz com que PRs sejam revisados mais rapidamente e evita retrabalho. Sempre siga os padrões do repositório e aproveite os recursos do Markdown para deixar suas descrições mais claras!
