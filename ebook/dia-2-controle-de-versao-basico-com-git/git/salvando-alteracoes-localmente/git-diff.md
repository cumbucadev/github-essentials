# git diff

O comando <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark> é usado para mostrar as diferenças entre o estado atual do seu repositório e o último commit. Ele é útil para visualizar as alterações feitas nos arquivos antes de criar um novo commit.

No terminal, o output do <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark> apresentará as diferenças de forma clara. Cada alteração será mostrada com um prefixo indicando se é uma adição `+`, uma remoção `-`, ou uma modificação `*`.

### Estrutura

Esta é a estrutura base do comando <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark> que iremos utilizar neste momento

> <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark> <mark style="color:green;">\[arquivo]</mark>

Em que:&#x20;

* <mark style="color:purple;">**git**</mark>** **<mark style="color:orange;">**diff**</mark>: Este é o comando principal que invoca a ferramenta de diferenciação do Git.
* <mark style="color:green;">**\[arquivo]**</mark>** (opcional)**: Este é um argumento opcional que especifica o arquivo específico para o qual você deseja ver as diferenças. Se nenhum arquivo for especificado, o <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark> mostrará as diferenças de todos os arquivos modificados em relação ao último commit.

### Exemplo de Uso

#### **Exemplo 1:** <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark> <mark style="color:green;">arquivo</mark>

Suponha que o arquivo `index.html` originalmente tinha o seguinte conteúdo:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Meu Site</title>
</head>
<body>
    <!-- Conteúdo do site -->
</body>
</html>
```

Agora, você fez algumas alterações nesse arquivo. Por exemplo, você modificou o título do site. O arquivo `index.html` modificado ficou assim:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Meu Novo Site</title>
</head>
<body>
    <!-- Conteúdo do site -->
</body>
</html>
```

Ao executar o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark> <mark style="color:green;">index.html</mark>, o output no terminal mostrará as diferenças entre o estado atual do arquivo `index.html` e o último commit. Ele indicará que o título do site foi alterado de "Meu Site" para "Meu Novo Site", destacando essa mudança no código:

```sh
diff --git a/index.html b/index.html
index abcdef1..1234567 100644
--- a/index.html
+++ b/index.html
@@ -1,5 +1,5 @@
 <!DOCTYPE html>
 <html>
 <head>
-    <title>Meu Site</title>
+    <title>Meu Novo Site</title>
 </head>
 <body>
```

Em que:

1.  **Diff do arquivo index.html:**

    ```sh
    diff --git a/index.html b/index.html
    ```

    Esta linha indica que está sendo mostrada a diferença entre dois arquivos: `a/index.html` (o arquivo original) e `b/index.html` (o arquivo modificado).
2.  **Cabeçalho de Mudança::**

    ```sh
    index abcdef1..1234567 100644
    --- a/index.html
    +++ b/index.html
    ```

    Este cabeçalho técnico fornece informações detalhadas sobre as mudanças nos arquivos e pode ser ignorado por enquanto, focando apenas nas alterações visíveis no conteúdo.
3.  **Linha de Mudança:**

    ```sh
    @@ -1,5 +1,5 @@
    ```

    Esta linha mostra a linha inicial e o número de linhas afetadas pela mudança em cada arquivo. No exemplo, `-1,5` indica que a mudança começa na linha 1 do arquivo original (`a/index.html`) e afeta 5 linhas. `+1,5` indica que a mudança começa na linha 1 do arquivo modificado (`b/index.html`) e também afeta 5 linhas.
4.  **Alterações Específicas:**

    ```sh
    -    <title>Meu Site</title>
    +    <title>Meu Novo Site</title>
    ```

    Essas linhas mostram as alterações específicas que ocorreram em cada versão do arquivo. \
    A linha original `<title>Meu Site</title>` foi removida (indicada pelo sinal `-`).\
    Em seu lugar, foi adicionada a linha `<title>Meu Novo Site</title>` (indicada pelo sinal `+`).

#### Exemplo 2: <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark>

Para visualizar as diferenças em todos os arquivos modificados, basta utilizar o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark> sem nenhum argumento. Dessa forma, o Git apresentará todas as alterações realizadas em todos os arquivos do repositório, oferecendo uma visão abrangente das mudanças efetuadas, sem focar em um arquivo específico, ao contrário do comando <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark> <mark style="color:green;">arquivo</mark>.

#### Conteúdo Original dos Arquivos:

**index.html:**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Meu Site</title>
</head>
<body>
    <!-- Conteúdo do site -->
