# Boas Práticas

A forma como você interage durante a revisão de código pode impactar diretamente a qualidade do feedback e a experiência de todos os envolvidos. Pode parecer óbvio, mas pequenas atitudes fazem uma grande diferença! Ao adotar essas práticas, você facilita o processo, melhora a colaboração e evita retrabalho. Por outro lado, quando elas não são seguidas, as revisões podem se tornar demoradas, confusas e frustrantes para todos.

## Revise o seu código antes de pedir revisão

Antes de abrir um PR, faça uma análise cuidadosa do seu código. Tente identificar possíveis melhorias ou erros que possam ser corrigidos antes de envolver outra pessoa. Isso demonstra atenção aos detalhes e respeito pelo tempo da equipe.

## Garanta que todos os checks estão passando antes de pedir revisão

Se o projeto possui verificações automáticas, certifique-se de que tudo está passando antes de solicitar uma revisão. Isso evita feedbacks desnecessários sobre problemas que poderiam ser resolvidos previamente.

Caso encontre dificuldades, peça ajuda diretamente nos comentários do PR antes de seguir para a revisão formal.

## **Responda aos comentários com clareza**

Interagir de forma clara e objetiva nos comentários da revisão melhora a comunicação e reduz o tempo necessário para finalizar um PR. Para cada sugestão recebida:

* Se concordar, implemente a mudança e marque a conversa como resolvida.
* Se discordar, explique seu ponto de vista educadamente.

**Exemplos:** ❌ "Feito." ✅ "Boa sugestão! Apliquei a mudança na última versão. Obrigado!"

❌ "Prefiro assim." ✅ "Acredito que manter a estrutura atual facilita a leitura, pois segue o padrão do projeto. O que acha?"

## **Seja receptivo ao feedback**

Comentários em revisões não são críticas pessoais. Encare-os como oportunidades de aprendizado e aprimoramento. Se não concordar com uma sugestão, argumente de forma respeitosa. Se tiver dúvidas, pergunte para entender melhor.

## Pergunte quando não entender

Se algum comentário parecer vago ou ambíguo, peça mais detalhes. Isso evita retrabalho e melhora a comunicação entre quem escreve e quem revisa o código.

Além disso, se um comentário mencionar algo que você não conhece ou não tem experiência técnica, aproveite para perguntar e aprender mais sobre o assunto.

**Exemplos:** ❌ "Não entendi." ✅ "Você pode explicar melhor o que quis dizer sobre a estrutura desse bloco? Há algo específico que acha que pode ser melhorado?"

Se precisar de ajuda técnica, seja específico sobre sua dúvida.

❌ "Como faço isso?" ✅ "Poderia me explicar como essa função interage com o restante do código? Não estou certo de como implementar essa lógica."

## Não tire conclusões precipitadas

Nem todo comentário mais direto ou objetivo é uma crítica negativa. Se algo parecer ríspido, tente interpretar da melhor forma possível antes de reagir. Se necessário, peça esclarecimentos para evitar mal-entendidos.

**Exemplo:** ❌ "Isso não faz sentido!" ✅ "Poderia detalhar melhor essa sugestão? Quero entender seu ponto de vista para ver como podemos melhorar o código."

## Peça opinião de mais pessoas

Se houver um impasse ou discordância significativa com uma sugestão, pedir a opinião de outras pessoas do time pode ser útil. Isso ajuda a chegar a um consenso mais sólido.

***

Seguindo essas práticas, o processo de revisão se torna mais eficiente, contribuindo para um código de melhor qualidade e um ambiente de colaboração mais saudável. Além de otimizar o tempo da equipe, boas práticas ajudam a evitar desgastes desnecessários e possíveis atritos, tornando a revisão um momento produtivo e construtivo para todas as pessoas envolvidas.

Na próxima seção, analisaremos um exemplo prático de revisão, utilizando o PR que já temos aberto no repositório **hello-world**.
