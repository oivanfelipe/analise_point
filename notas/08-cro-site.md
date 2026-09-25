# MÓDULO 08 — CRO DO SITE PRINCIPAL

## Contexto quantitativo (HypeStat)

**Limitação registrada:** HypeStat não retornou dados para pointthermic.com.br (domínio fora da base pública). Não há bounce rate, tempo de visita ou páginas por visita estimados disponíveis nesta sessão.

## Navegação realizada

Site navegado via Chromium headless em 25/09/2026: Página inicial, Sobre Nós, Serviços, Clientes e Projetos, Certificados, Venda e Locação de Equipamentos, Contato (formulário de orçamento) e Blog.

## 1. Primeira impressão e proposta de valor

**Fato observado (screenshot desktop e mobile da home):** em cinco segundos, o visitante entende que é uma empresa de tratamento térmico e limpeza química industrial — a headline "Bem-vindo a Point Thermic!" é fraca isoladamente (fala da marca, não do benefício), mas a linha logo abaixo, "LÍDER NACIONAL EM TRATAMENTO TÉRMICO E LIMPEZA QUÍMICA", cumpre a função de comunicar o que a empresa faz. Ainda assim, é uma afirmação de categoria (o que a empresa é) e não uma proposta de valor orientada a benefício para quem está decidindo contratar (ex: reduzir tempo de parada, evitar falha em ativo crítico).

**Achado crítico (visual, confirmado por screenshot desktop e mobile):** ao lado da headline, no espaço mais nobre da página — a primeira dobra —, há uma caixa com borda laranja completamente vazia, sem imagem, vídeo ou conteúdo. O mesmo espaço vazio aparece tanto no desktop quanto no mobile, o que indica que não é um problema pontual de carregamento, mas um elemento de layout quebrado ou mal configurado (provável imagem ou vídeo que não foi preenchido). É o primeiro elemento visual que o site "promete" ao visitante logo abaixo da headline, e entrega um vazio — prejudica diretamente a primeira impressão.

## 2. Arquitetura de conversão do site

**Fato observado:** a conversão principal (Solicitar Orçamento) está a um clique de distância da home, com CTA visualmente forte (botão verde sobre imagem escura) logo na primeira rolagem. A página de destino desse CTA (`/contato-2/`) tem um formulário razoável (nome completo, telefone, e-mail empresarial, assunto, mensagem) — mais completo do que o formulário secundário do rodapé (que só pede nome e e-mail e é, na prática, uma captura de newsletter, não de orçamento).

**Fato observado:** as páginas de Serviços e Venda e Locação de Equipamentos têm CTA "Solicitar Orçamento" no topo, mas terminam sem CTA de fechamento — a página de Serviços termina com o texto genérico "Clique aqui" seguido diretamente do rodapé/newsletter, sem reforçar a chamada para orçamento ao final do conteúdo, exatamente no ponto em que o visitante acabou de ler todos os detalhes técnicos e está mais propenso a agir.

**Hipótese:** o site depende de um único caminho de conversão de intenção alta (o formulário de orçamento) e de um único caminho de baixa intenção (newsletter), sem conversões intermediárias (ex: baixar material técnico, falar direto no WhatsApp a partir da página de serviço, agendar uma ligação). Isso concentra toda a conversão em quem já está pronto para pedir orçamento, sem capturar quem ainda está pesquisando.

## 3. Navegação e usabilidade

**Fato observado:** menu principal claro e com labels descritivos (Sobre Nós, Serviços, Clientes e Projetos, Certificados, Venda e Locação, Contato). Não há busca interna (esperado, dado o volume pequeno de páginas). Não há breadcrumbs em nenhuma página. Menu mobile funciona via ícone hambúrguer (confirmado em screenshot mobile). Rodapé é aproveitado para links sociais, endereço, contato e newsletter — mas não repete o CTA de orçamento, apenas a captura secundária.

## 4. Páginas de produto ou serviço

**Fato observado:** a página de Serviços explica bem o que é cada serviço e seu benefício técnico, incluindo uma seção "Onde pode ser feito?" que lista aplicações (sistemas hidráulicos, refrigeração, tubulações, turbinas, motores, compressores) — bom conteúdo de suporte à decisão. Não há diferenciação de preço (esperado no nicho, orçamento sob consulta). Não há prova social contextual por serviço (nenhum case ou depoimento específico vinculado a "Flushing" ou "Alívio de Tensões", por exemplo). O texto menciona "Antes" e "Depois" na seção de Desengraxe, sugerindo imagens comparativas de resultado, mas essas imagens não têm alt text (não confirmável via inspeção de texto se são fotos reais de projeto ou genéricas de banco de imagem).

