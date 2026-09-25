# MÓDULO 03 — GOOGLE ADS

## Fontes e método

Diferente da metodologia padrão (que usa apenas o Google Ads Transparency Center, sem métricas), esta análise teve acesso a **dados reais de performance via Windsor.ai**, conectado à conta Google Ads "Point Thermic" (ID 761-300-6526), cobrindo 01/03/2026 a 31/08/2026. Isso inclui campanha, grupo de anúncio, termos de pesquisa reais que geraram clique, texto completo dos anúncios (Responsive Search Ads), investimento, cliques, impressões, conversões e parcela de impressões. Google Keyword Planner não foi utilizado (exigiria login do cliente em conta própria do Google Ads, não disponível nesta sessão) — os termos de pesquisa reais que geraram clique substituem parcialmente essa lacuna, com a vantagem de serem dado real, não estimativa de ferramenta.

## 1. Resumo executivo

**CORREÇÃO (25/09/2026):** a leitura original deste módulo — de que a conta estava pausada desde 31/08 — estava incorreta. O campo `campaign_status` retornado pela API se mostrou não confiável (aparece como "PAUSED" inclusive em campanhas com gasto registrado nos dias seguintes à consulta) e o corte de dado usado não cobria setembro. Nova consulta confirma que a conta segue ativa, com duas campanhas novas lançadas em 04/09 ("Search- 04/09" e "Performance Max- 04/09 L.Q."), somando R$ 511,45 até 25/09.

**O achado real e mais urgente, revisado: zero conversão rastreada por 72 dias corridos (desde 15/07/2026), em quatro estruturas de campanha diferentes**, incluindo as duas lançadas em 04/09. Esse padrão — zero persistente mesmo trocando campanha, palavra-chave e até o tipo de campanha (Search e Performance Max) — é mais compatível com uma falha de rastreamento de conversão (possivelmente ligada aos três contêineres GTM identificados no módulo de contexto, ou à migração de URL identificada no módulo de SEO) do que apenas com tráfego mal segmentado. Recomenda-se verificar se a tag de conversão dispara corretamente na thank-you page atual antes de qualquer outro ajuste. O investimento total do período (01/03–25/09) é R$ 7.492,04, não R$ 6.980,59.

No período em que esteve ativa, a conta teve investimento total de R$ 6.980,59 e gerou aproximadamente 63 conversões rastreadas, mas de forma muito desigual entre campanhas. A campanha historicamente mais eficiente da conta ("Search I CPC I Auto I Tratamento Termico", com custo por conversão de R$ 68,94) foi substituída em 16/07/2026 por duas campanhas novas ("[Search] Tratamento térmico" e "[Search] Limpeza Quimica") que, juntas, gastaram R$ 1.580,88 e **não registraram uma única conversão** até a pausa em 31/08. A análise de termos de pesquisa reais explica o motivo: essas campanhas capturaram buscas fora do escopo do negócio, incluindo "empresa que limpa piso encardido", "empresas de tratamento de água" e, mais relevante, uma família de buscas por "têmpera", "revenimento" e "tratamento térmico de metais" — termos de um segmento adjacente e diferente (tratamento térmico metalúrgico em forno, para dureza e usinabilidade) que não é o serviço que a Point Thermic presta (alívio de tensões localizado pós-solda). Esta é exatamente a hipótese de ambiguidade semântica do nome/categoria levantada no módulo de contexto (módulo 00), agora confirmada com dado real de busca.

**Nota geral de maturidade de captura de demanda: 5,5/10.** A conta tem evidência de sofisticação real (RSAs bem escritos para o serviço correto, uso de certificação ISO 9001 e ONIP na copy, uma campanha historicamente eficiente), mas perde muitos pontos pela pausa atual, pela troca de uma campanha eficiente por outras que não convertem, e por um problema de correspondência de palavra-chave não corrigido que já era prevísivel dado o nome da categoria de serviço.

## 2. Panorama das campanhas (dado real, não apenas observável publicamente)

