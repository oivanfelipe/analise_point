# MÓDULO 10 — PROJEÇÃO DE MERCADO

**Nota de metodologia:** este módulo corresponde ao módulo 09 ("Projeção de mercado") da metodologia Doutor Carvalho (V4 Company — Carvalho & Co.), executado em 25/09/2026. Foi renumerado para 10 neste repositório porque o número 09 já estava em uso pelo diagnóstico de performance de ads consolidado (`09-diagnostico-performance-ads.md`).

Este módulo não usa dado real de vendas da Point Thermic (a empresa não expõe CRM nem funil comercial publicamente). Ele dimensiona o que o mercado entrega, em benchmark, para um negócio com este nicho, este modelo e este ticket, dado o funil identificado nos módulos anteriores. **É dimensionamento, não promessa.**

## 1. Contexto coletado dos módulos anteriores

| Parâmetro | Valor | Origem |
|---|---|---|
| Nicho | Tratamento térmico de alívio de tensões, limpeza química e descontaminação industrial | Módulo 00 |
| Modelo de negócio | B2B industrial, projeto/contrato, decisão técnica multi-stakeholder | Módulo 00 |
| Ticket médio | R$ 5.000 a R$ 15.000 por projeto/contrato | Informado pelo usuário nesta sessão (não observável publicamente) |
| Região de atuação | Nacional | Módulo 00 |
| Funil comercial | Time comercial com qualificação (inside sales / SDR) | Informado pelo usuário nesta sessão |
| Canais ativos | Meta Ads e Google Ads (LinkedIn Ads não avaliado nesta análise) | Módulos 02 e 09 |
| Horizonte de projeção | Mensal | Informado pelo usuário nesta sessão |
| Meta de resultado | Não informada — usa referência padrão de operação mínima viável (10 vendas/mês para B2B com inside sales) | Padrão da metodologia |

## 2. Benchmarks coletados (WebSearch, 25/09/2026)

Cada linha cruza no mínimo duas fontes independentes, exceto quando indicado. Aderência: Alta (Brasil + nicho ou porte de ticket compatível), Média (setor amplo ou fora do Brasil), Baixa (genérico).

| Canal / etapa | Métrica | Mín | Máx | Fonte | Aderência |
|---|---|---|---|---|---|
| Google Ads (Search) | CTR | 2,41% | 6,57% | WordStream 2026, WebFX 2026 | Média — B2B services vs. industrial/comercial, EUA |
| Google Ads (Search) | CVR clique→lead | 5% | 10% | WebFX 2026 | Média — B2B services, EUA |
| Google Ads (Search) | CPL | US$ 85,63 (≈ R$ 445, câmbio 5,20) | — | Web Tonic 2026 (comparativo dentro de artigo de Meta Ads) | Média — industrial genérico, EUA |
| Meta Ads | CTR | 0,78% | 4,3% (industrial otimizado) | LocaliQ 2026, Web Tonic 2026 | Média — B2B genérico vs. industrial |
| Meta Ads | CPL genérico | US$ 50 (≈ R$ 260) | US$ 150 (≈ R$ 780) | Web Tonic 2026 | Baixa — B2B genérico, EUA |
| Meta Ads | CPL industrial segmentado | US$ 4,83 (≈ R$ 25) | US$ 15,65 (≈ R$ 81) | Web Tonic 2026 | Média — manufatura/industrial, EUA |
| Funil comercial | Lead → MQL | 20% | 45% (top quartile) | Data-Mania 2026, MarketJoy 2026 | Baixa — genérico, não Brasil |
| Funil comercial | MQL → SQL | 35% | 50% | RD Station Panorama de Vendas 2025 | **Alta** — Brasil, B2B com SLA formalizado |
| Funil comercial | SQL → Oportunidade | 50% | 70% | RD Station Panorama de Vendas 2025 | **Alta** — Brasil, B2B com discovery estruturado |
| Funil comercial | Oportunidade → Venda | 25% | 35% | Landbase 2026 (win rate por porte de negócio, ticket < US$ 50 mil) | Média — porte de ticket compatível, não Brasil |
| Ciclo de venda | Duração | 3 meses | 18 meses | Gartner 2024 (via agenciatribo.com.br) | **Alta** — vendas complexas B2B industriais |

**Achado de cruzamento importante, mais forte que qualquer benchmark externo:** a própria conta da Point Thermic já opera, quando ativa, **dentro ou abaixo da faixa otimista** desses benchmarks. O CPL real do Meta Ads em setembro de 2026 foi de R$ 28,22 (módulo 09) — dentro da faixa de CPL industrial segmentado (R$ 25–81) e muito abaixo do CPL genérico B2B (R$ 260–780). O melhor CPA histórico do Google Ads (grupo "Alívio de Tensões") foi R$ 68,94 — abaixo do benchmark industrial genérico (R$ 445). **Por isso, este módulo usa o CPL real da própria conta como referência de mídia em vez do benchmark externo genérico**, reservando a incerteza do benchmark de mercado exclusivamente para as etapas do funil comercial, onde não há dado interno disponível (a empresa não expõe CRM).

