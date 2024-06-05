# git status

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> serve para mostrar o estado atual dos arquivos de um projeto.&#x20;

Ao executar o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark>, serão listado os arquivos modificados, preparados e não rastreados.

### **Arquivos modificados**

O comando irá mostrar quais arquivos foram modificados desde o último commit. Esses arquivos ainda não estão preparados (_staged_) para o próximo commit.&#x20;

Exemplo: Se você editou `index.html`, o <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> mostrará que `index.html` foi modificado (_`modified`_).&#x20;

<figure><img src="../../../.gitbook/assets/image (7).png" alt="git status On branch main Your branch is up to date with &#x27;origin/main&#x27;.  Changes not staged for commit:   (use &#x22;git add <file>...&#x22; to update what will be committed)   (use &#x22;git restore <file>...&#x22; to discard changes in working directory) 	modified:   index.html  no changes added to commit (use &#x22;git add&#x22; and/or &#x22;git commit -a&#x22;)"><figcaption></figcaption></figure>

### **Arquivos preparados**

O comando irá mostrar a lista dos arquivos que estão na área de preparação (_staging area_), prontos para serem incluídos no próximo commit.

Exemplo: Se você usou <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> <mark style="color:green;">index.html</mark>, o <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> mostrará que `index.html` está na área de preparação.

<figure><img src="../../../.gitbook/assets/image (8).png" alt="git status On branch main Your branch is up to date with &#x27;origin/main&#x27;.  Changes to be committed:   (use &#x22;git restore --staged <file>...&#x22; to unstage) 	modified:   index.html"><figcaption></figcaption></figure>

### **Arquivos não rastreados**

O comando irá mostrar quais arquivos do diretório de trabalho não estão sendo rastreados pelo Git. Esses são arquivos que ainda não foram adicionados ao repositório.&#x20;

Exemplo: Se você criou um novo arquivo chamado `script.js` e não usou <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark> nele, <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> mostrará que `script.js` é um arquivo não rastreado.

<figure><img src="../../../.gitbook/assets/image (11).png" alt="git status On branch main Your branch is up to date with &#x27;origin/main&#x27;.  Untracked files:   (use &#x22;git add <file>...&#x22; to include in what will be committed) 	script.js  nothing added to commit but untracked files present (use &#x22;git add&#x22; to track)"><figcaption></figcaption></figure>

#### **Estrutura**

O formato base do comando <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> é:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> <mark style="color:blue;">\[opções]</mark>

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`status`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-status/pt\_BR).
{% endhint %}

