# MÓDULO 07 — SEO SCOPE (Search, Content, On-Page, Performance, External)

## Limitação estrutural

Sem acesso ao Google Search Console ou ao GA4 do cliente, não há dado real de impressões, cliques, CTR por página ou posição média. A análise combina inspeção técnica direta do site (Chromium headless), pesquisa pública no Google e HypeStat. A API pública do PageSpeed Insights retornou erro de cota excedida no momento da consulta (25/09/2026) — limitação registrada, não foi possível obter Core Web Vitals oficiais nesta sessão. HypeStat não retornou dados para pointthermic.com.br (domínio fora da base).

## 1. Resumo executivo

A Point Thermic tem rastreabilidade técnica básica funcional (HTTPS válido, HTTP/2, robots.txt correto, sitemap referenciado, sem bloqueio de indexação), mas apresenta lacunas estruturais de SEO on-page que colocam o site atrás dos três concorrentes analisados no módulo 01: zero meta description em todas as páginas verificadas, zero dado estruturado (JSON-LD), H1 incorreto e duplicado ("Contato") em todas as páginas internas, e um blog publicado e indexável que está completamente vazio. Some-se a isso um achado técnico concreto: URLs antigas do site (de uma estrutura anterior) seguem indexadas no Google e retornam erro 404 em vez de redirecionamento para a página atual equivalente, desperdiçando equity de SEO já conquistada.

**Nota geral de SEO: 3,5 de 10.** A base técnica de rastreabilidade está correta (o que evita nota ainda mais baixa), mas a ausência quase total de otimização on-page e de estratégia de conteúdo limita fortemente a capacidade do site de capturar demanda orgânica qualificada.

## 2. Visão geral do domínio

Sem ferramenta de SEO conectada (Ahrefs/Semrush) e sem retorno do HypeStat para este domínio — limitação registrada. Observação manual via busca pública ("site:pointthermic.com.br"): o Google tem indexadas tanto páginas da estrutura atual (/certificados/, home) quanto páginas de uma estrutura de URL anterior (ex: /tratamento-termico-alivio-tensao, /pos-aquecimento, /locacao-equip-tratamento-termico, /tratamento-termico-em-rp), sinal de que o site passou por uma reestruturação de URLs sem tratamento adequado de redirecionamento (ver seção 3.1).

## 3. SEO técnico

### 3.1. Rastreabilidade e indexação

**Fato observado:**
- robots.txt acessível e corretamente configurado, referenciando `https://pointthermic.com.br/wp-sitemap.xml`. Único bloqueio é `/wp-admin/` (padrão e correto).
- Sitemap XML existe e está estruturado (index de sitemaps do WordPress, com sub-sitemap de páginas).
- Nenhuma página verificada tem meta robots noindex — páginas estão livres para indexação.
- Canonical tag presente na home (aponta corretamente para si mesma) mas ausente na página de blog verificada — inconsistência de implementação.
- **Achado crítico:** o domínio `www.pointthermic.com.br` redireciona corretamente (301) para `pointthermic.com.br` (boa prática de canonicalização a nível de domínio). Porém, ao consultar `site:pointthermic.com.br` no Google, aparecem URLs de uma estrutura de site anterior (`/tratamento-termico-alivio-tensao`, `/pos-aquecimento`, `/locacao-equip-tratamento-termico`, `/tratamento-termico-em-rp`). Testadas diretamente em 25/09/2026, essas URLs retornam **HTTP 404** (confirmado via requisição direta), sem redirecionamento para a página atual equivalente em `/servicos/`. Isso significa que o Google ainda mantém essas URLs em seu índice — possivelmente com links externos ou histórico de posicionamento associado a elas — e qualquer clique vindo da busca ou de um link antigo cai em uma página de erro, perdendo o valor de SEO acumulado por essas URLs antes da reestruturação.

### 3.2. Velocidade e Core Web Vitals

**Limitação registrada:** PageSpeed Insights indisponível (cota da API excedida no momento da consulta). Observação qualitativa: o carregamento da home via navegador headless completou em poucos segundos até o estado de rede ociosa, sem erros de console registrados. Isso não substitui uma medição formal de Core Web Vitals, que deve ser feita em ferramenta própria (PageSpeed Insights ou GA4/CrUX do cliente) antes de qualquer meta de performance ser fechada.

**Fato observado:** o site carrega um volume grande de scripts de terceiros já no carregamento inicial da home (três contêineres GTM distintos, Google Ads, GA4, Meta Pixel, Microsoft Clarity, Hotjar, sincronização Bing) — carga de terceiros elevada para o padrão do nicho, com potencial de impacto em Total Blocking Time e Time to Interactive. Recomenda-se validação formal.

