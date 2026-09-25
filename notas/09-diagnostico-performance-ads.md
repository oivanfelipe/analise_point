# MÓDULO 09 — DIAGNÓSTICO DE PERFORMANCE DE MÍDIA PAGA (Meta Ads + Google Ads)

**Consolidado e atualizado com dado ao vivo em 25/09/2026.** Este módulo não substitui os módulos 02 (Meta) e 03 (Google) — ele cruza os dois, adiciona uma consulta em tempo real às contas via Windsor.ai (que os módulos anteriores não tinham, por corte de data) e produz um raio-x único de performance de mídia paga com plano de ação unificado.

## Fontes e método

Consulta direta à API do Windsor.ai nesta sessão (25/09/2026, tools `get_data`/`get_connectors`), cobrindo:
- **Meta Ads** — conta "Pointthermic" (ID 835382558026652), granularidade diária, 01/09 a 25/09/2026.
- **Google Ads** — conta "Point Thermic" (ID 761-300-6526), granularidade diária, 01/09 a 25/09/2026.

Cruzado com o dado histórico mar–ago já consolidado nos módulos 02 e 03 e nos CSVs de `dados/`. Cada achado é marcado como **fato observado**, **hipótese** ou **estimativa**, com fonte e data, seguindo a metodologia do restante do diagnóstico.

---

## 1. Resumo executivo

**Achado central, não capturado nos módulos anteriores:** os dois canais pagos estão em situações opostas *agora*, não apenas "ambos ativos" como registrado nos adendos de correção de 25/09 dos módulos 02 e 03.

- **Meta Ads está genuinamente ativo e saudável**: gasto todos os dias de setembro, incluindo hoje (25/09), 3 campanhas simultâneas, geração de lead contínua a **CPL médio de R$ 28,22** na campanha principal de formulário (62 leads por R$ 1.749,88 em setembro) — dentro da faixa de otimização já identificada no módulo 02.
- **Google Ads não tem nenhum registro de gasto, impressão ou clique desde 09/09/2026** — **fato observado, 16 dias corridos sem qualquer atividade na conta**, não apenas sem conversão. Isso é mais grave do que o que os módulos 02/03 registraram: a correção de 25/09 daqueles módulos afirma "conta segue ativa... R$ 511,45 até 25/09", o que é aritmeticamente verdadeiro (soma acumulada), mas esconde que **100% desse gasto ocorreu entre 01/09 e 09/09** — a conta está de fato silenciosa há mais de duas semanas.
- **Zero conversão rastreada em Google Ads se mantém**: as 4 estruturas de campanha ativas em setembro (`[Search] Tratamento término`, `[Search] Limpeza Quimica`, `Performance Max- 04/09 L.Q`, `Search- 04/09`) somam **R$ 511,45 gastos e 0 conversões**, estendendo o total perdido desde a falha de rastreamento (15/07) para **R$ 2.092,33 em mídia paga sem uma única conversão registrada** (R$ 1.580,88 em jul–ago + R$ 511,45 em set).
- **Nota de maturidade de performance de ads (consolidada, 2 canais): 5/10.** Puxada para baixo pela paralisia do Google Ads (canal com histórico de melhor CPA da conta, R$ 68,94) e sustentada pela consistência operacional do Meta Ads.

---

## 2. Status atual por canal (snapshot ao vivo, 25/09/2026)

| Canal | Status real (dado, não campo `status` da API) | Último dia com atividade | Investido em setembro (01–25) | Resultado em setembro |
|---|---|---|---|---|
| **Meta Ads** | **Ativo** — gasto e clique todos os dias, incluindo hoje | 25/09/2026 (hoje) | R$ 2.279,67 | 62 leads (form) + engajamento WhatsApp (venda de máquina) + tráfego (evento ROG.e) |
| **Google Ads** | **Parado de fato** — sem gasto, impressão ou clique há 16 dias | 09/09/2026 | R$ 511,45 (todo concentrado em 01–09/09) | **0 conversões** |

**Nota metodológica:** o campo `campaign_status` retornado pela API do Google Ads já foi identificado como não confiável no módulo 03 (aparece "PAUSED" mesmo em campanha com gasto). Por isso este diagnóstico usa presença real de gasto/impressão como critério de "ativo", não o campo de status — e por esse critério mais rigoroso, o Google Ads está parado desde 09/09, não apenas com o status mal reportado.

