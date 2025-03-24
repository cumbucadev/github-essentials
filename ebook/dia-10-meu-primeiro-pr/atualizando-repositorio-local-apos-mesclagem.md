# Atualizando Repositório Local Após Mesclagem

Após a mesclagem de um Pull Request (PR) no repositório remoto, é essencial atualizar seu repositório local para garantir que você esteja trabalhando com a versão mais recente do código. Seguir esses passos evita conflitos e garante que suas futuras contribuições estejam alinhadas com a base de código principal.

## Passos

### 1. Mudar para o branch principal

Antes de atualizar o repositório local, certifique-se de que está no branch principal `main`. Para alternar para ele, execute:

```bash
git checkout main
```

### 2. Baixar as últimas alterações do repositório remoto

Agora, atualize seu branch principal baixando as últimas mudanças do repositório remoto:

```bash
git pull origin main
```

Isso garante que seu repositório local esteja sincronizado com as alterações feitas remotamente, incluindo o seu PR recentemente mesclado.

### 3. Remover branches locais obsoletos

Como o branch da feature já foi excluído no repositório remoto, você pode removê-lo do seu ambiente local com:

```bash
git branch -d nome-da-branch
```

***

Seguindo esses passos, seu repositório local estará atualizado e pronto para o próximo ciclo de desenvolvimento. Agora, você poderá iniciar uma nova tarefa com um ambiente limpo e sincronizado com o repositório remoto.