### 3.3. Mobile-friendliness

**Fato observado:** meta viewport configurada corretamente (`width=device-width, initial-scale=1`). Existe imagem de banner dedicada para mobile (`BANNER-MOBILE-2.png`), indicando algum cuidado com a experiência mobile. Teste de responsividade completa (toque, legibilidade, zoom) não foi validado neste módulo — será aprofundado no módulo de CRO do site.

### 3.4. Arquitetura do site

**Fato observado:** estrutura de URL limpa e hierárquica na versão atual (`/servicos/`, `/sobre/`, `/clientes-e-projetos/`, `/certificados/`), sem parâmetros. Profundidade de clique baixa: todas as páginas principais estão a um clique da home, via menu principal. Não há breadcrumbs em nenhuma página verificada. Navegação principal é clara e enxuta (7 itens).

### 3.5. HTTPS e segurança

**Fato observado:** HTTPS ativo em todas as páginas, servido via Cloudflare, com HTTP/2 habilitado. Certificado SSL válido, emitido para `pointthermic.com.br`, com validade até 30/11/2026. Nenhum aviso de mixed content foi capturado no console durante a navegação.

## 4. SEO on-page

### 4.1. Títulos e meta descriptions

**Fato observado (5 páginas verificadas: home, serviços, sobre, clientes e projetos, blog):**
- Title tags existem e são únicos por página (ex: "Serviços – Point Thermic", "Sobre Nós – Point Thermic"), seguindo um padrão consistente de "Página – Point Thermic". O title da home, porém, é apenas "Point Thermic", sem palavra-chave de serviço — oportunidade perdida no title mais importante do site.
- **Meta description: ausente em 100% das páginas verificadas (5 de 5).** Isso é um problema técnico direto: sem meta description, o Google gera automaticamente um trecho a partir do conteúdo da página para exibir no resultado de busca, o que reduz o controle sobre a taxa de clique (CTR) e a mensagem que aparece para quem está pesquisando.

### 4.2. Heading structure

**Fato observado:** em todas as 5 páginas verificadas, o único H1 encontrado é "Contato" — na prática, o rótulo de um formulário de rodapé compartilhado por todas as páginas, não um H1 de conteúdo principal da página. Isso significa que, tecnicamente, nenhuma página do site tem um H1 que descreva o conteúdo real daquela página (ex: a página de Serviços deveria ter H1 como "Serviços de Tratamento Térmico e Limpeza Química Industrial", não "Contato"). H2 são usados de forma extensa e com bom conteúdo semântico (nomes de serviços, setores atendidos), mas sem um H1 correto acima deles, a hierarquia de heading está tecnicamente quebrada em todo o site.

### 4.3. Conteúdo das páginas principais

**Fato observado:** as páginas de Serviços e Sobre Nós têm conteúdo textual substancial e tecnicamente específico (nomes de processos, normas, benefícios técnicos de cada serviço), o que é positivo para relevância de busca em termos técnicos do nicho. A página de Clientes e Projetos, por outro lado, tem quase nenhum texto — apenas uma frase de abertura e uma grade de logos, sem nomear os projetos, os resultados obtidos ou o contexto de cada cliente, o que é ao mesmo tempo uma lacuna de SEO (página praticamente sem texto indexável) e de prova social (ver módulo de CRO).

### 4.4. Imagens

**Fato observado:** todas as imagens inspecionadas na home (banner e ícones de serviço) têm atributo `alt` vazio. Isso é uma lacuna de acessibilidade e de SEO de imagem (o Google usa o alt text para entender e indexar imagens, inclusive para a busca de imagens do Google).

### 4.5. Schema markup

**Fato observado:** nenhuma página verificada tem dado estruturado (JSON-LD). Para uma empresa de serviço local B2B com endereço físico, os tipos de schema mais relevantes e ausentes são Organization/LocalBusiness (nome, endereço, telefone, área de atuação) e Service (para cada linha de serviço). A ausência desses dados reduz a chance de aparecer em rich results e painéis de conhecimento do Google, e é uma prática básica que os concorrentes Filtrovali (tem JSON-LD) já implementam.

## 5. Estratégia de conteúdo

### 5.1. Blog e conteúdo editorial

