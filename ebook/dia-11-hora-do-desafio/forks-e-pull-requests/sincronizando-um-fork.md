# Sincronizando um Fork



\----

**Rascunho**

Você precisa atualizar seu fork quando o repositório original (upstream) teve mudanças e você quer manter seu fork sincronizado com a versão mais recente. Isso é útil para evitar conflitos ao contribuir com o projeto. Algumas situações comuns incluem:

1. **Antes de criar um Pull Request** → Para garantir que sua contribuição está baseada na versão mais atual do projeto.
2. **Quando há mudanças significativas no upstream** → Para manter seu fork atualizado e evitar conflitos futuros.
3. **Ao trabalhar em um fork de longo prazo** → Se você está desenvolvendo algo por um período maior, atualizar periodicamente evita desatualizações.
4. **Caso veja a mensagem “This branch is behind…” no GitHub** → O próprio GitHub avisa quando seu fork está desatualizado.
5. **Se precisar usar novas funcionalidades ou correções** → Se o upstream adicionou algo útil para o seu trabalho, atualizar o fork permite que você use essas novidades.

O GitHub facilita esse processo com a opção "Sync fork", mas você também pode fazer isso manualmente via terminal usando `git fetch upstream` e `git merge upstream/main`. 🚀

