# Interagindo com o Repositório Central

Até agora, explicamos como fazer mudanças no repositório local, na sua própria máquina. Aprendemos a:

* Inicializar um novo repositório com <mark style="color:purple;">git</mark> <mark style="color:orange;">init</mark>.
* Obter e definir configurações de pessoa usuária e repositório com <mark style="color:purple;">git</mark> <mark style="color:orange;">config</mark>.
* Adicionar arquivos ao repositório com <mark style="color:purple;">git</mark> <mark style="color:orange;">add</mark>.
* Verificar o estado do repositório com <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark>.
* Salvar mudanças com <mark style="color:purple;">git</mark> <mark style="color:orange;">commit</mark>.
* Revisar o histórico de commits com <mark style="color:purple;">git</mark> <mark style="color:orange;">log.</mark>
* Ver as diferenças entre alterações com <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark>.
* Criar e listar branches com <mark style="color:purple;">git</mark> <mark style="color:orange;">branch</mark>.
* Trocar de branch com <mark style="color:purple;">git</mark> <mark style="color:orange;">switch</mark>.
* Mesclar branches com <mark style="color:purple;">git</mark> <mark style="color:orange;">merge</mark>.
* Restaurar arquivos ao último commit com <mark style="color:purple;">git</mark> <mark style="color:orange;">restore</mark>.
* Resetar o estado do repositório para um commit anterior com <mark style="color:purple;">git</mark> <mark style="color:orange;">reset</mark>.
* Reverter um commit com <mark style="color:purple;">git</mark> <mark style="color:orange;">revert</mark>.
* Definir arquivos ou pastas para serem ignorados com .gitignore.
* Remover arquivos do repositório com <mark style="color:purple;">git</mark> <mark style="color:orange;">rm</mark>.

Essas operações são fundamentais para controlar a versão de seus arquivos localmente, mas elas só afetam o repositório no seu próprio computador.

Nesta seção, vamos explorar como interagir com um repositório remoto central **já existente**. Isso envolve pegar (pull/fetch) e enviar (push) mudanças entre seu repositório local e o repositório central hospedado em serviços como GitHub, GitLab ou Bitbucket.

**O que Vamos Aprender:**

1. **Clonar um Repositório Remoto:**
   * Como criar uma cópia do repositório remoto em sua máquina local.
2. **Puxar Mudanças (Pull):**
   * Como atualizar seu repositório local com as últimas mudanças do repositório central.
3. **Buscar Mudanças (Fetch):**
   * Como buscar as mudanças do repositório remoto sem mesclá-las automaticamente.
4. **Enviar Mudanças (Push):**
   * Como compartilhar suas mudanças locais com o repositório central.

Essas operações permitem que você colabore com outras pessoas desenvolvedores de forma eficiente, mantendo seu repositório local sincronizado com o repositório central e garantindo que suas contribuições sejam incorporadas ao projeto principal.
