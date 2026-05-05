# TCC-Monografia Agent Context

Instrucoes repo-locais para agentes trabalhando na monografia do TCC.

## Prioridade

Este repositorio e a frente textual do TCC. Evite mudancas amplas sem plano claro e mantenha rastreabilidade entre decisoes, texto e evidencias experimentais.

## Trello / tarefas

- Fonte da verdade para tarefas do TCC2: Trello board `TCC2`.
- Contexto operacional versionado: `/home/felip/repos/TCC-KANBAN.md`.
- Skill de apoio: `trello-tcc`.
- Edicoes vivas de cards devem usar o MCP `trello` no OpenCode.
- Slash command `/trello-sync` apenas exporta cache read-only para o Obsidian; nao use como caminho de edicao.
- Cache Obsidian: `/home/felip/syncthing/vault/Facul/TCC/TCC2-Kanban.md`.
- Script canonico do cache: `/home/felip/repos/scripts/trello-sync.py`.
- Credenciais ficam fora do git em `/home/felip/repos/.secrets/trello.env`; nunca imprimir chaves/tokens.

Ao revisar escopo, prioridades ou pendencias textuais, consulte Trello via MCP ou use o cache somente como apoio/historico.

## Relacao com Talus-Droid

O contexto tecnico/experimental vivo fica em `/home/felip/repos/talus-droid`.

Antes de alterar metodologia, desenvolvimento ou resultados, confira pelo menos:

- `/home/felip/repos/talus-droid/AGENTS.md`
- `/home/felip/repos/talus-droid/README.md`
- `/home/felip/repos/talus-droid/docs/HOSTS-CONTEXT.md`
- relatorios recentes em `/home/felip/repos/talus-droid/docs/reports/`

Nao inventar resultados. Use marcadores explicitos para evidencias pendentes quando necessario.

## LaTeX

- Base branch deste repo: `main`.
- Antes de commitar alteracoes em `.tex`, tente compilar localmente quando houver ferramenta disponivel.
- Se `pdflatex`/`latexmk` nao estiverem instalados no host, registre isso no test plan e prefira container ou slash command `/build-pdf` quando existir.
- O `.bib` principal e `TEXTO-Bibliografia.bib`; o Zotero/Better BibTeX pode atualiza-lo fora deste repo.

## GitHub / PRs

- O host `talus` deve manter o `gh` autenticado para permitir que agentes criem Pull Requests automaticamente.
- Verificacao rapida antes de finalizar trabalho remoto: `gh auth status --show-token=false`.
- O token/credencial do `gh` precisa permitir criacao de Pull Requests; na pratica, OAuth com escopo `repo` ou token fine-grained com `Contents: read/write` e `Pull requests: read/write`.
- Para desenvolvimentos longos, variantes de texto, execucoes pouco supervisionadas ou mudancas que devem ser revisadas comparativamente, o fluxo final esperado e:
  1. criar branch ou worktree isolada;
  2. implementar e validar;
  3. commitar apenas arquivos relacionados;
  4. fazer `git push -u github <branch>`;
  5. abrir PR com `gh pr create` ou MCP GitHub;
  6. entregar a URL do PR e o resumo de verificacao.
- Nao deixar apenas link manual de criacao de PR quando `gh`/MCP estiverem autenticados e com permissao; criar o PR automaticamente.
- Nao fazer push direto em `main`; use PR para revisao, especialmente em alteracoes textuais amplas da monografia.
