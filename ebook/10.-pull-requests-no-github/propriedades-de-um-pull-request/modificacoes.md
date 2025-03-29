# Modificações

Quando você está criando um Pull Request (PR) no GitHub, uma das seções mais importantes é a de **Modificações**. Essa seção mostra exatamente quais partes do código foram modificadas, removidas ou adicionadas. É como um "antes e depois" do seu trabalho, ajudando revisores (e você mesmo) a entenderem o impacto da sua contribuição antes de submetê-la para análise.

A seção de Mudanças funciona como um **git diff** do PR inteiro, comparando todas as alterações feitas na sua branch em relação à branch principal do repositório. Isso significa que você consegue ver, de uma só vez, todas as edições antes de criar oficialmente o PR.

A seção de Mudanças tem três funções principais:

1. **Facilitar a revisão**: Você pode verificar tudo antes de enviar o PR e revisores poderão ver rapidamente o que mudou.
2. **Garantir qualidade**: Permite identificar erros, inconsistências ou melhorias necessárias antes mesmo da revisão oficial.
3. **Histórico de alterações**: Ajuda a documentar a evolução do projeto, sendo útil para consultas futuras.

## Boas Práticas

### 1. Revise seu Próprio Código Antes de Criar o PR

Antes de submeter o PR, faça uma autoavaliação do seu código. Isso ajuda a identificar erros simples, melhorar a clareza e garantir que a proposta esteja alinhada com os objetivos do projeto.

### 2. Evite PRs Gigantes

Pull Requests muito grandes dificultam a revisão e aumentam o risco de erros passarem despercebidos. Sempre que possível, divida suas modificações em partes menores e mais gerenciáveis.

### 3. Assegure-se de que os Commits Estão Descritivos

Cada commit deve ter uma mensagem clara e objetiva, explicando o que foi alterado. Isso facilita a compreensão das mudanças e ajuda a equipe a manter um histórico organizado.

### 4. Peça feedback

Se algo não estiver claro ou precisar de mais contexto, inclua um comentário explicativo no código. Isso ajuda os revisores a entenderem suas decisões e torna a revisão mais eficiente.

### 5. Escreva Código Fácil de Entender

Um código claro e bem estruturado facilita a vida de pessoas revisoras e futuras pessoas desenvolvedoras que irão trabalhar no projeto. Algumas boas práticas incluem:

* Nomear variáveis e funções de forma descritiva.
* Evitar trechos de código muito complexos e difíceis de entender.
* Adicionar comentários explicativos quando necessário, sem excessos.

## Modos de visualização: Unified vs. Split

O GitHub permite visualizar as mudanças de duas formas diferentes:

### **1. Split (Dividido)**

As mudanças aparecem lado a lado, com o código antigo à esquerda e o novo à direita.

* Pró: Melhor para comparar cada linha detalhadamente.
* Contra: Ocupa mais espaço na tela, exigindo mais rolagem.

### **2. Unified (Unificado)**

Todas as alterações aparecem em um único bloco, onde as linhas removidas são destacadas em vermelho e as adicionadas em verde.

* Pró: Mais compacto, ideal para revisar rapidamente.
* Contra: Pode ser mais difícil comparar código lado a lado.

### Como Alternar Entre os Modos

1. Na seção de **Mudanças**, procure pelo botão de alternância entre os modos (ele exibe as opções **Split** e **Unified**).\
   ![](<../../.gitbook/assets/image (3).png>)
2. Escolha a opção desejada.
3. Para voltar ao modo anterior, basta clicar novamente na outra opção.

### Pré-visualização de Arquivos

Se o seu PR inclui arquivos Markdown (`.md`), como documentos de README ou guias, o GitHub permite pré-visualizar como ficará o documento já formatado, garantindo que links, imagens e estilos de cabeçalhos estejam corretos antes de criar o PR. Para isso,

1. Na seção de **Mudanças**, no cabeçalho do arquivo em questão, procure pelo botão de alternância entre os modos **código** (ícone `<>`) e **pré-visualização** (ícone de documento 📄).\
   ![](<../../.gitbook/assets/image (5).png>)
2. Escolha a opção do ícone do documento.
3. Para voltar à visualização de código, clique novamente no botão `<>`.

Essa funcionalidade também pode estar disponível para outros formatos, como arquivos HTML e JSON.

***

Quando um PR está bem estruturado, com código claro e organizado, mensagens de commit bem escritas e comentários explicativos quando necessário, ele reduz a quantidade de idas e voltas durante a revisão. Isso agiliza o processo e evita múltiplas interações desnecessárias, tornando a experiência mais produtiva e menos frustrante para todos os envolvidos.
