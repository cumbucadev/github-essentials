# Pull Requests no GitHub

**Pull Request (PR)** significa literalmente "Pedido de Puxar". No GitHub, é um pedido para que mudanças em um projeto sejam analisadas e, se aprovadas, adicionadas ao código principal.

Imagine que um grupo está escrevendo um livro em conjunto. Cada pessoa escreve um capítulo separadamente e, quando termina, pede para que o editor revise e adicione ao livro principal. No mundo do GitHub, um **Pull Request (PR)** funciona da mesma forma:

* Ele é um pedido para que alterações sejam revisadas e incorporadas ao projeto.
* Em vez de modificar diretamente o código do projeto, a pessoa sugere mudanças e pede a aprovação de outras pessoas.

## Como Era Feito Antes?

Antes da existência dos PRs, colaborar em um projeto era muito mais complicado. Imagine que duas pessoas estão escrevendo um livro juntas, mas cada uma está usando um caderno diferente. Para juntar os textos, era preciso mandar as páginas por carta ou e-mail, e a outra pessoa teria que copiar e colar manualmente no livro final. Se houvesse erros ou sugestões, o processo de revisar e modificar seria bem mais demorado.

No mundo do desenvolvimento, antes dos PRs, as mudanças no código eram enviadas por e-mail em arquivos separados. Quem administrava o projeto tinha que baixar, comparar e juntar tudo manualmente, o que aumentava o risco de erros e tornava a colaboração muito mais lenta.

Os **PRs foram criados para facilitar esse processo**, trazendo:

* **Revisão de código integrada**: Outras pessoas podem comentar e sugerir melhorias.
* **Histórico claro de alterações**: O GitHub mostra exatamente o que mudou.
* **Menos erros**: Como há revisão antes da fusão (merge), menos bugs chegam ao código principal.

## O nome "Pull Request"

O nome pode parecer estranho à primeira vista, mas faz sentido quando entendemos a lógica por trás dele.

* "Request" significa **pedido**.
* "Pull" significa **puxar**.
* Ou seja, um Pull Request é um **pedido para que as mudanças sejam puxadas para dentro do projeto principal**.

A ideia é que, ao criar um PR, a pessoa desenvolvedora está sugerindo alterações e pedindo que elas sejam incorporadas ao código principal por quem gerencia o projeto.

Outras plataformas também usam conceitos semelhantes. No [GitLab](https://about.gitlab.com/), por exemplo, chama de "Merge Request" (pedido de fusão), que enfatiza o objetivo final de unir as mudanças ao código principal. Já o [Bitbucket](https://bitbucket.org/product/) também adota o termo "Pull Request".

## Ciclo de Vida

O ciclo de um PR pode ser dividido em etapas:

1. **Criação do PR**: Uma pessoa propõe uma mudança no código.
2. **Revisão**: Outras pessoas analisam o PR, verificam o código, fazem comentários e sugerem melhorias.
3. **Ajustes**: Com base no feedback recebido, a pessoa autora do PR pode fazer alterações para corrigir erros, melhorar a solução ou esclarecer pontos levantados.
4. **Aprovação**: Quando quem revisa considera que o código está pronto, aprova o PR, indicando que ele pode ser integrado ao projeto.
5. **Merge e fechamento**: Após a aprovação, o código é mesclado ao projeto principal e o PR é encerrado.

Cada etapa garante que o código seja revisado com cuidado antes de entrar no projeto, tornando o desenvolvimento mais organizado e colaborativo.

Nas próximas seções, entraremos em mais detalhes sobre cada uma dessas etapas.&#x20;

{% hint style="warning" %}
É importante ressaltar que, por se tratar de um curso introdutório, vamos explorar os Pull Requests apenas da perspectiva de quem os cria, e não do ponto de vista de quem os revisa.
{% endhint %}
