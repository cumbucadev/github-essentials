# Unindo os Pontos

## Desfazendo Alterações Antes do Commit

* **`git restore <arquivo>`**: Este comando é usado para desfazer as mudanças feitas em um arquivo que ainda não foi comprometido. Ele **restaura o arquivo** para o estado que está no último commit ou na área de staging, descartando as modificações feitas.
* **`git reset HEAD <arquivo>`**: Este comando remove um arquivo da área de staging, mas **não o apaga do seu diretório de trabalho**. O arquivo permanece no seu diretório, mas não será incluído no próximo commit.

## Desfazendo Commits

* **`git revert hash-do-commit:`** Este comando cria um novo commit que reverte as alterações de um commit específico. Isso é útil quando você deseja desfazer algo que já foi feito, mas não quer afetar outros commits feitos depois desse.
* **`git reset HEAD~n:`** Este comando desfaz os "n" commits mais recentes, caso ainda não tenham sido enviados para o repositório remoto, preservando as alterações feitas no diretório de trabalho. É uma forma rápida de voltar para um estado anterior sem deixar rastros no histórico. Use `--soft` para manter as mudanças na área de staging.

## Alterando o Último Commit