## 5. Página de contato e formulários

**Fato observado:** a página de orçamento (`/contato-2/`) é acessível via CTA direto, com formulário proporcional ao valor da oferta (nome completo, telefone, e-mail empresarial, assunto, mensagem) — nível de qualificação razoável para o ticket do serviço. Não há indicação de tempo de resposta ("respondemos em até X horas úteis") nem texto de privacidade/LGPD vinculado especificamente ao envio do formulário (existe apenas o banner de cookies, que é uma camada diferente de consentimento). O botão de envio usa o texto genérico "ENVIAR" em vez de um texto orientado à ação específica (ex: "Solicitar Orçamento Agora"). Existe página de agradecimento dedicada (`/pagina-de-obrigado/`, identificada no sitemap), o que é positivo e provavelmente sustenta o rastreamento de conversão do Google Ads já instrumentado no site.

## 6. Provas sociais e elementos de confiança

**Achado relevante:** a página de Certificados exibe os documentos reais via visualizador de PDF embutido (não como imagem de badge), incluindo um **Certificado de Registro Cadastral (CRC) da Petrobras**, comprovando que a Point Thermic é fornecedora cadastrada da Petrobras, e o certificado ISO 9001 emitido pela Fundação Carlos Alberto Vanzolini. Este é um ativo de credibilidade de altíssimo valor para o nicho (ser fornecedor cadastrado Petrobras é um selo de confiança forte para qualquer comprador do setor de óleo e gás) — e está subutilizado: aparece apenas nesta página interna, em formato de visualizador de PDF (experiência de leitura de documento, não de vitrine de credibilidade), e não é mencionado como manchete em nenhum outro ponto do site (home, sobre, ou nos anúncios, a confirmar no módulo de Meta/Google Ads).

**Fato observado:** logos de clientes (Usiminas, MAN, Medquímica, Milplan, TSE, entre outros) aparecem apenas na página interna "Clientes e Projetos", sem nomeação de projeto, resultado ou contexto — não aparecem na homepage, que é a página de maior tráfego. Não há depoimentos de clientes com nome, cargo e resultado em nenhuma página verificada. Não há números de prova social (quantidade de projetos executados, anos de mercado com número, clientes atendidos).

## 7. Conteúdo de suporte à decisão

**Fato observado:** existe uma página de FAQ linkada no rodapé ("Acesse nosso FAQ"), não aprofundada neste módulo por não constar na navegação principal nem no sitemap de páginas coletado — possível página órfã ou de outro tipo de conteúdo (a verificar). Blog existente está vazio (detalhado no módulo de SEO), eliminando qualquer conteúdo educativo de nutrição de visitante frio.

## 8. Experiência mobile

**Fato observado (screenshot mobile completo):** o site é responsivo, com menu hambúrguer funcional, texto legível sem necessidade de zoom, e CTA "Solicitar Orçamento" visível logo após a dobra inicial. A grade de ícones de segmento industrial se reorganiza em duas colunas no mobile, deixando o último ícone ("Usinas Termelétricas") sozinho e centralizado na última linha — detalhe estético menor, não crítico. O problema da caixa vazia ao lado da headline se repete integralmente no mobile. O banner de consentimento de cookies ocupa uma porção significativa da tela no primeiro carregamento mobile, exigindo interação antes de qualquer outra ação — comportamento padrão de LGPD/GDPR, mas o modal é extenso e não está desenhado como um bottom-sheet compacto, o que aumenta a fricção percebida no primeiro contato em tela pequena.

## 9. Velocidade e performance aparente

**Fato observado:** o carregamento até o estado de rede ociosa ocorreu em poucos segundos durante a navegação automatizada, sem erros de console. Medição formal de Core Web Vitals não disponível nesta sessão (ver módulo de SEO, limitação de cota da API do PageSpeed Insights). O volume de scripts de terceiros carregados (três GTMs, GA4, Google Ads, Meta Pixel, Clarity, Hotjar, sincronização Bing) é alto e pode impactar a performance percebida, especialmente em conexões móveis mais lentas — recomenda-se validação formal antes de qualquer decisão de otimização.

## 10. Coerência entre canais e site

A ser aprofundado nos módulos de Meta Ads e Google Ads (comparação entre a promessa dos anúncios e a entrega do site). Nesta etapa, o posicionamento do site (técnico, institucional, apoiado em certificação) é coerente com o que foi observado no módulo de contexto.