| Campanha | Tipo | Status | Investimento (6m) | Impressões | Cliques | CTR | CPC médio | Conversões | Custo/Conversão | Parcela de impressões (Search) |
|---|---|---|---|---|---|---|---|---|---|---|
| Search I CPC I Auto I Tratamento Termico | Search | Pausada | R$ 3.745,86 | 22.171 | 2.679 | 12,08% | R$ 1,40 | 54,33 | **R$ 68,94** | 11,14% |
| [Performance] Limpeza Química Industrial | Search | Pausada | R$ 719,04 | 4.237 | 677 | 15,98% | R$ 1,06 | 5 | R$ 143,81 | 34,79% |
| Search I CPC I Auto I Branding | Search | Pausada | R$ 470,77 | 3.390 | 340 | 10,03% | R$ 1,38 | 1,67 | R$ 282,47 | 100,6% |
| P.Max I Auto I Point Thermic | Performance Max | Pausada | R$ 464,04 | 41.737 | 1.575 | 3,77% | R$ 0,29 | 2 | R$ 232,02 | 12,68% |
| [Search] Tratamento térmico | Search | Pausada | R$ 833,41 | 4.167 | 514 | 12,34% | R$ 1,62 | **0** | N/D | 21,04% |
| [Search] Limpeza Quimica | Search | Pausada | R$ 747,47 | 5.564 | 582 | 10,46% | R$ 1,28 | **0** | N/D | 42,19% |

Todas as campanhas são de Search ou Performance Max automatizado — não há Display nem Vídeo. A parcela de impressões da campanha de marca é de praticamente 100% (cobertura total de quem busca "Point Thermic" diretamente), enquanto a campanha historicamente mais forte de captura de categoria ("Tratamento Termico") tem parcela de impressões de apenas 11,14% — ou seja, a conta está perdendo cerca de 89% das impressões disponíveis para esse termo por limitação de orçamento ou de ranking, mesmo sendo a campanha mais eficiente da conta.

## 3. Mensagens e ofertas nos anúncios (dado real de RSA)

**Fato observado — grupo de anúncio "Alívio de Tensões" (o mais eficiente da conta, R$ 41 por conversão):**

> Headlines: "Alívio de Tensão em Metais | Alívio de Tensões Pós-Soldagem | Tratamento Térmico de Tensão | Prevenção de Trincas e Falhas | Estabilidade Dimensional Total | Conformidade Normas ASME ASTM | Point Thermic: Alívio Térmico | Controle de Tensões Residuais | Especialistas em Vasos Pressão"
> Descrições: "Reduza tensões internas de soldagem ou usinagem. Conformidade com normas ASME e ASTM. | Evite deformações em estruturas soldadas de grande porte. [...] Especialistas em vasos de pressão e caldeiras."

Esta é a copy mais tecnicamente precisa e mais alinhada ao serviço real da empresa encontrada em toda a análise (incluindo os módulos de Meta Ads e CRO): cita normas técnicas específicas (ASME, ASTM), nomeia o ativo crítico do comprador (vasos de pressão, caldeiras) e comunica o benefício correto do processo. É também, não coincidentemente, o grupo de anúncio com melhor custo por conversão da conta inteira.

**Achado crítico — grupo de anúncio "Recozimento e Normalização" (o menos eficiente da campanha, R$ 248 por conversão, quase 6 vezes mais caro que "Alívio de Tensões"):**

> Headlines: "Recozimento de Metais e Aço | Normalização de Peças de Aço | Facilite a Usinagem de Peças | Recozimento para Ductilidade | Redução de Dureza Industrial | Recozimento e Normalização | Precisão em Ciclos Térmicos"
> Descrições: "Melhore a usinabilidade e reduza a dureza do aço. Recozimento com resfriamento controlado. [...] Atendimento aeroespacial e automotivo."

Este grupo de anúncio promove **um serviço que a Point Thermic não presta**: recozimento e normalização são processos de tratamento térmico em forno, para alterar dureza e usinabilidade de metal bruto — um segmento diferente (identificado no módulo 01 como o segmento de empresas como COOPERTRATT e INDUSTRAT), distinto do alívio de tensões localizado pós-solda que é o negócio real da empresa. É provável que este grupo de anúncio tenha sido gerado de forma automática (o nome da campanha inclui "Auto") a partir de uma interpretação ampla demais do termo "tratamento térmico", sem validação contra o portfólio real de serviço.

**Achado positivo:** ao contrário do que foi observado no Meta Ads (módulo 02), aqui a certificação da empresa **é usada como argumento de venda**: o grupo de anúncio de Limpeza Química cita explicitamente "Padrão de Qualidade ISO 9001", "Registro ONIP Setor Petróleo" e "Certificação NBR ISO 9001:2015" nos headlines. Esta é uma inconsistência de canal a corrigir: o Google Ads já usa o ativo de credibilidade mais forte da empresa, o Meta Ads ainda não.

## 4. Coerência entre anúncio, intenção e destino