</body>
</html>
```

**style.css:**

```css
body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
}
```

#### Conteúdo Modificado dos Arquivos:

**index.html:**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Meu Novo Site</title>
</head>
<body>
    <!-- Conteúdo do site -->
</body>
</html>
```

**style.css:**

```css
body {
    font-family: Arial, sans-serif;
    background-color: #ffffff; /* Alteração de cor de fundo */
}
```

Ao executar o comando <mark style="color:purple;">git</mark> <mark style="color:orange;">diff</mark>, o output no terminal mostrará as diferenças entre o estado atual dos arquivos e o último commit. Ele indicará as alterações feitas em ambos os arquivos:

```sh
diff --git a/index.html b/index.html
index abcdef1..1234567 100644
--- a/index.html
+++ b/index.html
@@ -1,5 +1,5 @@
 <!DOCTYPE html>
 <html>
 <head>
-    <title>Meu Site</title>
+    <title>Meu Novo Site</title>
 </head>
 <body>

diff --git a/style.css b/style.css
index abcdef1..1234567 100644
--- a/style.css
+++ b/style.css
@@ -2,4 +2,4 @@
     font-family: Arial, sans-serif;
     background-color: #f0f0f0;
 }

+body {
+    background-color: #ffffff; /* Alteração de cor de fundo */
+}
```

Em que:

1.  **Diff do arquivo index.html:**

    ```sh
    diff --git a/index.html b/index.html
    ```

    Esta linha indica que está sendo mostrada a diferença entre dois arquivos: `a/index.html` (o arquivo original) e `b/index.html` (o arquivo modificado).
2.  **Cabeçalho de Mudança:**

    ```sh
    index abcdef1..1234567 100644
    --- a/index.html
    +++ b/index.html
    ```

    Este cabeçalho técnico fornece informações detalhadas sobre as mudanças nos arquivos e pode ser ignorado por enquanto, focando apenas nas alterações visíveis no conteúdo.
3.  **Linha de Mudança:**

    ```sh
    @@ -1,5 +1,5 @@
    ```

    Esta linha mostra a linha inicial e o número de linhas afetadas pela mudança em cada arquivo. No exemplo, `-1,5` indica que a mudança começa na linha 1 do arquivo original (`a/index.html`) e afeta 5 linhas. `+1,5` indica que a mudança começa na linha 1 do arquivo modificado (`b/index.html`) e também afeta 5 linhas.
4.  **Alterações Específicas:**

    ```sh
    -    <title>Meu Site</title>
    +    <title>Meu Novo Site</title>
    ```

    Essas linhas mostram as alterações específicas que ocorreram em cada versão do arquivo. \
    A linha original `<title>Meu Site</title>` foi removida (indicada pelo sinal `-`).\
    Em seu lugar, foi adicionada a linha `<title>Meu Novo Site</title>` (indicada pelo sinal `+`).
5.  **Diff do arquivo style.css:**

    ```sh
    diff --git a/style.css b/style.css
    ```

    Esta linha indica que está sendo mostrada a diferença entre dois arquivos: `a/style.css` (o arquivo original) e `b/style.css` (o arquivo modificado).
6.  **Cabeçalho de Mudança:**

    ```sh
    index abcdef1..1234567 100644
    --- a/style.css
    +++ b/style.css
    ```

    Assim como no arquivo `index.html`, este cabeçalho técnico fornece informações detalhadas sobre as mudanças nos arquivos e pode ser ignorado por enquanto, focando apenas nas alterações visíveis no conteúdo.
7.  **Linha de Mudança:**

    ```sh
    @@ -2,4 +2,4 @@
    ```

    Esta linha mostra a linha inicial e o número de linhas afetadas pela mudança em cada arquivo. No exemplo, `-2,4` indica que a mudança começa na linha 2 do arquivo original (`a/style.css`) e afeta 4 linhas. `+2,4` indica que a mudança começa na linha 2 do arquivo modificado (`b/style.css`) e também afeta 4 linhas.
8.  **Alterações Específicas:**

    ```sh
    +body {
    +    background-color: #ffffff; /* Alteração de cor de fundo */
    +}
    ```

    Essas linhas mostram as alterações específicas que ocorreram em cada versão do arquivo. Linhas com `+` indicam adições ou modificações no arquivo modificado (`b/style.css`). Neste caso, houve uma adição de estilo para alterar a cor de fundo do corpo da página para `#ffffff`.

{% hint style="warning" %}
Esta é uma explicação simplificada para fins didáticos. Para explorar todas as possibilidades do comando <mark style="color:purple;">`git`</mark><mark style="color:orange;">`diff`</mark>, consulte a [documentação oficial](https://git-scm.com/docs/git-diff/pt\_BR).
{% endhint %}