## Inventário de pontos de conversão

| Tipo | Página | Localização | Texto do CTA | Destino | Status |
|---|---|---|---|---|---|
| Botão CTA | Home | Acima da dobra, sobre imagem | "SOLICITAR ORÇAMENTO" | `/contato-2/` | Funcional |
| Botão CTA | Serviços | Topo da página | "SOLICITAR ORÇAMENTO" | `/contato-2/` | Funcional |
| Botão CTA | Venda e Locação | Meio da página | "SOLICITAR ORÇAMENTO" | `/contato-2/` | Funcional |
| Link de texto | Serviços | Fim da seção de Flushing | "Clique aqui" | Não verificado (texto de link genérico) | Funcional, mas copy fraco |
| Formulário de orçamento | Contato (`/contato-2/`) | Corpo da página | "ENVIAR" | Envio interno (WordPress), thank you page dedicada | Funcional |
| Formulário de newsletter | Rodapé, todas as páginas | Rodapé | "Enviar" | Envio interno (WordPress) | Funcional, mas só pede nome/e-mail |
| Link WhatsApp | Rodapé, todas as páginas | Rodapé, ícone social | Ícone (sem texto) | `api.whatsapp.com/send/?phone=11999325055` | Funcional, mas não é botão flutuante nem tem texto de chamada |
| Link Facebook | Rodapé, todas as páginas | Rodapé, ícone social | Ícone | facebook.com/www.pointthermic.com.br | Funcional |
| Link LinkedIn | Rodapé, todas as páginas | Rodapé, ícone social | Ícone | linkedin.com/company/point-thermic | Funcional |
| Link YouTube | Rodapé, todas as páginas | Rodapé, ícone social | Ícone | youtube.com/@pointthermicoficial | Funcional |
| Link Instagram | Rodapé, todas as páginas | Rodapé, ícone social | Ícone | instagram.com/point_thermic | Funcional |
| Telefone clicável | Rodapé, todas as páginas | Rodapé | "11 4580 – 3934" | `tel:1145803934` | Funcional |
| E-mail clicável | Rodapé, todas as páginas | Rodapé | "comercial@pointthermic.com.br" | `mailto:contato@pointthermic.com.br` | Funcional, porém com **inconsistência**: o texto exibido é um e-mail (comercial@) e o link real aponta para outro (contato@) |
| Link FAQ | Rodapé, todas as páginas | Rodapé, "Links Importantes" | "Acesse nosso FAQ" | Não mapeado no sitemap coletado | Não verificado nesta sessão |

**Avaliação do inventário:** o site depende de dois caminhos de conversão reais (formulário de orçamento e WhatsApp/telefone via rodapé) e um caminho de baixa intenção (newsletter). Não há chat ao vivo, não há botão de WhatsApp flutuante (apesar do número já estar disponível no site), não há popup ou barra de captura, e não há CTA de agendamento. Para um serviço de decisão B2B considerada, a ausência de um caminho de conversão de "meio de funil" (ex: material técnico para baixar, ou botão de WhatsApp com texto explícito e visível, não só ícone no rodapé) concentra toda a captação em quem já decidiu pedir orçamento.

## Scoring do site

| Dimensão | Nota |
|---|---|
| Proposta de valor e primeira impressão | 5/10 |
| Arquitetura de conversão | 5/10 |
| Navegação e usabilidade | 7/10 |
| Páginas de produto ou serviço | 6/10 |
| Contato e formulários | 6/10 |
| Provas sociais e confiança | 3/10 |
| Conteúdo de suporte à decisão | 2/10 |
| Mobile | 6/10 |
| Velocidade | Não avaliável formalmente (estimativa qualitativa: 6/10) |
| Coerência entre canais | A confirmar nos módulos de mídia paga |
| **Nota geral do site** | **5,0/10** |

Justificativa da nota geral: o site tem fundação funcional (formulário de orçamento qualificado, navegação clara, responsividade correta), mas desperdiça dois dos seus melhores ativos de conversão — o cadastro Petrobras e a certificação ISO 9001, hoje enterrados em um visualizador de PDF — e falha em pontos de baixo esforço e alto impacto, como o elemento visual vazio na primeira dobra e a ausência de um caminho de conversão de WhatsApp mais visível.

## Diagnóstico da arquitetura de conversão

