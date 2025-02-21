# git rm

Às vezes, um arquivo já está sendo rastreado pelo Git, mas você percebe que ele não deveria estar no repositório. Isso pode acontecer quando você esquece de adicioná-lo ao `.gitignore` ou quando ele deixa de ser relevante. Nesses casos, você pode usar o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">rm</mark> para removê-lo do repositório e garantir que ele não seja rastreado no futuro.

## **Como Funciona**

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">rm</mark> remove arquivos do controle de versão do Git. Por padrão, ele exclui o arquivo tanto do repositório quanto do seu computador (diretório local). No entanto, é possível preservar o arquivo no diretório usando opções específicas.

## Estrutra

> <mark style="color:purple;">git</mark> <mark style="color:orange;">rm</mark> <mark style="color:blue;">\[opções]</mark> <mark style="color:green;">arquivo</mark>

Esse comando remove o arquivo tanto do repositório quanto do seu diretório local.

## Casos de Uso

### 1. Remover um Arquivo do Repositório e do Diretório

Se você deseja excluir um arquivo do repositório e apagá-lo do seu computador, use:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">rm</mark> <mark style="color:green;">exemplo.txt</mark>

### 2. Remover um Arquivo Apenas do Controle de Versão (Sem Excluir Localmente)

Se o arquivo já está no repositório, mas você quer que o Git pare de rastreá-lo sem apagá-lo do disco, use a opção <mark style="color:blue;">--cached</mark>:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">rm</mark> <mark style="color:blue;">--cached</mark> <mark style="color:green;">exemplo.txt</mark>

Após isso, adicione o arquivo ao `.gitignore` para evitar que ele seja rastreado novamente.

### 3. Remover Diretórios Inteiros

Se precisar remover um diretório inteiro e todos os seus arquivos, use a opção `-r`:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">rm</mark> <mark style="color:green;">pasta/</mark>

O diretório e todos os arquivos dentro dele serão apagados do seu computador. Use <mark style="color:blue;">--cached</mark> para manter os arquivos no diretório local.

## Confirmando a Remoção

Após usar <mark style="color:purple;">git</mark> <mark style="color:orange;">rm</mark>, o arquivo será removido do rastreamento, mas a alteração precisa ser confirmada em um commit.

1. **Verifique o status dos arquivos:**

```sh
git status
```

2. **Remova o arquivo do repositório:**

```sh
git rm --cached temp.log
```

3. **Confirme a remoção:**

```sh
git commit -m "Remover temp.log do repositório"
```

### Considerações Finais

* **Desfazendo a Remoção:** Se você removeu um arquivo por engano e ainda não fez o commit, pode restaurá-lo com:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">restore</mark> <mark style="color:green;">arquivo</mark>

* **Removendo um Arquivo do Histórico do Repositório:** Para remover um arquivo de todo o histórico do Git (e não apenas da versão atual), é necessário usar comandos avançados como <mark style="color:purple;">git</mark> <mark style="color:orange;">filter-branch</mark> ou <mark style="color:purple;">git</mark> <mark style="color:orange;">rebase</mark>, que não serão abordados aqui.

**Dicas Importantes:**

* Sempre use <mark style="color:purple;">git</mark> <mark style="color:orange;">status</mark> antes de remover arquivos para evitar exclusões acidentais.
* Faça backup (cópia) de arquivos importantes antes de removê-los do Git.

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`rm`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-rm/pt_BR).
{% endhint %}
