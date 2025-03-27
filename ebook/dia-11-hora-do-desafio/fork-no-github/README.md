# Fork no GitHub

O fork surgiu como solução para um problema específico. Por isso, antes de entender o que ele é, é importante analisar o contexto que levou à sua criação. Compreender a necessidade que motivou os forks nos ajuda a entender seu propósito.

## Problema

Imagine que você quer sugerir uma nova funcionalidade para um projeto de código aberto. Com base no que aprendemos até agora, os passos seriam:

1. Ler a documentação do projeto para entender seus padrões, boas práticas e como contribuir.
2. Escolher uma issue para trabalhar.
3. Pedir para ser responsável por essa issue.
4. Depois que isso for confirmado, clonar o repositório.
5. Criar um branch específico para a nova funcionalidade.
6. Alternar para esse branch.
7. Implementar e salvar as mudanças localmente.
8. Enviar as mudanças para o repositório remoto (push).

No último passo, um erro apareceria: **"...Permissão negada"**. Isso acontece porque você não possui permissões de escrita no repositório. Mas por que não? Afinal, você só quer contribuir!

Agora, imagine que o projeto seja seu. Se qualquer pessoa pudesse modificar o código diretamente, mesmo que fosse em um branch separado, o caos se instalaria rapidamente.

Primeiro, permitir a criação livre de branches no repositório principal faria com que ele rapidamente se enchesse de branches temporários, experimentais ou abandonados. Isso dificultaria a organização do projeto e tornaria mais complexo encontrar o que realmente importa.

Além disso, mesmo que toda mudança passasse por revisão antes de ser mesclada, ainda haveria riscos. Um branch dentro do repositório principal poderia acabar sendo referenciado por engano, ou até mesmo mesclado por alguém que não percebeu que ele ainda não estava pronto. Quanto mais pessoas com acesso direto, maior a chance de erros humanos acontecerem.

Outro problema seria a segurança. Se alguém com acesso direto sofresse um ataque, por exemplo, uma pessoa mal-intencionada poderia criar ou modificar branches dentro do repositório, expondo o projeto a vulnerabilidades antes que os responsáveis percebessem o problema.

Por fim, gerenciar permissões seria inviável. Com milhares de pessoas querendo contribuir, os responsáveis pelo projeto precisariam decidir, uma a uma, quem pode ou não criar branches no repositório principal. Isso tornaria o fluxo de contribuições lento e burocrático.

## Solução

O modelo baseado em **Forks e Pull Requests** é a solução para isso. Em vez de modificar diretamente o repositório original, você cria uma cópia independente do projeto (**fork**) dentro da sua conta. Essa cópia permite que você trabalhe nas mudanças livremente, sem precisar de permissões especiais. Quando estiver satisfeito com suas alterações, pode sugeri-las para o repositório original por meio de um Pull Request. Dessa forma, quem mantém o projeto pode revisar o código antes de aceitá-lo, garantindo que as mudanças sejam seguras e organizadas.

Esse fluxo beneficia todos os envolvidos. Quem contribui pode trabalhar sem restrições, enquanto quem mantém o projeto tem controle total sobre o que entra no código-fonte. Com isso, o projeto se mantém estruturado e seguro, ao mesmo tempo que permite uma colaboração ampla e acessível.

## O Que é um Fork, Afinal?

Um **fork** é, basicamente, uma cópia independente de um repositório. Quando você faz um **fork** de um projeto no GitHub, uma réplica completa do código é criada na sua conta, mantendo o mesmo nome do repositório original.

Imagine, por exemplo, que existe um projeto chamado `projeto-incrivel`, mantido pela organização `cumbucadev`. O repositório original está disponível em `https://github.com/cumbucadev/projeto-incrivel` . Se você fizer um **fork** desse repositório, ele será copiado para a sua conta e estará acessível em `https://github.com/sua-conta/projeto-incrivel`.

O nome e o conteúdo do repositório continuam os mesmos, mas agora ele pertence a você. Isso significa que você pode modificar o código da forma que quiser, sem afetar o projeto original.

## Por Que e Quando Usar um Fork?

Os **forks** são extremamente úteis no desenvolvimento de software, especialmente em projetos de código aberto. Eles permitem que qualquer pessoa contribua sem precisar de permissões diretas no repositório original. Dessa forma, você pode testar mudanças e sugerir melhorias sem comprometer o código principal.

Além de facilitar contribuições, **forks** também são usados para explorar e modificar projetos livremente. Como são cópias independentes, você pode testar ideias sem se preocupar com impactos no repositório original. Muitas pessoas utilizam **forks** para criar suas próprias versões de um projeto, personalizando-o conforme suas necessidades ou dando continuidade ao desenvolvimento de um código desatualizado.

Outro benefício importante é a possibilidade de aprendizado. Se você quer entender melhor como um determinado software funciona, pode criar um fork e estudar o código sem medo de causar problemas. Isso torna os **forks** uma excelente ferramenta tanto para quem quer contribuir para projetos open source quanto para quem deseja estudar códigos já existentes.

Porém, nem sempre um **fork** é necessário. Se você já tem permissões no repositório original, por exemplo, pode criar um branch diretamente nele, sem precisar de uma cópia separada. O mesmo vale para casos em que você quer apenas testar o código localmente sem modificá-lo ou contribuir de volta — nesse cenário, basta clonar o repositório.

{% hint style="success" %}
É importante destacar que **"fork" não é um conceito do Git, mas sim do GitHub e de outras plataformas de hospedagem de código**. O Git, por si só, não possui um comando específico chamado "fork".

Se você estivesse apenas usando o Git sem o GitHub, para conseguir algo semelhante a um fork, precisaria seguir alguns passos manualmente: primeiro, clonar o repositório (<mark style="color:purple;">`git`</mark><mark style="color:orange;">`clone`</mark>), depois criar um novo repositório em outro lugar, adicionar esse novo repositório como um remoto (<mark style="color:purple;">`git`</mark><mark style="color:orange;">`remote add`</mark>) e, então, gerenciar suas alterações a partir daí.

O GitHub facilita esse processo tornando o **fork** um recurso nativo da plataforma. Com apenas um clique, você cria automaticamente uma cópia independente de um repositório dentro da sua própria conta, sem precisar configurar nada manualmente. Isso torna a colaboração em projetos open source muito mais simples e acessível para qualquer pessoa.
{% endhint %}

***

Na próxima seção, vamos entender como criar um **fork** no GitHub e como utilizá-lo no nosso fluxo de trabalho.