Fonte de câmbio: USD/BRL 5,20 em 25/09/2026 (TradingEconomics/Investing, consultado nesta sessão).

## 3. Faixa de investimento sugerida (cálculo retroativo)

Meta de resultado âncora: **10 vendas/mês**, referência de operação mínima viável para B2B com inside sales de 1 a 2 pessoas.

**CPL usado (dado real da própria conta, não benchmark externo):**
- Google Ads: R$ 68,94/lead (CPA histórico real, grupo mais eficiente da conta)
- Meta Ads: R$ 28,22/lead (CPL real de setembro/2026)
- Distribuição de investimento: como o LinkedIn Ads não está ativo, a distribuição padrão da metodologia (50% Google / 30% Meta / 20% LinkedIn) é renormalizada entre os dois canais ativos: **62% Google / 38% Meta**.
- CPL médio ponderado: 0,62 × R$ 68,94 + 0,38 × R$ 28,22 = **R$ 53,45/lead**

**Cálculo do funil, de trás para frente:**

| Etapa | Cenário otimista (taxas máximas) | Cenário conservador (taxas mínimas) |
|---|---|---|
| Vendas (meta) | 10 | 10 |
| ÷ Oportunidade→Venda | ÷ 35% = 29 oportunidades | ÷ 25% = 40 oportunidades |
| ÷ SQL→Oportunidade | ÷ 70% = 41 SQLs | ÷ 50% = 80 SQLs |
| ÷ MQL→SQL | ÷ 50% = 82 MQLs | ÷ 35% = 229 MQLs |
| ÷ Lead→MQL | ÷ 40% = **204 leads** | ÷ 20% = **1.143 leads** |
| × CPL médio ponderado | × R$ 53,45 | × R$ 53,45 |
| **Investimento necessário** | **≈ R$ 10.900/mês** | **≈ R$ 61.100/mês** |

**Faixa de investimento sugerida: entre R$ 10.900 e R$ 61.100 por mês para sustentar 10 vendas/mês.**

A distância entre os dois extremos (5,6 vezes) não vem do custo de mídia — o CPL é o mesmo nos dois cálculos, porque já é dado real da própria conta, não uma variável de incerteza aqui. **A distância inteira vem da eficiência do funil comercial** (lead até venda), que passa de 4,9% no cenário otimista para 0,875% no cenário conservador. Isso é o achado central deste módulo: a alavanca de maior impacto no resultado não está na mídia paga, que já opera em nível competitivo, está no processo comercial que recebe o lead depois que ele é gerado.

## 4. Funil benchmark projetado — dois cenários

### Cenário 1 — Mínimo Viável

Usa o investimento mínimo da faixa (R$ 10.900/mês) com as taxas mínimas do benchmark comercial em cada etapa. Representa o resultado se o investimento for contido e a execução comercial for apenas mediana, sem SLA formal entre marketing e vendas.

| Etapa | Taxa aplicada | Volume |
|---|---|---|
| Investimento | — | R$ 10.900 |
| Leads (CPL médio R$ 53,45) | — | 204 |
| MQL | 20% | 41 |
| SQL | 35% | 14 |
| Oportunidade | 50% | 7 |
| **Vendas** | 25% | **2** |
| **Receita projetada** (ticket R$ 5.000–15.000) | — | **R$ 10.000 a R$ 30.000** |

ROAS estimado: 0,9x a 2,8x sobre o investimento em mídia. **Confiança: Média** — CPL é dado real, mas as taxas de funil comercial no piso combinam para um resultado severamente comprimido.

### Cenário 2 — Potencial de Mercado

Usa o investimento máximo da faixa (R$ 61.100/mês) com as taxas máximas do benchmark comercial. Representa o que os melhores operadores do setor entregam com SLA de marketing-vendas formalizado e discovery comercial estruturado — não é o teto absoluto.

| Etapa | Taxa aplicada | Volume |
|---|---|---|
| Investimento | — | R$ 61.100 |
| Leads (CPL médio R$ 53,45) | — | 1.143 |
| MQL | 40% | 457 |
| SQL | 50% | 229 |
| Oportunidade | 70% | 160 |
| **Vendas** | 35% | **56** |
| **Receita projetada** (ticket R$ 5.000–15.000) | — | **R$ 280.000 a R$ 840.000** |

ROAS estimado: 4,6x a 13,7x sobre o investimento em mídia. **Confiança: Baixa a Média** para o volume absoluto — ver validação de capacidade abaixo, que restringe a leitura deste número.

### 4.1 Comparativo entre cenários

| Indicador | Cenário 1 — Mínimo Viável | Cenário 2 — Potencial de Mercado |
|---|---|---|
| Investimento mensal | R$ 10.900 | R$ 61.100 |
| Leads | 204 | 1.143 |
| MQL | 41 | 457 |
| SQL | 14 | 229 |
| Oportunidades | 7 | 160 |
| Vendas | 2 | 56 |
| Receita (ticket médio R$ 10.000) | R$ 20.000 | R$ 560.000 |
| ROAS estimado | ~1,8x | ~9,2x |