**Fato observado:** existe uma seção de Blog publicada, presente no menu principal e no sitemap, com uma frase de boas-vindas ("Nosso blog oferece informações atualizadas sobre tendências e tecnologias relacionadas ao tratamento térmico, construção naval, limpeza química e muito mais") — mas **zero artigos publicados** ("It seems we can't find what you're looking for"). Última modificação registrada no sitemap para essa página é de novembro de 2023, indicando abandono de longa data, não uma iniciativa recente ainda em construção.

### 5.2. Content gaps

Sem ferramenta de pesquisa de palavra-chave conectada — análise manual via pesquisa pública. Termos técnicos centrais do negócio (ex: "alívio de tensões localizado", "flushing hidráulico industrial", "o que é passivação de tubulação") são exatamente o tipo de busca de cauda longa que um engenheiro de manutenção faz antes de contratar um fornecedor, e é um espaço de conteúdo hoje vazio no site, tanto para a Point Thermic quanto, nas evidências coletadas, para os três concorrentes analisados — nenhum deles demonstrou uma estratégia de blog robusta e ativa. Isso é lido como janela de oportunidade compartilhada, não como desvantagem competitiva isolada.

### 5.3. Internal linking

**Fato observado:** a navegação principal linka as páginas entre si de forma direta, mas não há links internos contextuais dentro do corpo de texto das páginas (ex: a página de Serviços não linka para Certificados ou para Clientes e Projetos no meio do texto). Isso é esperado dado o volume pequeno de páginas do site atualmente, mas se tornará relevante assim que o blog for ativado.

## 6. Perfil de backlinks

**Limitação registrada:** sem ferramenta de SEO conectada e sem retorno do HypeStat para o domínio, não há dado quantitativo de backlinks disponível nesta sessão. Sinal indireto observado: as URLs antigas indexadas pelo Google (seção 3.1) sugerem que o site teve alguma atividade de indexação/linking no passado que não foi preservada na migração de estrutura.

## 7. SEO local

**Fato observado:** o site declara endereço físico completo (Rua Tarauacá, 127, Cotia – SP) com link para Google Maps embutido no rodapé, o que é positivo para SEO local. Não foi possível confirmar diretamente, nesta sessão, se existe Perfil da Empresa no Google (Google Business Profile) ativo, número de avaliações ou nota — pesquisa pública não retornou esse dado específico. Recomenda-se verificação direta pelo cliente (login na própria conta) como próximo passo, já que é um ativo de baixo custo e alto potencial para um negócio B2B regional que também atende presencialmente fornecedores/compradores da região de Cotia/Grande São Paulo.

## 8. SEO SCOPE Score

| Dimensão | O que avalia | Nota |
|---|---|---|
| Search (Rastreabilidade) | Indexação, robots, sitemap, canonical, duplicatas | 6/10 — base técnica correta, mas com URLs antigas indexadas retornando 404 |
| Content (Conteúdo) | Blog, content gaps, qualidade, cobertura de tópicos | 2/10 — blog publicado e vazio, zero conteúdo de cauda longa |
| On-Page (Otimização) | Titles, metas, headings, schema, imagens, conteúdo | 2/10 — zero meta description, zero schema, H1 incorreto em 100% das páginas |
| Performance (Técnico) | Velocidade, Core Web Vitals, mobile, HTTPS, arquitetura | 6/10 — HTTPS/HTTP2 corretos, viewport mobile correto, mas Core Web Vitals não medidos e carga de terceiros elevada |
| External (Autoridade) | Backlinks, DR, domínios referentes, menções | Não avaliável — sem dado disponível nesta sessão (limitação registrada) |

**Nota geral (média das quatro dimensões avaliáveis): 4,0/10**, ponderada para baixo (3,5/10) pelo peso estrutural do On-Page e do Content, que são as duas dimensões com maior controle direto do cliente e maior retorno esperado em curto prazo.

## 9. Oportunidades

