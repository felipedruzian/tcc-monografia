# Checkpoint de fechamento de semestre - TCC2

Data: 2026-06-16

## Contexto

Este checkpoint registra o estado da monografia e do projeto Talus-Droid no fechamento do semestre 2026/1. A versao atual foi integrada na `main`, enviada ao GitHub e sincronizada com o Overleaf, mas ainda nao representa uma versao pronta para defesa final.

O texto foi reorganizado para ter tom de versao final e servir como entrega de revisao ao orientador. A intencao academica, no entanto, e dar continuidade ao desenvolvimento no semestre 2026/2, com mais tempo para concluir a validacao do robo, aprofundar os experimentos e fechar a defesa em condicoes melhores.

## Estado da monografia

- Repositorio: `/home/felip/repos/tcc-monografia`
- Branch base: `main`
- Commit sincronizado com GitHub e Overleaf: `fe75064`
- Remoto GitHub: `github/main`
- Remoto Overleaf: `origin/master`
- PR5 integrado na `main`
- Figuras regeneradas de resultados foram versionadas e referenciadas no capitulo de resultados
- VSCode/LaTeX Workshop configurado para gerar artefatos em `build/`

A monografia agora apresenta:

- introducao, metodologia, desenvolvimento, resultados e conclusao com tom de versao final;
- resultados tratados como primeira linha de base experimental;
- limitacoes explicitadas sobre odometria de rodas, giros, trajetorias longas e sensibilidade do RTAB-Map;
- continuidade futura ligada a odometria robusta, Nav2, offloading e sensores modernos.

## Estado tecnico do robo

O Talus-Droid ainda nao esta finalizado para a defesa pretendida. A plataforma fisica existe, o pipeline ROS 2/RTAB-Map foi exercitado e ha evidencias iniciais de micro-mapeamento controlado, mas a validacao completa ainda esta pendente.

Pendencias tecnicas principais:

- validar odometria de rodas de forma confiavel;
- integrar/fundamentar fusao sensorial com `robot_localization`;
- estabilizar VO RGB-D em movimentos reais mais longos;
- melhorar comportamento em giros e trajetorias com maior variacao visual;
- consolidar protocolo experimental de desempenho;
- decidir e executar a comparacao/otimizacao final prometida no escopo do TCC.

## Encaminhamento planejado

O proximo passo academico e retornar ao orientador com esta versao para alinhar os encaminhamentos formais. A premissa atual e nao defender no fim de 2026/1, mas usar esta entrega como marco de revisao e continuar o projeto no semestre 2026/2.

## Locais de verdade apos este checkpoint

- Monografia e texto academico: `/home/felip/repos/tcc-monografia`
- Implementacao e estado tecnico do robo: `/home/felip/repos/talus-droid`
- Tarefas vivas: Trello `TCC2`
- Historico/runbook de gestao: `/home/felip/repos/TCC-KANBAN.md`
- Memoria compartilhada entre sessoes Codex: `/home/felip/.codex/memories/TCC-AND-TALUS-STATUS.md`