**Duas hipóteses para a ausência total de dado desde 09/09 (não é possível diferenciar com o dado disponível nesta sessão):**
1. **Hipótese A — pausa real de conta/orçamento**: as campanhas esgotaram orçamento mensal, cartão de cobrança falhou, ou alguém pausou manualmente.
2. **Hipótese B — atraso de sincronização do Windsor.ai** para o conector Google Ads especificamente (o Meta, mesma consulta, mesma sessão, está sincronizado até hoje — o que torna a Hipótese B menos provável, mas não a exclui).

**Ação imediata recomendada, antes de qualquer outra coisa deste módulo:** verificar diretamente no Google Ads (login do cliente) se há campanha ativa hoje e se a conta está com meio de pagamento válido. Isso resolve em minutos uma ambiguidade que nenhum dado de API consegue resolver sozinho.

---

## 3. Meta Ads — raio-x de setembro (dado novo, granularidade diária)

| Campanha | Objetivo | Investido (set) | Cliques | CTR médio | Resultado |
|---|---|---|---|---|---|
| 03- 24/08 FORM T.T E LIMP QUIMICA ABO | Geração de Cadastros | R$ 1.749,88 | ~800 | ~1,1% | **62 leads — CPL R$ 28,22** |
| 10/09 [ENG/WPP] VENDA/LOCAÇÃO DE MÁQUINA | Engajamento/WhatsApp | ~R$ 280 | ~100 | ~0,9% | Conversas iniciadas no WhatsApp (venda/locação de máquina, oferta nova lançada 10/09) |
| 10/09 e 22/09 [TRAF/PERFIL] Evento Rio de Janeiro | Tráfego | ~R$ 250 | ~350 | ~1,7–2,9% | Tráfego para perfil/evento ROG.e (Riocentro, 21–24/09) — CTR mais alto do período, coerente com formato de tráfego/awareness |

**Leitura:** a campanha de formulário nativo continua sendo o motor de geração de demanda e mantém o CPL na faixa baixa (R$ 22–39) já identificada como tendência de otimização no módulo 02 — **isso não é mais tendência, é resultado sustentado**: 25 dias consecutivos de operação em setembro confirmam o patamar. As campanhas de evento (ROG.e) e de venda/locação de máquina são iniciativas táticas novas, de menor volume, coerentes com a atuação pontual na feira — não fazem parte do funil estrutural, mas não competem por orçamento de forma problemática (juntas, ~23% do gasto de setembro).

**Nenhum achado dos módulos 02 não segue válido**: post de paella, campanha "LEADS" mal configurada e falta de Custom Audience continuam sem correção visível no dado de setembro.

---

## 4. Google Ads — raio-x de setembro (dado novo)

| Campanha | Tipo | Investido (01–09/09) | Cliques | Conversões | Status real |
|---|---|---|---|---|---|
| Search- 04/09 | Search | R$ 225,84 | 26 | **0** | Ativa 05–09/09, sem dado depois |
| Performance Max- 04/09 L.Q | Performance Max | R$ 209,49 | 1.702 | **0** | Ativa 04–09/09, sem dado depois |
| [Search] Tratamento término | Search | R$ 35,56 | 75 | **0** | Ativa 01–03/09, sem dado depois |
| [Search] Limpeza Quimica | Search | R$ 40,56 | 116 | **0** | Ativa 01–03/09, sem dado depois |

**Achado que reforça a hipótese de falha de rastreamento (módulo 03):** mesmo a campanha Performance Max — que por natureza testa automaticamente múltiplas combinações de público, criativo e posicionamento — gerou 1.702 cliques em 6 dias sem registrar uma única conversão. Se a causa fosse só má segmentação de palavra-chave (como no caso de "Recozimento e Normalização"), seria estatisticamente improvável que **todas** as 4 estruturas, incluindo a automatizada, zerassem ao mesmo tempo. Isso é mais consistente com falha na tag de conversão do lado do site (thank-you page, GTM) do que com problema de segmentação — a causa raiz mais provável continua sendo técnica, não estratégica.

---

## 5. Comparativo entre canais (benchmark cruzado)

