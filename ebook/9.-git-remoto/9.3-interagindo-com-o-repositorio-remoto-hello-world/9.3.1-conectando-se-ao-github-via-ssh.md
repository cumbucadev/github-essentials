# Conectar-se ao GitHub via SSH

Quando trabalhamos com o GitHub, muitas vezes precisamos provar que somos nós mesmos antes de realizar ações como enviar código ou clonar repositórios. Isso se chama autenticação. Em vez de digitar usuário e senha toda vez, podemos usar uma conexão SSH para facilitar esse processo.

## O que é uma conexão SSH?

SSH (Secure Shell) é um sistema que permite a comunicação segura entre dois computadores. Imagine que é como um túnel protegido entre sua máquina e um servidor, garantindo que ninguém mais possa ver ou modificar os dados que estão sendo trocados.

No contexto do GitHub, uma conexão SSH permite que seu computador fale com o servidor do GitHub de forma segura, sem precisar digitar credenciais toda vez. Isso é feito através de um par de chaves.

### O que são as chaves SSH?

As chaves SSH funcionam como o registro de um crachá de acesso digital para sua máquina. Pense em um prédio com segurança na entrada: para entrar sem precisar se identificar a cada vez, você recebe um crachá. Esse crachá tem duas partes:

* **Parte que fica com você (chave privada)**: Assim como um crachá físico que você carrega no bolso, a chave privada fica armazenada no seu computador e nunca deve ser compartilhada.
* **Parte registrada na portaria (chave pública)**: Para que você possa entrar no prédio sem problemas, seu crachá precisa estar registrado na recepção. No caso do GitHub, isso significa adicionar sua chave pública à sua conta.

Quando você tenta se conectar ao GitHub via SSH, ele verifica se a "portaria" (o GitHub) tem o registro da sua chave pública e se ela corresponde à chave privada que está com você. Se tudo estiver certo, você entra sem precisar digitar senha.

As chaves SSH são, na verdade, apenas arquivos de texto com um conteúdo aparentemente embaralhado. A chave privada geralmente fica salva no seu computador em um arquivo chamado `id_rsa` (ou similar), enquanto a chave pública fica em outro arquivo chamado `id_rsa.pub`. O conteúdo da chave pública começa com `ssh-rsa` e continua com uma longa sequência de caracteres aleatórios.

## Configurando uma conexão SSH com o GitHub

### Gerando uma nova chave SSH e adicionando-a ao agente SSH

A primeira parte para fazer a conexão com o GitHub é gerar o seu crachá (chave privada) e o seu registro que futuramente será adicionado à portaria (chave pública).

Além disso, é necessário adicionar a chave ao **agente SSH**, que é um programa que guarda sua chave privada em memória para que você não precise digitá-la toda vez que for se conectar ao GitHub. É como se fosse um chaveiro que mantém seu crachá sempre pronto para ser usado.

Para completar essas duas etapas, siga os passos da documentação oficial, se atentando para selecionar o sistema operacional correto.

{% embed url="https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent" %}

### Adicionar uma nova chave SSH à sua conta do GitHub

Agora iremos cadastrar o registro do crachá criado à portaria do GitHub.

Para isso, siga os passos da documentação oficial, se atentando para selecionar o sistema operacional correto.

{% embed url="https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account?tool=webui" %}

### Testar a conexão SSH

Agora é hora de verificar se seu crachá está funcionando e se você passa na portaria.

Para isso, siga os passos da documentação oficial, se atentando para selecionar o sistema operacional correto.

{% embed url="https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/testing-your-ssh-connection" %}

***

Agora que você configurou sua chave SSH e testou a conexão, seu ambiente está pronto para interagir com o GitHub de forma segura e prática. O próximo passo é clonar um repositório, e agora você pode fazer isso sem precisar digitar usuário e senha. Caso troque de máquina ou precise configurar outro dispositivo, basta repetir o processo para gerar uma nova chave e adicioná-la ao GitHub.&#x20;