1. **Corrigir o H1 de cada página** (problema: todas as páginas usam "Contato" como H1; impacto: alto, é o sinal de relevância de conteúdo mais direto para o Google; facilidade: alta, ajuste de template; prioridade: máxima; resultado esperado: melhora de relevância de página para os termos que ela deveria representar).
2. **Escrever meta description única para cada página** (problema: 100% ausente; impacto: alto para CTR em busca; facilidade: alta; prioridade: máxima; resultado esperado: mais cliques por posição equivalente no ranking).
3. **Otimizar o title da home** para incluir o serviço principal, não só o nome da marca (impacto: médio-alto; facilidade: alta; prioridade: alta).
4. **Implementar redirecionamento 301 das URLs antigas indexadas** (`/tratamento-termico-alivio-tensao`, `/pos-aquecimento`, `/locacao-equip-tratamento-termico`, `/tratamento-termico-em-rp`) para as páginas atuais equivalentes (impacto: alto, recupera equity de SEO já indexado; facilidade: alta, mudança de configuração de servidor/CMS; prioridade: máxima).
5. **Implementar schema Organization/LocalBusiness e Service** em JSON-LD (impacto: médio-alto; facilidade: média; prioridade: alta).
6. **Preencher alt text descritivo em todas as imagens** (impacto: médio; facilidade: alta; prioridade: média).
7. **Ativar o blog com pauta técnica de cauda longa** ligada aos serviços centrais (alívio de tensões, flushing hidráulico, passivação, decapagem) (impacto: alto no médio prazo; facilidade: média, exige produção de conteúdo; prioridade: alta).
8. **Reescrever a página de Clientes e Projetos com texto real** (contexto de cada projeto, setor, resultado), não apenas logos (impacto: médio, ajuda SEO e prova social; facilidade: média; prioridade: alta).
9. **Adicionar canonical tag em todas as páginas**, incluindo o blog (impacto: baixo-médio, mas evita duplicidade futura; facilidade: alta; prioridade: média).
10. **Medir Core Web Vitals formalmente** via PageSpeed Insights/GA4 assim que possível e priorizar a redução de scripts de terceiros não essenciais (impacto: médio-alto em experiência e ranking; facilidade: média; prioridade: alta).
11. **Auditar e ativar o Perfil da Empresa no Google (Google Business Profile)**, se ainda não estiver otimizado, incluindo categoria de serviço, área de atendimento e fotos de projetos (impacto: médio-alto para SEO local; facilidade: alta; prioridade: alta).
12. **Adicionar breadcrumbs** ao site (impacto: baixo-médio, ajuda navegação e rich results; facilidade: média; prioridade: baixa-média).
13. **Criar página dedicada por serviço** (hoje todos os serviços estão agrupados em uma única página `/servicos/`), seguindo o padrão observado na Hydratight (BR), que segmenta por serviço para capturar buscas mais específicas (impacto: alto no médio prazo; facilidade: média; prioridade: alta).
14. **Adicionar prova social ativa** (depoimentos, números de projetos executados, cases nomeados) nas páginas de conteúdo, não apenas como logos (impacto: médio, apoia SEO e conversão; facilidade: média; prioridade: média).
15. **Revisar consistência de NAP** (nome, endereço, telefone) entre site, Google Business Profile e redes sociais, já que o site usa dois e-mails de contato distintos em pontos diferentes (`comercial@pointthermic.com.br` visível e `contato@pointthermic.com.br` no link mailto real) — pequena inconsistência que vale padronizar (impacto: baixo-médio; facilidade: alta; prioridade: média).

## 10. Quick wins (até 30 dias)

Corrigir H1 por página (1), escrever meta descriptions (2), otimizar title da home (3), redirecionar 301 as URLs antigas indexadas (4), preencher alt text (6), adicionar canonical no blog (9), padronizar e-mail de contato (15). Nenhuma dessas ações depende de produção de conteúdo novo — são ajustes técnicos e de template, executáveis rapidamente.

## 11. Argumentos para a reunião

O que observamos: o site tem uma base técnica funcional, mas está tecnicamente "invisível" para o Google em quase todos os critérios de otimização on-page que dependem de configuração, não de conteúdo novo — meta description, H1, schema. O impacto disso é direto: cada real investido em mídia paga hoje carrega sozinho o peso de gerar demanda, porque o canal orgânico está desativado tecnicamente, não por falta de conteúdo relevante (o conteúdo técnico que existe no site é bom). Empresas com SEO maduro no mesmo nicho, como a Filtrovali, já resolveram o básico (meta description única, dados estruturados) e ainda somam mídia paga simultânea em dois canais. O ganho esperado ao corrigir os itens técnicos listados como quick win é de curto prazo e baixo custo de implementação, e cria a base necessária para que qualquer investimento futuro em conteúdo (blog) tenha efeito.

Fonte e método: inspeção direta do site via Chromium headless em 25/09/2026 (home, serviços, sobre, clientes e projetos, blog), robots.txt e sitemap consultados via requisição direta, verificação de redirecionamento e status HTTP das URLs antigas via requisição direta, pesquisa pública no Google (site:pointthermic.com.br), certificado SSL verificado via requisição TLS direta. PageSpeed Insights indisponível por cota de API excedida — limitação registrada. HypeStat sem dado para o domínio — limitação registrada.
