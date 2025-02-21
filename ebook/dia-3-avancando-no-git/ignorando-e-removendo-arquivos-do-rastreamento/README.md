# Ignorando e Removendo Arquivos do Rastreamento Local

## O que significa "rastrear" um arquivo no Git?

No Git, um arquivo "rastreado" é aquele que está sob monitoramento do sistema de controle de versões. Isso significa que qualquer modificação feita nesse arquivo pode ser detectada e registrada no histórico do repositório.

## Por que não **rastrear** um arquivo?

Em alguns casos, pode ser útil impedir que o Git acompanhe determinadas mudanças ou até mesmo remover arquivos do rastreamento. Veja algumas situações comuns:

### **1. Arquivos temporários ou configurações pessoais**

Alguns arquivos são específicos do seu ambiente e não precisam ser compartilhados no repositório.

📌 **Exemplo:** Você criou um arquivo `config.txt` com preferências personalizadas do seu editor de código. Esse arquivo só faz sentido para você e não deve ser incluído no controle de versões.

### **2. Arquivos grandes ou desnecessários**

Arquivos pesados, como vídeos e imagens, podem tornar o repositório lento e difícil de gerenciar, especialmente se não forem essenciais ao projeto.

📌 **Exemplo:** Você adicionou um vídeo `tutorial_grande.mp4`, mas percebeu que ele não é necessário para os colaboradores do repositório.

### **3. Arquivos gerados automaticamente**

Muitos sistemas criam arquivos temporários, caches ou logs que não precisam ser armazenados no Git, pois são recriados automaticamente.

📌 **Exemplo:** Seu projeto gera um arquivo `log.txt` sempre que o programa roda. Esse arquivo contém informações de depuração momentâneas e não deve ser versionado.

### **4. Arquivos adicionados por engano**

É comum adicionar arquivos ao repositório sem querer. Felizmente, o Git permite remover arquivos do rastreamento sem apagá-los do disco.

📌 **Exemplo:** Você sem querer adicionou um banco de dados temporário `temp.db` ao repositório, mas ele não deve fazer parte do versionamento.

## Em resumo

* **Rastrear** um arquivo significa que o Git está **controlando todas as alterações** feitas nesse arquivo.
* Você pode querer **parar de rastrear** um arquivo por diversos motivos, como quando ele é específico do seu computador, quando é desnecessário ou quando foi adicionado acidentalmente.

Esses exemplos mostram situações comuns onde parar de rastrear um arquivo é uma decisão prática para manter seu repositório limpo e eficiente.

Neste capítulo, veremos como evitar o rastreamento e como remover arquivos do controle do Git sem excluí-los.
