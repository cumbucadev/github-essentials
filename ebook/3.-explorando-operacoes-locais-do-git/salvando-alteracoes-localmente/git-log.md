# git log

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> serve para mostrar o histórico de commits de um repositório. Ele exibe uma lista de commits no histórico atual do branch, incluindo detalhes como o autor, a data, a mensagem do commit e o identificador único (hash) do commit. É comumente usado para navegar pelo histórico de commits do projeto e entender as mudanças ao longo do tempo.

<figure><img src="../../.gitbook/assets/Commit (1).png" alt=""><figcaption><p>Nesta imagem temos 2 commits diferentes, e cada um possui seu próprio ID, informações de autoria, data/hora e uma breve descrição. Eles se comportam como um "print screen" que capta todas essas informações no momento em que o Desenvolvedor "<em>commita"</em> essas atualizações. </p></figcaption></figure>

## Estrutura

O formato base do comando <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> é:

> <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> <mark style="color:blue;">\[opções]</mark>

## **Exemplos de uso** <a href="#exemplos-de-uso" id="exemplos-de-uso"></a>

* Exibir o histórico completo de commits:
  * <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark>
  * Lista todos os commits do repositório com detalhes como autor, data e mensagem do commit.

```sh
git log
▶ commit a1b2c3d4e5f67890123456789abcdef12345678 (HEAD -> main)
Author: Nome do Autor <email@exemplo.com>
Date:   Mon Feb 19 10:00:00 2024 -0300

    Mensagem do segundo commit, o mais recente

commit f6e5d4c3b2a190876543210fedcba9876543210
Author: Outro Autor <outro@exemplo.com>
Date:   Sun Feb 18 15:30:00 2024 -0300

    Mensagem do primeiro commit

```

* Exibir o histórico de commits de forma resumida::
  * <mark style="color:purple;">git</mark> <mark style="color:orange;">log</mark> <mark style="color:blue;">--oneline</mark>
  * Mostra uma versão compacta do histórico, exibindo apenas o hash abreviado e a mensagem do commit.

```sh
git log --oneline
▶ a1b2c3d Mensagem do segundo commit, o mais recente
f6e5d4c Mensagem do primeiro commit
```

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`log`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-log/pt_BR).
{% endhint %}
