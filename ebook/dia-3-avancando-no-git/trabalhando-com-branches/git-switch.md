---
description: >-
  O comando git switch permite alternar entre branches de forma eficiente,
  facilitando a navegação no histórico do repositório.
---

# git switch

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">switch</mark> é utilizado para alternar entre branches no Git de maneira intuitiva e eficiente, facilitando o fluxo de trabalho.

## Estrutura

O formato base do comando `git switch` é:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">switch</mark> <mark style="color:blue;">\[opções]</mark> <mark style="color:green;">nome-do-branch</mark>

## Exemplos de uso

* Alternar para um branch existente
  * <mark style="color:purple;">git</mark> <mark style="color:orange;">switch</mark> <mark style="color:green;">nova-feature</mark>
  * Muda para o branch `nova-feature`.
* Criar e alternar para um novo branch:
  * <mark style="color:purple;">git</mark> <mark style="color:orange;">switch</mark> <mark style="color:blue;">-c</mark> <mark style="color:green;">nova-feature</mark>
  * Cria um novo branch chamado `nova-feature` e muda para ele automaticamente.

***

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">switch</mark> melhora a experiência ao alternar entre branches, tornando o fluxo de trabalho mais eficiente e reduzindo erros.

{% hint style="info" %}
**Uma nota sobre o git checkout**

Se você já tem alguma experiência com o Git, pode estar se perguntando sobre o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">checkout</mark>, que também é utilizado para alternar entre branches. Historicamente, o <mark style="color:purple;">git</mark> <mark style="color:orange;">checkout</mark> desempenhou um papel central no fluxo de trabalho do Git, não só permitindo a troca de branches, mas também sendo usado para restaurar arquivos e até mesmo criar novos branches.

Com o tempo, à medida que o Git evoluía e novas funcionalidades eram adicionadas, o <mark style="color:purple;">git</mark> <mark style="color:orange;">checkout</mark> passou a acumular muitas responsabilidades. Essa sobrecarga de funções gerou certa confusão, especialmente para iniciantes, pois o mesmo comando era usado para realizar operações bem diferentes, como alternar entre branches e restaurar arquivos de versões anteriores.

Para resolver essa confusão e tornar o processo de alternância de branches mais claro, o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">switch</mark> foi introduzido na versão 2.23 do Git, lançada em agosto de 2019. O objetivo principal foi separar as responsabilidades: o <mark style="color:purple;">git</mark> <mark style="color:orange;">switch</mark> foi criado para simplificar a troca de branches, enquanto a restauração de arquivos foi transferida para o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">restore</mark>. Dessa forma, o <mark style="color:purple;">git</mark> <mark style="color:orange;">switch</mark> foca exclusivamente na tarefa de alternar entre branches, oferecendo uma experiência mais intuitiva e menos propensa a erros, especialmente para novos usuários.

Se você ainda estiver usando o <mark style="color:purple;">git</mark> <mark style="color:orange;">checkout</mark> para alternar entre branches, o <mark style="color:purple;">git</mark> <mark style="color:orange;">switch</mark> é a opção mais moderna e recomendada para essa tarefa.
{% endhint %}

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`switch`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-switch/pt_BR).
{% endhint %}