O site não tem páginas "sem saída" graves (todas levam de volta à navegação principal ou ao rodapé), mas tem dependência excessiva do formulário de orçamento como único caminho de conversão de alta intenção. Não há alinhamento hoje entre a instrumentação de mídia paga (Google Ads e Meta Ads ativos, conforme scripts identificados) e uma arquitetura de conversão que ofereça múltiplos pontos de contato — o que é revisado com mais profundidade nos módulos de Meta Ads e Google Ads.

## Oportunidades de melhoria priorizadas

1. **Corrigir a caixa vazia na primeira dobra da home** (problema: elemento visual quebrado no espaço mais nobre da página; impacto: alto; facilidade: fácil; prioridade: máxima).
2. **Transformar a página de Certificados em vitrine de credibilidade**, com o selo Petrobras e ISO 9001 como imagens/badges, não apenas PDF embutido (impacto: alto; facilidade: média; prioridade: alta).
3. **Trazer o selo de fornecedor cadastrado Petrobras para a home e para a página Sobre Nós** como argumento central de confiança (impacto: alto; facilidade: fácil; prioridade: máxima).
4. **Adicionar botão de WhatsApp flutuante com texto explícito** (ex: "Fale com um especialista"), usando o número já disponível no site (impacto: alto; facilidade: fácil; prioridade: máxima).
5. **Adicionar CTA de fechamento ao final da página de Serviços**, substituindo o link genérico "Clique aqui" por uma chamada específica (impacto: médio-alto; facilidade: fácil; prioridade: alta).
6. **Corrigir a inconsistência entre o e-mail exibido e o e-mail real do link mailto** no rodapé (impacto: baixo, mas gera desconfiança se notado; facilidade: fácil; prioridade: média).
7. **Adicionar depoimentos de clientes nomeados** com cargo, empresa e resultado (impacto: alto; facilidade: média, depende de coleta; prioridade: alta).
8. **Nomear os projetos na página Clientes e Projetos** (setor, desafio, serviço prestado), não apenas exibir logos (impacto: médio-alto; facilidade: média; prioridade: alta).
9. **Adicionar números de prova social** (anos de mercado, projetos executados, clientes atendidos) na home (impacto: médio; facilidade: fácil, se o dado existir internamente; prioridade: média).
10. **Adicionar indicação de tempo de resposta no formulário de orçamento** (ex: "respondemos em até 24h úteis") (impacto: médio; facilidade: fácil; prioridade: média).
11. **Trocar o texto do botão de envio do formulário** de "ENVIAR" para algo específico como "Solicitar Orçamento Agora" (impacto: baixo-médio; facilidade: fácil; prioridade: média).
12. **Adicionar aviso de privacidade/LGPD específico junto ao formulário de orçamento**, além do banner de cookies genérico (impacto: baixo-médio, relevante para confiança e conformidade; facilidade: fácil; prioridade: média).
13. **Criar páginas dedicadas por serviço** com CTA e prova social contextual (ver também módulo de SEO, oportunidade compartilhada) (impacto: alto no médio prazo; facilidade: média; prioridade: alta).
14. **Adicionar conteúdo de meio de funil** (ex: guia técnico para download, calculadora simples de necessidade de serviço) para capturar visitantes que ainda não estão prontos para pedir orçamento (impacto: médio-alto; facilidade: média; prioridade: média).

## Quick wins (até 30 dias)

Corrigir a caixa vazia da home (1), trazer o selo Petrobras para a home (3), adicionar WhatsApp flutuante (4), corrigir o CTA de fechamento da página de Serviços (5), corrigir a inconsistência de e-mail (6), trocar o texto do botão "ENVIAR" (11), adicionar indicação de tempo de resposta (10).

## Recomendações estruturais

Reformular a página de Certificados como vitrine visual de credibilidade (2), reestruturar Clientes e Projetos com casos nomeados (8), coletar e publicar depoimentos (7), criar páginas de serviço dedicadas com CTA e prova social contextual (13), desenvolver conteúdo de meio de funil (14).

## CRO Site Score Geral

**5,0/10.** O site funciona operacionalmente (não há pontos de conversão quebrados), mas subutiliza seus ativos de credibilidade mais fortes (Petrobras, ISO 9001) e depende de um único caminho de conversão de alta intenção, sem caminhos intermediários para visitantes que ainda estão avaliando fornecedores.

Fonte e método: navegação direta do site via Chromium headless em 25/09/2026, incluindo captura de screenshot desktop (1440px) e mobile (390px, emulação iPhone). HypeStat sem dado para o domínio — limitação registrada. Core Web Vitals não medidos formalmente nesta sessão — limitação registrada.