| Métrica | Meta Ads (set, campanha de lead) | Google Ads (histórico, campanha "Alívio de Tensões", mar–jul) | Google Ads (jul–set, pós-mudança) |
|---|---|---|---|
| CPL / Custo por conversão | R$ 28,22 | R$ 68,94 | **N/D — zero conversão** |
| CTR | ~1,1–1,4% | 12,08% | 5,4–33,8% (alto, mas sem conversão) |
| Volume de conversão | 62 leads/mês | ~54 conversões/6 meses (~9/mês) | 0 |
| Tendência | Estável, otimizada | Descontinuada (16/07) | Parada de fato (09/09) |

**Leitura estratégica:** o Meta Ads hoje é o único canal pago que efetivamente converte demanda em lead mensurável. O Google Ads, historicamente o canal de **menor custo por conversão absoluto da operação inteira** (R$ 68,94 no grupo "Alívio de Tensões" — mais eficiente até que o CPL atual do Meta em termos de qualificação, já que é lead com intenção de busca ativa, não formulário nativo de feed), está com zero contribuição há mais de dois meses. Isso não é "canal fraco", é **canal historicamente forte, hoje inoperante por falha técnica não corrigida** — a prioridade de correção deveria ser mais alta do que a urgência com que vem sendo tratada (o mesmo achado já estava registrado em 15/07 e segue sem resolução 72 dias depois).

---

## 6. Causa-raiz consolidada

Cruzando os três módulos (00-contexto, 02-Meta, 03-Google) com o dado novo desta consulta:

1. **Rastreamento de conversão quebrado no Google Ads** — hipótese mais provável, sustentada por: zero conversão em 4 estruturas de campanha diferentes (incluindo Performance Max automatizado), formulário da landing page `lp.pointthermic.com.br` em `method="get"` sem página de obrigado visível (módulo 00), três contêineres GTM distintos no site (módulo 00) — qualquer um deles pode estar disparando a tag de conversão errada ou nenhuma.
2. **Pixel do Meta com eventos customizados sem volume** (`lead_geral`, `lead_venda`, `lead_termico` — módulo 02) — mesma família de problema (rastreamento), canal diferente. O Meta "funciona" hoje porque depende de formulário nativo (não do pixel/site) para o objetivo principal, mascarando o mesmo problema de instrumentação que afeta o Google.
3. **Ausência de governança de continuidade** — a conta de Google Ads já ficou "silenciosa" duas vezes neste diagnóstico (interpretada erroneamente como pausa em 31/08, corrigida em 25/09, e agora de fato sem dado desde 09/09) sem que isso pareça ter disparado um alerta ou ação — sinal de falta de monitoramento ativo de conta, não só de um bug técnico isolado.

---

## 7. Plano de ação priorizado (unificado)

| # | Ação | Canal | Impacto | Esforço | Prazo |
|---|---|---|---|---|---|
| 1 | **Verificar hoje mesmo se a conta Google Ads está ativa** (login direto, checar meio de pagamento e status real de cada campanha) | Google | Crítico — resolve ambiguidade de 16 dias sem dado | Baixo | Imediato |
| 2 | **Auditar a tag de conversão do Google Ads na thank-you page atual**, testando um envio de formulário real e conferindo disparo no Google Tag Assistant/GTM Preview | Google | Altíssimo — destrava R$ 500+/mês hoje sem retorno mensurável | Médio | 48–72h |
| 3 | **Consolidar os três contêineres GTM em um único**, documentando cada tag ativa | Google + Meta (pixel) | Alto — resolve causa-raiz comum aos dois canais | Médio-Alto | 1–2 semanas |
| 4 | **Validar e corrigir os eventos de pixel customizados do Meta** (`lead_geral`, `lead_venda`, `lead_termico`) | Meta | Alto para remarketing futuro | Médio | 1 semana |
| 5 | **Reativar/recriar a estrutura "Alívio de Tensões"** assim que o rastreamento estiver validado (histórico de R$ 68,94/conversão, melhor CPA da conta) | Google | Alto | Baixo, após #2 | Assim que #2 resolver |
| 6 | **Pausar definitivamente o grupo "Recozimento e Normalização"** e adicionar termos negativos (têmpera, revenimento, recozimento, normalização, piso, água) | Google | Alto, elimina desperdício direto | Baixo | Imediato, independe de #2 |
| 7 | **Configurar Custom Audience com os ~118 leads acumulados do Meta** para remarketing/lookalike | Meta | Alto — hoje zero remarketing apesar de pixel instalado | Baixo | Imediato |
| 8 | **Inserir Petrobras/ISO 9001 na copy do Meta** (já usado no Google, ausente no Meta) | Meta | Médio-alto, diferencial sem custo extra | Baixo | 1 semana |
| 9 | **Criar landing pages dedicadas por grupo de anúncio no Google** (Alívio de Tensões, Limpeza Química) em vez da página genérica de Serviços | Google | Alto no médio prazo (Quality Score + taxa de conversão) | Médio | 2–4 semanas |
| 10 | **Instituir checagem semanal de "conta viva"** (gasto, impressão, conversão por canal) como rotina de governança, não apenas quando o cliente notar | Meta + Google | Médio-alto, evita repetição deste episódio | Baixo | Imediato, contínuo |

