# TCC Monografia Agent Context

Contexto repo-local para agentes atuando na monografia LaTeX do TCC2.

## Leitura obrigatoria

- `TEXTO-Principal.tex`
- `TEXTO-Introducao.tex`
- `TEXTO-FundamentacaoTeorica.tex`
- `TEXTO-Metodologia.tex`
- `TEXTO-Desenvolvimento.tex`
- `TEXTO-TrabalhosRelacionados.tex`
- `TEXTO-Conclusao.tex`
- `TEXTO-Bibliografia.bib`
- `/home/felip/repos/talus-droid/AGENTS.md`
- `/home/felip/repos/TCC-KANBAN.md`

## Escopo

Este repositorio contem a monografia em LaTeX do Talus-Droid/TCC2. A fonte de
verdade tecnica do robo fica em `/home/felip/repos/talus-droid`; o Trello `TCC2`
e a fonte de verdade das tarefas; o cache Obsidian gerado fica em
`/home/felip/syncthing/vault/10 Projetos/TCC Talus-Droid/TCC2-Kanban.md`.

## Git e remotos

- Branch base: `main`.
- Remoto GitHub: `github` (`git@github.com:felipedruzian/tcc-monografia.git`).
- Remoto Overleaf: `origin` (`https://git@git.overleaf.com/...`).
- Push normal de agentes vai para `github main`, salvo pedido explicito para
  sincronizar com Overleaf.
- Nao force-push.

## Regras de edicao

- Mudancas em `.tex` devem preservar o estilo academico e a estrutura ABNT atual.
- Antes de commitar alteracoes LaTeX, tente compilar localmente quando houver
  ferramenta disponivel. Se nao compilar por falta de ambiente, registre isso no
  resumo.
- Nao editar arquivos gerados por LaTeX nem PDFs exportados como fonte primaria.
- Figuras devem entrar em `figuras/` com nomes descritivos e referencias
  consistentes no texto.
- Evitar reescritas amplas sem escopo: prefira uma frente por vez
  (introducao, metodologia, resultados, conclusao, referencias).

## TCC / Trello / Obsidian

- Tarefas vivas ficam no Trello `TCC2`.
- `/home/felip/repos/TCC-KANBAN.md` e runbook/historico de migracao, nao o board
  vivo.
- O Kanban Obsidian e cache read-only gerado por `/home/felip/repos/scripts/trello-sync.py`.
- Novas pendencias encontradas na escrita devem virar cards Trello quando forem
  relevantes para planejamento.

## PRs e variantes

Existem branches/PRs historicas com variantes de reescrita. Antes de reaproveitar
texto delas, compare contra `main` e contra o estado atual do Talus-Droid. Nao
assumir que PR antiga esta atualizada so pelo nome da branch.
