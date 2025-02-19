# Unindo os Pontos

Quando trabalhamos com Git em projetos colaborativos, a capacidade de gerenciar diferentes versões do código de forma organizada e sem interferir no trabalho dos outros é essencial.&#x20;

O uso de **branches** (ramificações) permite que pessoas trabalhem em funcionalidades ou correções de forma isolada, sem afetar a base principal do código. Ao entender como criar, alternar e mesclar branches, conseguimos integrar essas alterações de forma eficiente, mantendo o código sempre atualizado e funcional.

* **git branch**: Um branch é uma linha de desenvolvimento independente. Com o comando `git branch`, você cria uma ramificação do código, permitindo que trabalhe em novas funcionalidades ou correções sem impactar o branch principal.
* **git switch**: O comando `git switch` é utilizado para alternar entre diferentes branches de forma simples e rápida. Ele permite que você mude de um branch para outro sem perder o progresso em que está trabalhando, facilitando a navegação entre várias linhas de desenvolvimento.
* **git merge**: Após concluir as alterações em um branch, você pode querer integrar essas mudanças de volta ao branch principal. O comando `git merge` é utilizado para combinar as alterações de dois branches. Quando não há conflitos, o merge é feito automaticamente.
* **Resolução de Conflitos**: Os conflitos acontecem quando duas alterações incompatíveis são feitas na mesma parte do código em diferentes branches. Nesses casos, o Git não sabe qual versão manter. Para resolver, você precisa revisar manualmente os arquivos conflitantes, decidir qual código manter ou combinar as mudanças e, em seguida, realizar o commit da resolução.

***

Em seguida, veremos um exemplo prático de como esses comandos funcionam.