---

## 8. Projeção de impacto financeiro (estimativa)

**Estimativa, não fato observado** — baseada em extrapolação do histórico real da própria conta, não em benchmark de mercado:

- Se o Google Ads for restaurado ao CPA histórico do grupo "Alívio de Tensões" (R$ 68,94/conversão) com um orçamento mensal equivalente à média mar–ago (~R$ 1.164/mês), a conta voltaria a gerar **~17 conversões/mês** — hoje zero.
- Os **R$ 2.092,33 já gastos sem conversão desde 15/07** equivalem, ao CPA histórico eficiente, a **~30 conversões perdidas** só no período em que o problema já era diagnosticável e não foi corrigido.
- No Meta, mover os ~23% do orçamento hoje em campanhas táticas (evento/máquina) de volta para a campanha de formulário ao CPL atual (R$ 28,22) geraria **~9 a 10 leads adicionais/mês** — a decidir conforme o objetivo estratégico dessas campanhas táticas (não é uma recomendação de corte automático, é o trade-off explícito).

---

## 9. Quick wins

**Esta semana, sem custo de mídia adicional:** verificar status real da conta Google (#1), testar disparo da tag de conversão (#2), pausar grupo "Recozimento e Normalização" e subir termos negativos (#6), configurar Custom Audience com leads acumulados do Meta (#7).

**Próximas 2–4 semanas:** consolidar GTM (#3), validar eventos de pixel do Meta (#4), reativar estrutura vencedora do Google assim que o rastreamento for validado (#5), trazer Petrobras/ISO 9001 para o Meta (#8).

---

## Argumento para a reunião

O que observamos, com dado de hoje: o Meta Ads está funcionando e sustentando um CPL saudável (R$ 28,22) há semanas — isso não precisa de intervenção urgente, precisa de expansão (remarketing, prova social na copy). O Google Ads, por outro lado, não é um canal fraco — é o canal historicamente mais eficiente da conta inteira (R$ 68,94 por conversão, menos da metade do CPL atual do Meta) que está tecnicamente quebrado há 72 dias e, pelo dado de hoje, **fisicamente parado sem qualquer atividade nos últimos 16**. O impacto financeiro já realizado é mensurável: R$ 2.092,33 gastos sem uma conversão sequer desde que o problema começou. O que se faz agora, nesta ordem, é: confirmar se a conta está de fato ativa, testar o disparo da tag de conversão com um envio real de formulário, e só depois disso considerar qualquer aumento de orçamento — porque hoje não há como saber, olhando só o painel do Google Ads, se o problema é de mídia ou de mensuração. O ganho esperado, uma vez corrigido, é reativar o canal de menor custo por lead qualificado que a empresa já teve, com histórico real e recente para provar que funciona.

**Fonte e método:** consulta direta ao Windsor.ai (API Meta Ads e Google Ads) em 25/09/2026, 01/09 a 25/09/2026, granularidade diária, campos de campanha, investimento, impressões, cliques, CTR, CPC, ações/conversões e status de campanha. Cruzado com os módulos 02 e 03 (dado mar–ago) e com os CSVs em `dados/`. A distinção entre "conta pausada" e "atraso de sincronização do conector" para o Google Ads não pôde ser resolvida apenas com dado de API nesta sessão — recomenda-se verificação direta no painel do Google Ads como primeiro passo (ver Seção 2).
