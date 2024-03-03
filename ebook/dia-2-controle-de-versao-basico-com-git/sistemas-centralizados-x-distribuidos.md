---
cover: ../.gitbook/assets/Cabeçalho (1).svg
coverY: 0
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Sistemas Centralizados x Distribuídos

Existem dois tipos principais de sistemas de controle de versão: sistemas centralizados e sistemas distribuídos.

1. **Sistemas Centralizados**: Nesses sistemas, há um único repositório central onde todo o histórico de alterações e versões do código é armazenado. Os usuários fazem check-in (envio de alterações) e check-out (obtenção de uma cópia atualizada) do código desse repositório central. Exemplos incluem CVS (Concurrent Versions System) e SVN (Subversion).
2. **Sistemas Distribuídos**: Esses sistemas não dependem de um repositório central. Cada cópia do repositório contém todo o histórico de alterações, o que significa que os desenvolvedores podem trabalhar localmente e, em seguida, sincronizar suas alterações com os outros repositórios. Exemplos populares incluem Git, Mercurial e Bazaar.
