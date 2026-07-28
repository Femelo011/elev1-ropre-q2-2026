# Handoff de sessão — ROPRE Quarter ELEV1 (Elevate) Q2/2026

**Data da sessão:** 2026-07-28 (iniciada 2026-07-27)
**Objetivo deste doc:** permitir continuar este trabalho de outra máquina/sessão sem depender da memória local desta máquina. Leia este arquivo primeiro, depois os arquivos referenciados.

## 1. Como a sessão começou

Felipe pediu para ativar a skill `ropre-do-quarter` para o cliente ELEV1 (Elevate), mas com uma fase de revisão explícita **antes** de construir qualquer conteúdo novo:
1. Ler o material prévio já construído por Rafael Clarindo: deck HTML em `rafaelclarindo.github.io/elev-ropre-q2-2026` + repo `github.com/rafaelclarindo/elev-ropre-q2-2026`.
2. Ler a retrospectiva do projeto: `minhas-retrospectivas.vercel.app/ELEV/`.
3. Ler o breakeven: planilha Google Sheets `1VXX4N-UpI6HK3Zbk9GeCJrM6ObZ51zr5bdUNVk31yh0`.
4. Analisar em profundidade 3 referências "outlier" (padrão-ouro): `blc-creamy-ropre-quarter.vercel.app`, `prev-ropre-q2-2026-julho.vercel.app`, `vcmu-ropre-q2-2026.vercel.app` — mais 2 referências normais (Malbork, MSYS).
5. Comparar o que já existia no deck prévio da Elevate com o padrão das outliers, listar gaps.
6. Só depois disso, seguir com a esteira normal do ROPRE.

## 2. O que a revisão encontrou (resumo)

Padrões repetidos nas 3 outlier: funil completo com etapa intermediária nomeada + custo por etapa; granularidade de mídia em 4 níveis (canal → campanha → público → criativo) sempre em ranking tabular; segmentação demográfica/posicionamento sempre presente com síntese; CRM decomposto por uma dimensão extra; criativos vencedores com imagem; restrição principal nomeada formalmente (Problema→Sintoma→Causa→Responsável); transparência de limite de dado como técnica retórica, não escondida.

Gaps do deck prévio da Elevate vs. esse padrão: funil raso (só 4 etapas, sem custo por etapa sistemático), zero breakdown de mídia por campanha/público/criativo, nenhuma segmentação demográfica, nenhum criativo mostrado, CRM pouco decomposto, sem "julho em andamento", sem seção de maturidade/risco estrutural do projeto.

## 3. Decisões de alinhamento tomadas com Felipe (nesta ordem)

1. Usar o deck prévio como **base**, elevando ao padrão outlier (não reconstruir do zero).
2. Usar a planilha de breakeven **ao vivo** como fonte de verdade (não o número desatualizado do deck).
3. Buscar granularidade de mídia via Cockpit/NEKT antes de seguir.
4. Tratar Q2/2026 como **1º quarter operacional real** (contrato iniciado 25/02/2026; sem Q1 comparável) — usar comparação mensal intra-quarter em vez de Q1 vs Q2.
5. Confirmar plano e ir para o diagnóstico de fontes pesado.
6. Divergência de leads Meta (446 plataforma vs 417 CRM): **usar o número da plataforma (446)**.
7. Breakeven: repuxar a planilha até bater por repetição (bateu: R$ 16.478.179,54 acumulado até dez/30, cenário Realista; fee R$ 7.922,41/mês).
8. Meta do Q2 informada por Felipe: **446 leads** (bateu exato); verba de mídia maio **R$ 15.000**; verba julho (referência Q3) **R$ 25.000**.

Registro completo em `decisoes-humanas.md` e `guardrails.md` (mesma pasta deste handoff).

## 4. Fontes de dado confirmadas (usar em qualquer sessão futura)

- **Flow/NEKT**: `projectDocumentId: bsbatk7lemxb9j20e3y8n279`. Meta Ads `accountId: act_1312693780484270`. Google Ads `accountId: 6333476896`. Ambos conectados e `queryable: true` (última sincronização 27/07/2026). Localizar via `mcp__bigquery-calls__localize_project` (search_text "Elevate") — **não** via `cockpit_list_projects`, porque ELEV1 **não está registrado no Cockpit central** (grade Strapi da org "Colli&Co"). É operado pela squad Invictus fora desse Cockpit.
- **Ekyte**: `workspaceId: 135598` (`[INVICTUS] [ELEV1] Elevate Incorporadora`).
- **Growth Pack / CRM**: fonte canônica do funil comercial mensal (aba "2.2 Acompanhamento Mensal"), mas **o link direto não foi obtido nesta sessão** — tentei a planilha Strategy Review (`1MrUklD9tulNHsxWmAh3fcUUBlBdY-IHzSUuEPAz32YQ`) e deu HTTP 401 (sem permissão de acesso). **Pendência real**: pedir a Felipe o link do Growth Pack ou o export do CRM.
- **Breakeven**: planilha Google Sheets `1VXX4N-UpI6HK3Zbk9GeCJrM6ObZ51zr5bdUNVk31yh0`, aba "Breakeven Realista". WebFetch nessa planilha se mostrou pouco confiável (3 leituras diferentes do mesmo número em momentos diferentes) — sempre validar por repetição ou confirmação direta com o humano antes de publicar um número de lá.

