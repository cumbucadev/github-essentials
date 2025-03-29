# Criando uma Issue no GitHub

No GitHub, as issues são fundamentais para gerenciar tarefas, bugs, melhorias e discussões em projetos. Criar uma issue bem estruturada facilita a organização, comunicação e resolução de problemas de forma eficiente. Vamos explorar como criar uma issue do início ao fim, com exemplos práticos e boas práticas.

Existem diversas formas de criar uma issue. Vamos focar em criar uma a partir da aba **Issues** de um repositório. [Essas são as instruções da documentação oficial](https://docs.github.com/pt/issues/tracking-your-work-with-issues/using-issues/creating-an-issue#creating-an-issue-from-a-repository), mas não se preocupe, logo abaixo vamos mostrar o passo a passo com um exemplo prático. Antes de começar, é importante conhecer os dois principais campos de uma issue: **Título** e **Descrição**.

## Título da Issue

O título é um resumo da issue. Ele deve ser curto, descritivo e direto ao ponto. Um bom título ajuda a identificar rapidamente do que se trata a tarefa, facilita a organização e a busca dentro do repositório, tornando a comunicação mais clara para quem for resolver o problema. Além disso, um título bem escrito aumenta as chances de a issue ser resolvida rapidamente, pois torna mais fácil para quem está buscando algo para contribuir entender do que se trata a questão.

**Dica:**

* **O Markdown é aceito:** Use formatação como negrito, itálico e outros para destacar informações importantes.

### **Boas práticas para o título**

#### **Seja claro e objetivo**

O título deve comunicar o problema ou a tarefa de forma simples e direta, sem a necessidade de ler a descrição.

Exemplo: "Corrigir erro ao carregar imagem no perfil"

#### **Evite títulos vagos ou genéricos**

Títulos que não fornecem informações suficientes podem dificultar a busca no repositório ou confundir quem vai ler.

Exemplo de título ruim: "Bug no site"

#### **Use palavras-chave relevantes**

Incluir palavras-chave relacionadas à tarefa ajuda a organizar melhor o repositório e torna mais fácil encontrar as issues.

Exemplo: "Adicionar botão de logout na página inicial"

#### **Inclua o tipo de tarefa, se necessário**

Se a tarefa for muito específica, como um bug ou uma melhoria, pode ser útil incluir isso no título.

Exemplo: "Melhoria na interface do usuário no formulário de login"

#### **Mantenha o título curto, mas informativo**

O título não precisa ser longo, mas deve ser informativo o suficiente para que alguém saiba do que se trata a tarefa sem precisar abrir a descrição.

Exemplo: "Ajustar responsividade da página de contato"

## Descrição da Issue

A descrição da issue fornece mais detalhes sobre a tarefa a ser realizada. Esse campo deve explicar o que precisa ser feito e, se possível, o motivo. Uma boa descrição ajuda a entender o problema ou a sugestão de melhoria, mantém um histórico claro da discussão e do progresso da tarefa.

### **Boas práticas para a descrição**

#### **Seja claro e específico sobre o que precisa ser feito**

Explique a tarefa de forma detalhada, mas sem ser excessivamente longo. Quanto mais clara a descrição, menos espaço para confusão haverá.

Exemplo: "A página de login não está exibindo corretamente em dispositivos móveis. Ajustar os elementos da página para que fiquem alinhados e adaptáveis em telas menores."

#### **Forneça contexto**

Se o problema for uma falha ou bug, explique em que situações ele ocorre e quais são as etapas para reproduzi-lo. Para melhorias ou novas funcionalidades, forneça o que se espera alcançar.

Exemplo: "O erro acontece quando o usuário tenta carregar uma imagem de perfil com mais de 1MB. A página quebra e exibe um erro 500. Para reproduzir, siga estes passos: 1) Vá até a página de perfil, 2) Tente carregar uma imagem maior que 1MB."

#### **Se possível, forneça um exemplo ou sugestão**

Mostrar o que você espera como resultado ajuda quem vai resolver a issue a ter uma ideia mais clara de como proceder.

Exemplo: "Gostaria de sugerir a adição de um botão de 'Limpar filtros' na página de pesquisa. Esse botão pode ser colocado ao lado do campo de pesquisa e deve limpar todos os filtros aplicados na busca."

#### **Inclua capturas de tela, GIFs ou links (se aplicável)**

Se for um erro visual ou comportamento inesperado, adicionar uma imagem ou um vídeo ajuda a comunicar o problema de forma mais eficiente.

Exemplo: "Veja a captura de tela abaixo onde a imagem da banner está sobrepondo o texto no topo da página."

#### **Evite descrições vagas ou muito curtas**

Uma descrição muito genérica ou com poucas informações pode gerar confusão. Evite usar frases como "A página está quebrando" sem explicar em que situação isso acontece.

Exemplo ruim: "Corrigir erro no login"

#### **Use markdown para melhorar a legibilidade**

Você pode utilizar _listas_, **negrito**, _itálico_ e até mesmo **códigos** ou links para tornar a descrição mais clara e fácil de ler.

Exemplo:

```markdown
**Erro:** A página de login não está respondendo após inserir credenciais válidas.

**Passos para reproduzir:**
1. Vá até a página de login.
2. Insira um nome de usuário e senha válidos.
3. Clique no botão de login.

**Resultado esperado:** O usuário deve ser redirecionado para a página inicial.
```

**Linguagem aceita:** A descrição também pode ser escrita em qualquer linguagem suportada pelo GitHub, com a possibilidade de usar Markdown para formatação. Além disso, imagens e links podem ser inseridos usando a sintaxe de Markdown.

## Criando Sua Primeira Issue

É hora de criar a sua primeira issue e ela será criada no repositório hello-world que você criou anteriormente. Neste momento, você irá criar uma tarefa para si mesmo resolver. Isso ajuda a praticar o uso de issues antes de colaborar em outros repositórios.

### **Objetivo da Issue**

A tarefa será adicionar uma imagem ou GIF ao final do README.md. Essa imagem/GIF deve ser uma saudação para quem visitar o repositório, tornando-o mais acolhedor e amigável.

### **Criando uma Nova Issue**

#### **1. Acesse a aba Issues**&#x20;

No repositório hello-world, clique na aba **Issues**. Em seguida, clique no botão **New issue** para criar uma nova.

#### **2. Preenchendo o título**

Preencha o campo título com: "Adicionar imagem de saudação ao README.md".

<figure><img src="../.gitbook/assets/image (77).png" alt=""><figcaption><p>Título da issue</p></figcaption></figure>

#### **3. Preenchendo a descrição**

Preencha o campo descrição com:

````
# Descrição da Issue

Para tornar o arquivo `README.md` mais acolhedor e convidativo para os visitantes do repositório, podemos adicionar uma imagem ou GIF de saudação ao final do arquivo.

## Objetivo
Adicionar uma imagem ou GIF animado ao final do arquivo `README.md` para criar uma experiência mais amigável para visitantes.

## Caminho do arquivo:
O arquivo a ser alterado é o `README.md`, localizado na raiz do repositório.

## Sugestões
- Um GIF animado de uma mensagem de "Boas-vindas!" 🎉
- Um GIF ou uma imagem divertida de uma pessoa acenando - representando uma saudação de boas-vinda

## Instruções para a modificação:
Adicione a imagem ou GIF após o conteúdo atual. 
Faça isso utilizando a sintaxe de Markdown para imagens:

- Para adicionar uma imagem: ![Texto alternativo](caminho-da-imagem)
- Para adicionar um GIF: ![Texto alternativo](caminho-do-gif)

Para mais informações sobre como usar a sintaxe de Markdown para imagens, consulte a [documentação oficial do Markdown](https://www.markdownguide.org/basic-syntax/#images).

## Exemplo:
```markdown
![Boas vindas ao meu repositório!](https://link-para-o-gif-ou-imagem)
```

## O que esperamos:
O arquivo `README.md` terá um toque mais acolhedor com uma saudação visual que pode engajar novos contribuidores ou visitantes do repositório.
````

<figure><img src="../.gitbook/assets/41- Descrição Issue.png" alt=""><figcaption><p>Descrição da issue</p></figcaption></figure>

#### **4. Salvar a issue**

Clique no botão "Create" para salvar a issue.

<figure><img src="../.gitbook/assets/42 Create Issue.png" alt=""><figcaption><p>Criar issue</p></figcaption></figure>

<figure><img src="../.gitbook/assets/43- Issue criada (1).png" alt=""><figcaption><p>Issue "Adicionar imagem de saudação ao README.md"</p></figcaption></figure>

## Permissões: Quem Pode Criar Issues?

No GitHub, nem todas as pessoas podem criar issues em qualquer repositório. Veja as regras gerais:

* **Repositórios próprios:** Você pode criar issues à vontade.
* **Repositórios públicos de outras pessoas/organizações:** Depende das permissões configuradas. Alguns projetos permitem que qualquer pessoa crie issues, enquanto outros limitam essa opção a contribuidores aprovados.
* **Repositórios privados:** Apenas pessoas com acesso ao repositório podem criar issues.

Ao criar um repositório, o padrão é que os contribuidores podem criar issues, a menos que a configuração seja alterada pelo administrador do repositório.

Se quiser abrir uma issue em um repositório de outra pessoa, verifique antes se isso é permitido e siga as diretrizes do projeto (muitas vezes descritas em um arquivo **CONTRIBUTING.md**).

## Criando Issues em Repositórios de Outras Pessoas/Organizações

Quando você abre uma issue em um repositório que não é seu, é essencial seguir algumas regras:

* **Leia a documentação:** Muitos repositórios têm um **CONTRIBUTING.md** com diretrizes para contribuir.
* **Pesquise antes:** Verifique se a issue já foi relatada para evitar duplicidade.
* **Siga o formato:** Alguns projetos têm templates pré-definidos. Use-os corretamente.
* **Respeite a comunidade:** Seja educado e objetivo. Evite mensagens exigindo soluções urgentes.
* **Colabore:** Se puder, ajude na discussão e contribua com soluções.

Pense que abrir uma issue em um repositório de terceiros é como entrar na casa de alguém: antes de agir, veja como as coisas são feitas por lá e respeite as regras.

***

Nas próximas seções, vamos aprofundar em outros aspectos das issues, como a categorização, a exibição delas no GitHub e o processo de atribuição de uma issue.
