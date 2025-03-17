# Aba Checks

A aba **Checks** em um Pull Request exibe verificações automáticas feitas no código antes que ele seja aceito no repositório. Essas verificações ajudam a garantir que o código segue certas regras, como boas práticas, funcionamento correto e compatibilidade com o projeto.

Como você viu anteriormente, os resultados dos checks também aparecem na seção **Seção de Verificação de Status** na [aba-conversation.md](aba-conversation.md "mention"). Essa seção fornece um resumo rápido do status do PR. No entanto, para obter mais detalhes sobre cada verificação, a aba **Checks** é a mais indicada.

{% hint style="warning" %}
**No seu PR, essa aba estará vazia!** Isso acontece porque o repositório em que você está contribuindo não foi configurado para rodar verificações automáticas. Caso checks fossem configurados, essa aba exibiria os resultados das verificações.

<img src="../../.gitbook/assets/104 PR_ aba checks 5.png" alt="" data-size="original">
{% endhint %}

Checks são verificações que podem incluir, por exemplo:

* **Testes automatizados**: Confere se o código funciona corretamente.
* **Análises de qualidade**: Avalia se há erros ou problemas no código.
* **Regras do projeto**: Garante que o código segue os padrões definidos pela equipe.

Esses checks são executados automaticamente sempre que um PR recebe novos commits.

<figure><img src="../../.gitbook/assets/100 PR_ aba checks.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/101 PR_ aba checks 2.png" alt=""><figcaption></figcaption></figure>

## **E se um Check Falhar?**

Se um ou mais checks falharem, você pode clicar neles tanto na aba **Checks** quanto na seção **Status Checks** da aba **Conversation** para ver mais detalhes sobre os erros e o que precisa ser corrigido. Algumas ações que você pode tomar:

* **Clicar no check** para visualizar mais informações sobre o problema.
* **Ler a mensagem de erro** para entender o que precisa ser corrigido.
* **Pedir ajuda**, se necessário, via comentários para pessoas colaboradoras que conhecem melhor a ferramenta que realizou a verificação.
* **Corrigir o código** e enviar um novo commit para que os checks sejam executados novamente.

<figure><img src="../../.gitbook/assets/102 PR_ aba checks 3.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/103 PR_ aba checks 4.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Não se preocupe com a mensagem de erro da imagem acima! Essas verificações vêm de outro repositório e estão ligadas a um contexto que você não precisa entender. O mais importante é saber onde encontrar as informações para corrigir qualquer problema, caso precise. 😊
{% endhint %}

A aba Checks ajuda a evitar que códigos com erros ou problemas sejam adicionados ao projeto, tornando o trabalho mais seguro e organizado para todas as pessoas desenvolvedoras envolvidas.

Para mais informações sobre a aba Checks, verifique a [Documentação Oficial do GitHub](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/collaborating-on-repositories-with-code-quality-features/about-status-checks).

***

Agora que você já sabe como funcionam os checks (ou por que eles não aparecem no seu PR), vamos explorar a aba **Files Changed**. Essa aba permite visualizar todas as alterações feitas no código dentro do Pull Request, facilitando a revisão e garantindo que as modificações estão corretas antes da fusão com o repositório.
