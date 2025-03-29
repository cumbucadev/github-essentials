# Desfazendo Alterações Localmente

Ao trabalhar com Git, cometer erros ou mudar de decisão faz parte do processo. Seja um arquivo modificado por engano, uma alteração que não faz mais sentido ou um commit que precisa ser ajustado, o Git oferece diversas formas de reverter mudanças de maneira segura e eficiente. Nesta seção, vamos explorar como desfazer alterações em diferentes estágios do fluxo de trabalho, garantindo que você tenha controle sobre as modificações feitas no seu repositório **localmente**, sem afetar repositórios remotos.

O Git permite reverter mudanças em momentos distintos do desenvolvimento. Vamos nos concentrar nos seguintes tipos de reversões:

* **Alterar arquivos antes do commit**\
  Exemplo: Você editou um arquivo, mas ainda não o adicionou ao staging ou já adicionou e deseja removê-lo do staging sem perder as alterações feitas.
* **Desfazer um commit local**\
  Exemplo: Você fez um commit por engano e quer removê-lo ou voltar a um estado anterior sem perder o histórico.
* **Alterar o último commit local**\
  Exemplo: Você deseja modificar o último commit feito, seja para corrigir a mensagem, adicionar novos arquivos ou editar alterações já incluídas.

O Git oferece diferentes formas de lidar com cada uma dessas situações. Nesta seção, vamos detalhar cada abordagem, explicando como e quando utilizá-las para evitar problemas e manter o histórico do seu repositório claro e organizado.