## 5. O que foi produzido (Markdown — fonte de verdade)

Todos os arquivos estão nesta mesma pasta (`ropre-quarter/`), já commitados no GitHub:

- `ropre-quarter-final.md` — documento consolidado completo, ordem narrativa oficial.
- `blocos/` — diagnostico-fontes, resultados, gargalos, plano-acao, projecao-proximo-quarter, objetivos, premissas-riscos, entregas, backlog-proximos-passos.
- `preview-consolidacao.md`, `decisoes-humanas.md`, `guardrails.md`, `observacoes-confiabilidade.md` — rastro auditável das decisões e lacunas.
- `memoria-proximo-quarter.md` — o que a V4 assume vs. o que precisa cobrar do Cliente no Q3.
- `../../../memoria-quarter-cliente.md` (`checkins/quarter/memoria-quarter-cliente.md`) — mapa longitudinal do cliente (1º registro).
- `fontes/nekt/media/meta_ads-resumo-q2-2026.json` e `google_ads-resumo-q2-2026.json` — snapshots de mídia granular (campanha, público, criativo, demografia, posicionamento).
- `fontes/ekyte-entregas-q2-2026.json` — snapshot de horas/entregas.
- `ropre-quarter-visual-input.md` — storyboard do deck visual.

**Achado central do quarter**: mídia saudável e batendo meta exata (446 = 446 leads), gargalo 100% concentrado no CRM/comercial pós-lead (Lead→Visita 0,95%), causa tripla evidenciada (238 leads abandonados sem contato, 76% "não qualificado" sem motivo decomposto, automação de cancelamento indevida ativa até 25/06).

## 6. Deck visual (HTML) e publicação

- Fonte: `visual/index.html` (35 slides, 1600x900, design system Colli&Co, validado via `validate_deck.py` — 0 erros).
- **Publicado em produção:** https://elev1-ropre-q2-2026.vercel.app (projeto Vercel `v4-felipe/elev1-ropre-q2-2026`).
- Pasta de deploy local: `.deploy/elev1-ropre-q2-2026/` (**não commitada no git** — segue o mesmo padrão de todos os outros clientes deste repo, que também não versionam `.deploy/`; contém token local do Vercel em `.env.local`). Para redeployar de outra máquina: copiar `visual/index.html` (+ `visual/assets/`) para uma pasta local, rodar `vercel link --project elev1-ropre-q2-2026 --scope v4-felipe` e depois `vercel --prod`.

### Round de revisão visual (feedback de Felipe em 2026-07-28, já aplicado)

Felipe revisou o primeiro deck (28 slides) contra referências visuais (prints de outro deck com padrão de tabela mensal, funil comercial B2B, ranking de campanha, execução do quarter, NPS) e pediu:
- Capas de seção em lista vertical com checklist (não mais colunas lado a lado).
- Remover slide de abertura solto.
- Meta Ads e Google Ads em tabela mensal (não cards).
- Adicionar: funil comercial mensal, "julho em andamento", bloco de drill-down até lead (campanha → público → ranking de criativos → top 3 → keywords → posicionamento → idade → gênero → estado).
- SMART simplificado, só 3 KRs.
- Projeção Q3 detalhada mês a mês com funil completo.
- Premissas reduzidas a 4 linhas.
- Entregas redesenhada (cards + barra horizontal).
- Slide de NPS antes do encerramento.

Tudo isso já está aplicado no `visual/index.html` atual e publicado. O deck passou de 28 para 35 slides.

## 7. Pendências reais (não decididas, precisam de Felipe)

1. **Link do Growth Pack** (ou export do CRM) — sem isso, MQL/SQL/Venda mês a mês (abril e junho) e o funil comercial de julho continuam marcados "aguardando Growth Pack" no deck. Só maio está fechado (142 leads = 142 leads Meta, alta confiança).
2. **Metas de MQL, SQL, Venda e Faturamento do Q2** — só existe meta formal de leads (446) e verba (maio R$ 15.000, julho R$ 25.000). O slide de funil geral projetado vs. realizado mostra "meta a confirmar" nessas linhas em vez de inventar um número.
3. Logo do cliente Elevate/Majestic não encontrado em nenhum lugar (nem no deck anterior) — capa usa fallback textual "ELEVATE".
4. Thumbnails dos criativos vencedores não disponíveis (já saíram do warehouse ativo do Nekt) — ranking de criativos é só tabular, sem imagem.

## 8. Próximo passo natural

Apresentar o ROPRE ao cliente e obter commit formal do objetivo Q3 — e, em paralelo, resolver os itens da seção 7 com Felipe (Growth Pack + metas) para fechar as lacunas antes ou depois da apresentação, conforme ele preferir.
