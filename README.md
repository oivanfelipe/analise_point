# Diagnóstico Digital — Point Thermic

Auditoria de aquisição digital da Point Thermic (pointthermic.com.br): contexto de mercado, concorrência, SEO, CRO do site e da landing page de Google Ads, Meta Ads e Google Ads — com dado real de performance das contas de mídia via Windsor.ai.

**Laudo publicado (artefato interativo, com gráficos e capturas reais):**
https://claude.ai/artifact/LDuGb9RV4Z6nGLPtxCxBvY

O HTML fonte desse laudo está em [`laudo/index.html`](laudo/index.html) e pode ser aberto direto no navegador.

## Estrutura do repositório

```
laudo/            Fonte HTML do laudo executivo publicado como artefato, com as imagens de criativo embutidas
notas/            Notas de análise completas por módulo (mais detalhadas que o laudo executivo)
evidencias/       Capturas de tela reais do site da Point Thermic, da landing page e dos concorrentes
dados/            Dados reais exportados via Windsor.ai (Meta Ads e Google Ads) em CSV
```

### `notas/` — módulos de análise

| Arquivo | Conteúdo |
|---|---|
| `00-contexto-mercado.md` | Identidade da empresa, nicho, panorama de mercado, maturidade digital, mapa de dores |
| `01-concorrentes.md` | Filtrovali, Hydratight (BR) e ITP Brasil — portfólio, presença digital, mote criativo, tabela comparativa |
| `02-meta-ads-organico.md` | Meta Ads: campanhas, copy, criativos, funil, audiências. Inclui adendo de correção (24/09) |
| `03-google-ads.md` | Google Ads: campanhas, grupos de anúncio, termos de pesquisa reais, RSAs. Inclui adendo de correção |
| `07-seo-scope.md` | SEO técnico e de conteúdo do site institucional |
| `08-cro-site.md` | CRO do site institucional: inventário de pontos de conversão, scoring, oportunidades |

### `dados/` — dado real de performance (Windsor.ai)

| Arquivo | Conteúdo |
|---|---|
| `meta-ads-campanhas-diario-mar-ago.csv` | Meta Ads, granularidade diária por campanha, 01/03–31/08/2026 |
| `meta-ads-criativos-copy.csv` | Texto completo (body/title) de todos os anúncios ativos do Meta, últimos 2 meses |
| `meta-ads-campanhas-setembro.csv` | Meta Ads, resumo de campanhas de setembro (inclui ativação na feira ROG.e 2026) |
| `google-ads-campanhas-resumo.csv` | Google Ads, resumo por campanha (mar–ago e setembro) |
| `google-ads-grupos-anuncio.csv` | Google Ads, detalhe por grupo de anúncio dentro da campanha mais eficiente |
| `investimento-mensal-meta-vs-google.csv` | Série mensal de investimento, mar–set 2026, os dois canais |

### `evidencias/` — capturas de tela

- `point-thermic/`: home (desktop e mobile), página de certificados (Petrobras/ISO em PDF), landing page usada para Google Ads (`lp.pointthermic.com.br`)
- `concorrentes/`: home da ITP Brasil, home da Filtrovali, Biblioteca de Anúncios do Meta da Filtrovali

## Achados mais críticos

1. **Google Ads não registra conversão desde 15/07/2026** (72 dias, quatro estruturas de campanha diferentes), mesmo com a conta ativa e gastando normalmente. Hipótese mais provável: falha de rastreamento — o formulário da landing page (`lp.pointthermic.com.br`) é `method="get"` sem página de obrigado visível, e o site roda três contêineres GTM distintos.
2. **SEO técnico do site institucional**: zero meta description, H1 incorreto ("Contato") em 100% das páginas, URLs antigas indexadas retornando 404, blog publicado e vazio desde 2023.
3. **CRO**: o selo de fornecedor cadastrado Petrobras (CRC) e a certificação ISO 9001 — o maior ativo de credibilidade da empresa — aparecem só como PDF cru numa página interna, não como selo de confiança na home nem nos anúncios do Meta.
4. **Concorrência**: Filtrovali é a mais madura digitalmente (mídia paga ativa nos dois canais, SEO técnico correto, mote criativo consistente entre site e anúncio). ITP Brasil tem portfólio quase idêntico ao da Point Thermic e o mesmo cadastro Petrobras/ONIP, mas converte pouco disso em resultado digital (site datado, sem CTA na home).
5. **Recozimento e Normalização são serviços reais** da Point Thermic (confirmado pela landing page dedicada) — achado anterior deste diagnóstico que classificava esse grupo de anúncio como erro de segmentação foi corrigido nas notas do módulo de Google Ads.

## Metodologia

Análise baseada na metodologia de diagnóstico consultivo "Doutor Carvalho" (V4 Company — Carvalho & Co.), adaptada para esta sessão: navegação de site e concorrentes via Chromium headless, dados reais de performance via Windsor.ai (não apenas Biblioteca de Anúncios/Transparency Center públicos), e pesquisa de mercado via busca web. Cada achado nas notas é marcado como fato observado, hipótese ou estimativa de terceiros, com fonte e data.

Limitações registradas: Instagram e LinkedIn (cliente e concorrentes) não puderam ser navegados diretamente nesta sessão — bloqueio de acesso não autenticado nas duas plataformas. HypeStat sem dado para os domínios analisados. Google Keyword Planner não acessado (exige login do cliente).