**Achado crítico, com evidência de termo de pesquisa real:** a campanha "[Search] Tratamento térmico" (a que substituiu a campanha eficiente e não converteu nada) tem anúncios com copy correta ("Tratamento Térmico Localizado", "Laudo Técnico Certificado"), mas os termos de pesquisa reais que geraram clique nela incluem: "empresa que limpa piso encardido", "empresas de tratamento de água", "tempera e revenimento", "tratamento termico de metais", "têmpera por indução", além de buscas por marca de concorrentes ("hotwork brasil engenharia térmica", "grefortec portão", "mxt tratamento termico"). Ou seja, **o problema não está na copy do anúncio, e sim na configuração de palavra-chave** (provável uso de correspondência ampla sem lista de termos negativos suficiente), que permite que o Google exiba o anúncio para buscas fora do escopo real do negócio. Isso confirma, com dado real, a hipótese levantada no módulo de contexto sobre o risco de ambiguidade do termo "tratamento térmico" nesse nicho.

A campanha historicamente eficiente, por outro lado, mostra termos como "empresas de soldagem industrial" e "metalúrgica" — mais próximos do público correto, ainda que genéricos, e convertendo (2 conversões cada).

## 5. Landing pages

**Fato observado:** os anúncios de Search não usam campo de URL de destino específico por página nos dados coletados (destino registrado de forma padrão para o domínio); presume-se, com base no módulo de CRO, que o destino seja a home ou a página de Serviços do site, não uma landing page dedicada por grupo de anúncio (ex: uma LP específica só para "Alívio de Tensões" ou só para "Limpeza Química"). Isso significa que alguém que clica no anúncio de "Alívio de Tensões Pós-Soldagem" muito provavelmente cai na mesma página genérica de Serviços que lista todos os quatro serviços, sem reforço de mensagem específica daquele anúncio — perda de "message match" entre anúncio e destino, um dos fatores que mais afeta taxa de conversão em Search.

## 6. Estrutura do site e SEO aparente

Já coberto em profundidade no módulo de SEO SCOPE (módulo 07): ausência de meta description, H1 incorreto e ausência de páginas de serviço dedicadas são lacunas que afetam tanto o SEO orgânico quanto o Quality Score potencial das campanhas de Search (a relevância da landing page é um dos três pilares do Quality Score do Google Ads).

## 7. Arquitetura de captura de demanda

**Fato observado:** a conta cobre bem a captura de marca (100% de parcela de impressões na campanha de Branding) e parcialmente a captura de categoria/serviço (Search e Performance Max), mas não há nenhuma campanha de captura de concorrente (ex: quem busca "Hydratight" ou "Filtrovali" diretamente) nem de conteúdo de topo de funil. A cobertura de categoria é limitada pela baixa parcela de impressões (11% a 42% conforme a campanha), o que indica orçamento ou lances insuficientes para capturar toda a demanda disponível nos termos certos — especialmente relevante porque a campanha com maior parcela de impressões disponível perdida é justamente a mais eficiente (Alívio de Tensões/Tratamento Térmico).

### 7.2. Mapa de palavras-chave estratégicas (a partir de termos de pesquisa reais, não do Keyword Planner)

**Fonte:** termos de pesquisa reais que geraram clique na conta, 01/03 a 31/08/2026 (dado direto da conta, não estimativa de ferramenta de terceiros — mais confiável que uma pesquisa de volume). Sem Keyword Planner conectado, não há volume de busca mensal nem dificuldade de SEO (SD/KD) disponíveis — campos marcados "N/D".

| Cluster | Termo observado | Cliques | Conversões | Intenção | Observação |
|---|---|---|---|---|---|
| CORE (correto) | alívio de tensão pós-soldagem / alívio de tensão em metais | Alto (grupo com 753 cliques) | 7 | C | Melhor custo por conversão da conta — cluster a priorizar e expandir |
| CORE (correto) | tratamento térmico localizado / tratamento térmico industrial | Alto (grupo com 1.612 cliques) | 46,33 | C | Maior volume e maior número absoluto de conversões da conta |
| CORE (correto) | limpeza química industrial / passivação de inox / flush tubulações | 677 (grupo) | 5 | C | Bom desempenho, custo por conversão moderado |
| RUÍDO / SEGMENTO ERRADO | têmpera, revenimento, recozimento, normalização, tratamento térmico de metais | 293+ (grupo Recozimento) + buscas soltas | 1 | C (mas do segmento errado) | Cluster a excluir via termos negativos — é o segmento de tratamento térmico metalúrgico em forno, não o serviço da Point Thermic |
| RUÍDO / FORA DE ESCOPO | empresa que limpa piso encardido, produto de limpeza desengraxante, empresas de tratamento de água | Baixo (1 clique cada) | 0 | C/I, mas fora de nicho | Termos negativos óbvios ainda não bloqueados |
| MARCA/CONCORRENTE | point thermic, hotwork brasil engenharia térmica, grefortec portão, mxt tratamento termico | Baixo | 0 | N | Buscas de marca própria e de concorrentes capturadas incidentalmente — oportunidade de campanha de marca própria já existe (Branding), mas não há campanha deliberada de captura de concorrente |
| CAUDA LONGA (não observada nos dados, mas coerente com o negócio) | flushing hidráulico industrial, teste hidrostático empresa, passagem de pig tubulação | N/D | N/D | C | Termos do portfólio de serviço que não aparecem nos termos de pesquisa reais coletados — possível lacuna de cobertura de palavra-chave, a validar com Keyword Planner |