## 5. Validações obrigatórias

**Compatibilidade com o mercado:** o mercado de óleo e gás e manutenção industrial no Brasil (módulo 00, capex da ordem de dezenas de bilhões de dólares) absorve com folga qualquer um dos dois cenários — R$ 20 mil a R$ 560 mil/mês é irrelevante em relação ao tamanho do mercado. A restrição real não está do lado do mercado.

**Capacidade comercial — restrição real identificada:** 56 vendas/mês (Cenário 2) equivalem a mais de duas vendas por dia útil de novos contratos de serviço técnico industrial. Não há evidência pública de que a Point Thermic tenha estrutura comercial e operacional (equipes de campo, capacidade de execução simultânea de tratamento térmico e limpeza química) para atender esse volume. **Recomenda-se tratar o Cenário 2 como o teto que o mercado permite, não como meta operacional imediata** — o investimento em mídia sem o correspondente investimento em capacidade comercial e operacional gera leads perdidos, não receita.

**Ciclo de venda:** com ciclo de venda de 3 a 18 meses para vendas B2B industriais complexas (multi-stakeholder, aprovação técnica), a receita projetada em um horizonte mensal representa o **regime estacionário de uma operação já madura**, não o resultado do primeiro mês de investimento. Os primeiros meses de qualquer aumento de investimento tendem a mostrar leads e oportunidades se acumulando no funil, sem receita proporcional ainda realizada — isso é esperado, não é sinal de falha.

**Nível de confiança geral do módulo: Médio.** Alta aderência no CPL (dado real da própria conta) e nas taxas MQL→SQL e SQL→Oportunidade (benchmark brasileiro, RD Station). Aderência baixa a média na taxa Lead→MQL e no benchmark de Oportunidade→Venda (fontes internacionais, não específicas do nicho). O ticket médio é uma estimativa informada pelo usuário, não validada com dado do cliente.

## 6. Pressupostos declarados

1. Ticket médio: R$ 5.000 a R$ 15.000 por projeto, estimativa informada nesta sessão, não confirmada com o cliente.
2. Horizonte: mensal, representando regime estacionário (ver ressalva de ciclo de venda acima).
3. Distribuição de investimento: 62% Google Ads / 38% Meta Ads, renormalização da distribuição padrão da metodologia (50/30/20) sem LinkedIn Ads ativo.
4. CPL de mídia: dado real da própria conta (R$ 68,94 Google, R$ 28,22 Meta), não benchmark externo — decisão metodológica registrada na seção 2, por ser evidência mais forte que estimativa de terceiros.
5. Taxas de funil comercial: benchmark de mercado (RD Station Brasil para MQL→SQL e SQL→Oportunidade; benchmarks internacionais para Lead→MQL e Oportunidade→Venda), por ausência de dado interno de CRM da Point Thermic.
6. Capacidade operacional: não considerada como limite matemático no cálculo, mas sinalizada como restrição real na validação da seção 5 — o Cenário 2 provavelmente excede a capacidade atual de entrega.
7. Investimento considerado é de mídia paga apenas; não inclui fee de gestão, produção de criativo ou custo de equipe comercial adicional.

## Insight acionável

O mercado entrega, para uma operação de mídia paga que já funciona (a Point Thermic já prova isso com CPL de R$ 28,22 no Meta), uma receita mensal projetada entre R$ 20 mil (mínimo viável) e R$ 560 mil (potencial de mercado, condicionado a capacidade comercial que ainda não está comprovada). A diferença entre os dois cenários é de R$ 540 mil por mês, e essa diferença não vem de gastar mais em anúncio: vem inteiramente da eficiência do funil comercial depois que o lead chega.

Para cada real investido em mídia hoje, o benchmark indica um retorno entre 1,8x (execução comercial mediana) e 9,2x (execução comercial madura, com SLA formal entre marketing e vendas). A alavanca mais barata e mais rápida para sair do mínimo viável em direção ao potencial de mercado não é aumentar o orçamento de mídia — é formalizar o processo comercial: um SLA de tempo de resposta entre lead e primeiro contato, critérios explícitos de qualificação (o que torna um lead um MQL, o que torna um MQL um SQL) e um discovery comercial estruturado. O próprio benchmark usado aqui mostra que isso sozinho move a taxa MQL→SQL de 35% para 50%, e a SQL→Oportunidade de 50% para 70% — ganhos que multiplicam ao longo do funil sem gastar um real a mais em anúncio.

Fonte e método: pesquisa ao vivo via WebSearch em 25/09/2026 (WordStream, WebFX, Web Tonic, LocaliQ, RD Station Panorama de Vendas 2025, Landbase 2026, Data-Mania, MarketJoy, Gartner via agenciatribo.com.br), cruzada com dado real de performance de mídia paga da própria conta (módulos 03 e 09) e com o contexto de negócio do módulo 00. Câmbio USD/BRL de 25/09/2026 (5,20). Nenhuma URL do cliente foi navegada neste módulo, conforme protocolo da metodologia Doutor Carvalho — toda a pesquisa de benchmark foi feita via WebSearch.
