# Antes do Commit

Durante o desenvolvimento, é comum modificar arquivos e depois perceber que deseja desfazer essas mudanças antes de realizar um commit. O Git oferece diferentes maneiras de lidar com essa situação, dependendo do estado dos arquivos. Vamos aqui focar em dois possíveis cenários:

* Desfazer alterações que ainda não foram adicionados à área de staging
* Remover arquivos da área de staging

### Desfazer Alterações Não Adicionadas à Área de Staging

Se um arquivo foi editado, mas ainda não foi adicionado ao staging com <mark style="color:orange;">git</mark> <mark style="color:purple;">add</mark>, você pode simplesmente descartar as alterações com:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">restore</mark> <mark style="color:green;">nome-do-arquivo</mark>

Isso reverterá o arquivo para o último estado salvo no repositório.

### Remover Arquivos da Área de Staging

Se você já adicionou o arquivo ao staging com <mark style="color:orange;">git</mark> <mark style="color:purple;">add</mark>, mas deseja remover as mudanças antes do commit, use:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">reset</mark> <mark style="color:green;">HEAD nome-do-arquivo</mark>

Isso removerá o arquivo do staging, mas manterá as mudanças no diretório de trabalho.  O comando apenas "desfaz o git add".

Para descartar completamente as mudanças, você pode utilizar o comando explicado no item anterios:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">restore</mark> <mark style="color:green;">nome-do-arquivo</mark>

***

{% hint style="info" %}
**Uma nota sobre o git checkout**

Se você já tem alguma experiência com o Git, pode estar se perguntando sobre o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">checkout</mark>, que também é utilizado para desfazer mudanças em arquivos. Historicamente, o <mark style="color:purple;">git</mark> <mark style="color:orange;">checkout</mark> desempenhou um papel central no fluxo de trabalho do Git, não só permitindo a restauração de arquivos, mas também sendo usado para troca de branches e até mesmo criação de novos branches.

Com o tempo, à medida que o Git evoluía e novas funcionalidades eram adicionadas, o <mark style="color:purple;">git</mark> <mark style="color:orange;">checkout</mark> passou a acumular muitas responsabilidades. Essa sobrecarga de funções gerou certa confusão, especialmente para iniciantes, pois o mesmo comando era usado para realizar operações bem diferentes, como alternar entre branches e restaurar arquivos de versões anteriores.

Para resolver essa confusão e tornar o processo de alternância de branches mais claro, o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">switch</mark> foi introduzido na versão 2.23 do Git, lançada em agosto de 2019. O objetivo principal foi separar as responsabilidades: o <mark style="color:purple;">git</mark> <mark style="color:orange;">switch</mark> foi criado para simplificar a troca de branches, enquanto a restauração de arquivos foi transferida para o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">restore</mark>. Dessa forma, o <mark style="color:purple;">git</mark> <mark style="color:orange;">restora</mark> foca exclusivamente na restauração de arquivos, oferecendo uma experiência mais intuitiva e menos propensa a erros, especialmente para novas pessoas usuárias.

Se você ainda estiver usando o <mark style="color:purple;">git</mark> <mark style="color:orange;">checkout</mark> para restauração de arquivos, o <mark style="color:purple;">git</mark> <mark style="color:orange;">restore</mark> é a opção mais moderna e recomendada para essa tarefa.
{% endhint %}

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades dos comandos <mark style="color:purple;">`git`</mark><mark style="color:orange;">`restore`</mark> e <mark style="color:purple;">`git`</mark><mark style="color:orange;">`reset`</mark> , consulte as documentações oficiais:

* [documentação oficial git restore](https://git-scm.com/docs/git-restore/pt_BR)
* [documentação oficial git reset](https://git-scm.com/docs/git-reset/pt_BR)
{% endhint %}