### Quick Win SEO

Sem dado de SD/KD desta sessão (Keyword Planner não acessado). A recomendação direta, porém, é clara pelo próprio dado de Google Ads: os termos do cluster CORE correto ("alívio de tensão pós-soldagem", "tratamento térmico localizado", "flushing hidráulico") são os mesmos que deveriam virar páginas de serviço dedicadas no site (oportunidade já registrada no módulo de SEO) — o Google Ads já provou que esses termos convertem.

### Prioridade Google Ads

**Ação imediata, sem custo de mídia adicional:** adicionar termos negativos para o cluster de ruído ("têmpera", "revenimento", "recozimento", "normalização", "piso", "água", quando não acompanhados de termos do core do negócio) e pausar ou reestruturar o grupo de anúncio "Recozimento e Normalização". Isso por si só deve reduzir o custo por conversão médio da conta, já que esse grupo custa quase 6 vezes mais por conversão que o grupo mais eficiente.

### Hub de conteúdo de marca ou comparativo

Buscas por nomes de concorrentes (Hotwork, Grefortec, MXT) já aparecem incidentalmente na conta. Isso sugere espaço para uma campanha de captura de concorrente deliberada e/ou conteúdo comparativo no site, mas o volume observado é pequeno demais nesta amostra para dimensionar o cluster com confiança — registrado como oportunidade a validar, não como prioridade imediata.

## 8. Copy Score e Landing Score

| Item | Nota |
|---|---|
| Copy — grupo Alívio de Tensões / Tratamento Térmico | 8,5/10 — tecnicamente precisa, cita normas, nomeia ativo crítico |
| Copy — grupo Recozimento e Normalização | 2/10 — copy competente, mas para o serviço errado |
| Copy — grupo Limpeza Química | 7,5/10 — usa certificação real como argumento |
| Landing page (destino) | 4/10 — provavelmente página genérica de Serviços, sem message match por grupo de anúncio (ver módulo de CRO) |

## 9. Benchmark de maturidade

| Dimensão | Nota |
|---|---|
| Cobertura de demanda | 5/10 — boa cobertura de marca, cobertura de categoria limitada por parcela de impressões baixa |
| Qualidade das landing pages | 4/10 |
| Coerência de mensagem (anúncio x serviço real) | 6/10 — puxada para baixo pelo grupo Recozimento e Normalização |
| Ofertas | 4/10 — apenas orçamento direto, sem oferta de topo/meio de funil |
| Provas usadas na copy | 7/10 — certificação ISO/ONIP já aparece nos anúncios |
| Captura de conversão | 5/10 — conta pausada agora; quando ativa, resultado concentrado em poucos grupos de anúncio |
| **Nota geral: 5,5/10** |

## 10. Oportunidades

