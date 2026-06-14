# Figuras da monografia

Esta pasta reúne as imagens usadas ou candidatas a uso na monografia do TCC2. As figuras listadas abaixo foram adicionadas como **baseline preliminar auditado** em 2026-06-14, antes da regeneração visual final.

O objetivo deste baseline é deixar as imagens atuais versionadas e disponíveis para outros agentes/PRs, preservando o histórico do que foi avaliado. Quando as figuras forem corrigidas, a preferência é **manter os mesmos nomes de arquivo** e substituir os PNGs no Git, em vez de criar subpastas `v1`, `v2` ou `old`. Assim, as referências LaTeX permanecem estáveis e o histórico do Git documenta a evolução.

## Critérios usados na auditoria

A auditoria considerou o Manual de Normalização de Trabalhos Acadêmicos da UNIPAMPA/SisBi 2025 e os limites factuais do Talus-Droid:

- figuras, gráficos, quadros e esquemas são tratados como ilustrações;
- a chamada deve aparecer no texto antes ou próxima da figura;
- a identificação/caption deve seguir o padrão `Figura X - Título breve` no LaTeX;
- a fonte deve ficar abaixo da figura, em fonte menor e espaçamento simples;
- notas metodológicas devem ir preferencialmente na caption, no texto ou em nota abaixo da figura, não comprimidas dentro do PNG;
- títulos internos redundantes devem ser evitados quando a caption já identifica a figura;
- os resultados de VO/RTAB-Map não têm ground truth externo e devem ser apresentados como consistência relativa ou proxies internos, não como erro absoluto;
- ticks Hall são diagnóstico de movimento/simetria, não odometria oficial;
- wheel odom está fora do pipeline atual;
- drift deve ser descrito como relativo após a primeira amostra válida de `/rtabmap/odom`, em janela curta/controlada.

## Estado das figuras novas

| Arquivo | Estado atual | Uso recomendado | Observações para a próxima revisão |
| --- | --- | --- | --- |
| `talus_pipeline_ros_rtabmap_openloop.png` | Passa com ressalvas | Corpo do texto, em metodologia/desenvolvimento | Diagrama legível. Trocar termos menos acadêmicos, como "defendido" e "raspi", e mover o baseline textual para a caption ou nota. |
| `talus_vo_quality_summary.png` | Passa com ressalvas | Corpo do texto | Boa figura-síntese. Remover ou mover nota inferior cortada, traduzir "run" e explicar que quality/falhas/nós são proxies internos do RTAB-Map. |
| `db_node_xy_compare.png` | Passa com ressalvas | Apêndice; corpo apenas se discutir histórico exploratório | Há espaço vazio nos eixos e título interno em inglês com data. Usar como evidência preliminar de poses/nós estimados, sem sugerir ground truth. |
| `talus_motor_forward_deadband_v151_v155.png` | Falha temporária | Corpo, após regenerar | O rodapé e o eixo x estão sobrepostos/cortados. A nota sobre ticks Hall deve sair da imagem e ir para caption/fonte. |
| `talus_static_drift_v156_v166.png` | Falha temporária | Corpo, após regenerar | Texto inferior sobreposto/cortado. Suavizar a ideia de estabilidade e explicitar drift relativo após a primeira amostra válida. |
| `talus_vo_trajectories_xy_normalized.png` | Falha temporária | Corpo, após regenerar | Figura central para resultados, mas o PNG atual tem muito espaço branco, gráfico comprimido e legenda cobrindo dados. Regenerar com melhor enquadramento. |
| `odom_timeseries_compare.png` | Falha | No máximo apêndice; preferencialmente descartar do corpo | Muito densa, com três legendas repetidas, mistura de inglês/português e risco de interpretação indevida do yaw absoluto. |

## Captions/fonte sugeridas

Estas sugestões servem como ponto de partida para a inserção no LaTeX. Ajustar numeração e contexto conforme a seção final.

- `talus_pipeline_ros_rtabmap_openloop.png`  
  Caption: Pipeline experimental de percepção RGB-D/RTAB-Map e atuação em malha aberta.  
  Fonte: Elaboração própria (2026), com base na arquitetura experimental implementada no Talus-Droid.

- `talus_vo_quality_summary.png`  
  Caption: Proxies internos de qualidade da odometria visual e tamanho do grafo RTAB-Map por ensaio.  
  Fonte: Elaboração própria (2026), a partir dos bancos e registros RTAB-Map dos ensaios v156-v171.

- `db_node_xy_compare.png`  
  Caption: Poses XY estimadas nos nós do banco RTAB-Map em ensaios exploratórios.  
  Fonte: Elaboração própria (2026), a partir dos bancos RTAB-Map dos ensaios preliminares do Talus-Droid.

- `talus_motor_forward_deadband_v151_v155.png`  
  Caption: Ensaio de banda morta para avanço linear com contagem bruta dos sensores Hall.  
  Fonte: Elaboração própria (2026), a partir dos logs Hall v151-v155; os ticks são usados apenas como diagnóstico de movimento e simetria.

- `talus_static_drift_v156_v166.png`  
  Caption: Drift relativo de `/rtabmap/odom` com o robô parado em janela curta controlada.  
  Fonte: Elaboração própria (2026), a partir dos registros v156 e v166 de `/rtabmap/odom`, normalizados após a primeira amostra válida.

- `talus_vo_trajectories_xy_normalized.png`  
  Caption: Trajetórias XY relativas estimadas por odometria visual RGB-D/RTAB-Map em microdeslocamentos no chão.  
  Fonte: Elaboração própria (2026), a partir dos registros `/rtabmap/odom`; trajetórias normalizadas ao início de cada ensaio, sem ground truth externo.

- `odom_timeseries_compare.png`  
  Caption: Séries temporais de `/rtabmap/odom` em ensaios exploratórios de microdeslocamento.  
  Fonte: Elaboração própria (2026), a partir dos tópicos ROS 2 registrados nos ensaios do Talus-Droid.

## Próximo passo recomendado

Regenerar primeiro as figuras com falhas temporárias que têm maior valor acadêmico: `talus_vo_trajectories_xy_normalized.png`, `talus_motor_forward_deadband_v151_v155.png` e `talus_static_drift_v156_v166.png`. Em seguida, ajustar `talus_vo_quality_summary.png` e `talus_pipeline_ros_rtabmap_openloop.png`. A figura `odom_timeseries_compare.png` deve ser mantida apenas como apoio histórico ou descartada do corpo principal.