1. **Diagnosticar e resolver a pausa simultânea de Google Ads e Meta Ads** (problema: zero investimento pago há 25 dias em ambos os canais; impacto: crítico; facilidade: depende da causa; prioridade: máxima).
2. **Reativar a campanha "Search I CPC I Auto I Tratamento Termico" ou recriar sua estrutura vencedora**, historicamente a mais eficiente da conta (R$ 68,94/conversão) (impacto: alto; facilidade: fácil assim que a pausa geral for resolvida; prioridade: máxima).
3. **Pausar/reestruturar definitivamente o grupo de anúncio "Recozimento e Normalização"**, que promove um serviço fora do portfólio real da empresa e tem o pior custo por conversão da conta (impacto: alto; facilidade: fácil; prioridade: máxima).
4. **Adicionar lista de termos negativos** para o cluster de ruído identificado (têmpera, revenimento, recozimento, normalização, piso, água, limpeza doméstica) nas campanhas de "Tratamento Térmico" e "Limpeza Química" (impacto: alto, reduz desperdício direto; facilidade: fácil; prioridade: máxima).
5. **Investigar por que "[Search] Tratamento térmico" e "[Search] Limpeza Quimica" tiveram zero conversões** mesmo com copy correta — provável causa raiz já identificada (correspondência de palavra-chave), mas vale confirmar se há também problema de rastreamento de conversão nessas duas campanhas especificamente (impacto: alto; facilidade: média; prioridade: alta).
6. **Aumentar orçamento/lance na campanha de melhor desempenho** para capturar mais da parcela de impressões hoje perdida (apenas 11% capturado no melhor cluster) (impacto: alto; facilidade: fácil, decisão de investimento; prioridade: alta).
7. **Criar landing pages dedicadas por grupo de anúncio** (Alívio de Tensões, Limpeza Química, Flushing), em vez de direcionar todo o clique para a página genérica de Serviços (impacto: alto, melhora Quality Score e taxa de conversão; facilidade: média; prioridade: alta, compartilhada com o módulo de CRO e SEO).
8. **Levar o padrão de copy do grupo "Alívio de Tensões" para os demais grupos de anúncio**, replicando a citação de normas técnicas (ASME/ASTM) e ativos críticos (vasos de pressão) (impacto: médio-alto; facilidade: fácil; prioridade: alta).
9. **Trazer o uso de ISO 9001/ONIP do Google Ads para o Meta Ads**, corrigindo a inconsistência de canal identificada (impacto: médio-alto; facilidade: fácil; prioridade: alta, compartilhada com o módulo 02).
10. **Criar campanha deliberada de captura de concorrente**, aproveitando o sinal já existente de buscas por nomes como Hotwork e Grefortec (impacto: médio, a validar volume; facilidade: média; prioridade: média).
11. **Executar pesquisa formal no Google Keyword Planner** (com login do cliente) para validar volume e dificuldade dos termos de cauda longa do portfólio completo (flushing hidráulico, teste hidrostático, passagem de pig), hoje não capturados nos dados observados (impacto: médio, completude do diagnóstico; facilidade: fácil para o cliente; prioridade: média).
12. **Revisar a campanha Performance Max**, que tem a maior quantidade de impressões da conta (41.737) mas o segundo pior custo por conversão (R$ 232,02) e parcela de impressões baixa — validar se os ativos automáticos usados nela têm o mesmo problema de mensagem incorreta identificado na campanha de Search (impacto: médio-alto; facilidade: média; prioridade: alta).

## 11. Quick wins (até 30 dias)

Resolver a pausa da conta (1), pausar/corrigir o grupo Recozimento e Normalização (3), adicionar termos negativos (4), replicar o padrão de copy vencedor nos demais grupos (8), trazer ISO/ONIP para o Meta Ads (9).

## 12. Argumentos para a reunião

O que observamos: a conta de Google Ads já provou, com dado real, que sabe fazer o básico bem — o grupo de anúncio certo (Alívio de Tensões, citando normas técnicas) tem o melhor custo por conversão da conta inteira. O problema não é falta de conhecimento de como anunciar bem; é falta de governança na expansão automática de palavras-chave e grupos de anúncio, que introduziu um serviço errado (recozimento/normalização) na mesma campanha do serviço certo, além da conta estar parada agora nos dois canais pagos simultaneamente. O impacto disso é direto: o dinheiro que hoje se perde no grupo errado (quase 6 vezes o custo por conversão do grupo certo) poderia estar financiando mais volume no grupo que já funciona. O que normalmente se faz nesse ponto é uma limpeza de conta (termos negativos, pausa de grupo errado) antes de qualquer aumento de orçamento, e criação de landing pages dedicadas para capturar o ganho de relevância que a copy já entrega. O ganho esperado é reduzir o custo por conversão médio da conta e liberar orçamento para aumentar a captura da demanda de categoria, hoje capturada em apenas 11% a 42% das impressões disponíveis, a depender da campanha.

Fonte e método: dados de performance via Windsor.ai (API do Google Ads), conta 761-300-6526, período 01/03/2026 a 31/08/2026, incluindo campanha, grupo de anúncio, termos de pesquisa reais, texto completo dos Responsive Search Ads, investimento, cliques, impressões, CTR, CPC, conversões, custo por conversão e parcela de impressões. Google Keyword Planner não acessado nesta sessão (exige login do cliente) — limitação registrada.
