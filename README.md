# ROPRE Quarter — Elevate Incorporadora (ELEV1) — Q2/2026

Contexto completo do ciclo ROPRE Quarter (Growth Retrospective) da Elevate Incorporadora,
frente **Elevate Majestic**, para o Q2/2026 (abril–junho). Este repo existe pra permitir
continuar o trabalho a partir de outra máquina/pessoa, com o mesmo contexto que foi
usado pra construir o deck original.

**Deck publicado (produção):** https://elev1-ropre-q2-2026.vercel.app
**Vercel project:** `v4-felipe/elev1-ropre-q2-2026`

## Como continuar de outra máquina

1. Leia `handoff-sessao-2026-07-28.md` primeiro — decisões de alinhamento, fontes de
   dado confirmadas, e o histórico da sessão original.
2. Depois leia **"Estado atual e pendências reais"** abaixo — reflete três rodadas de
   ajuste feitas *depois* do handoff, que o handoff não cobre.
3. Para redeployar o `visual/index.html`: `vercel link --project elev1-ropre-q2-2026
   --scope v4-felipe` e depois `vercel --prod`, a partir de uma pasta com
   `visual/index.html` copiado pra `index.html` e `visual/assets/` copiado pra `assets/`
   (mesmo padrão usado nas sessões anteriores).

## Estrutura

- `ropre-quarter-final.md` — documento consolidado, ordem narrativa oficial (fonte de verdade em Markdown).
- `blocos/` — diagnóstico de fontes, resultados, gargalos, plano de ação, projeção Q3, objetivos, premissas/riscos, entregas, backlog.
- `visual/index.html` — deck HTML (34 slides, 1600×900, design system Colli&Co). `visual/assets/` tem os PNGs (logo do cliente, QR code do NPS, thumbnails dos 3 criativos vencedores, logos Colli&Co do rodapé).
- `decisoes-humanas.md` / `guardrails.md` / `observacoes-confiabilidade.md` — rastro auditável de decisões e limites de confiança dos dados.
- `memoria-proximo-quarter.md` — o que a V4 assume vs. o que precisa cobrar do Cliente no Q3.
- `memoria-quarter-cliente.md` — mapa longitudinal do cliente (histórico entre quarters).
- `fontes/` — snapshots JSON de mídia (NEKT Meta+Google) e entregas (Ekyte) usados na apuração original. **Atenção**: vários números desses snapshots foram corrigidos por consulta direta ao warehouse depois — ver seção abaixo.

## Fontes de dado (reconfirmar em qualquer sessão nova)

- **Flow/NEKT**: `projectDocumentId: bsbatk7lemxb9j20e3y8n279`. Meta Ads `accountId: act_1312693780484270`. Google Ads `accountId: 6333476896`. Localizar via `mcp__bigquery-calls__localize_project` (search "Elevate") — **não** via `cockpit_list_projects` (ELEV1 não está no Cockpit central, é operado pela squad Invictus fora dele).
- **Ekyte**: `workspaceId: 135598`.
- **Growth Pack / CRM**: fonte do funil comercial mensal (MQL/SQL/Venda/Faturamento). Link obtido na 2ª sessão: `https://docs.google.com/spreadsheets/d/10ZGTvfvme7d8BIO2Txe3jMCh9TA7aloAgAy5_FF9MTM` (aba com a tabela "Acompanhamento Mensal" — Investimento/Leads/MQL/SQL/Vendas/Receita por mês, sem cabeçalho de aba nomeado no export, procure pela linha `MQL` com dados de abril/maio/junho 2026 preenchidos).
- **Breakeven**: `https://docs.google.com/spreadsheets/d/1VXX4N-UpI6HK3Zbk9GeCJrM6ObZ51zr5bdUNVk31yh0`, aba "Breakeven Realista". WebFetch nessa planilha é pouco confiável — validar por repetição.
- **Logo do cliente**: convertido de um PDF (`Elev8-logo-square.pdf`) que o Felipe tinha em Downloads → `visual/assets/elevate-logo.png`.

## Estado atual e pendências reais (atualizado 2026-07-28, pós-handoff)

O `handoff-sessao-2026-07-28.md` documenta a sessão que criou o deck original (28 slides
→ 35 slides). Depois disso houve **três rodadas de ajuste** direto no deck publicado que
o handoff não cobre:

### O que foi corrigido/adicionado nas rodadas seguintes
- Slide de Funil Geral (03): agora tem faturamento (realizado vs. meta), Vendas corrigido
  para **2** (maio + junho — o handoff/deck original tinha só 1), CAC recalculado
  (R$ 17.718,36), e as metas de MQL/SQL/Venda/Faturamento preenchidas a partir das KRs do
  SMART do Q2 que o Felipe forneceu (ver "KRs do Q2" abaixo) — não são mais "meta a confirmar".
- Slide de Funil comercial mensal (06): mesma correção de Vendas/CAC + linha de faturamento
  mensal, taxas Lead→MQL→SQL→Venda e CAC/CPSQL por mês.
- **Correção importante de dado**: ao puxar métricas granulares (impressões/cliques/CTR/CPC)
  direto do warehouse Nekt via SQL para os slides 08–16 (campanha, público, criativo,
  keyword, posicionamento, idade, gênero, estado), descobriu-se que os snapshots JSON em
  `fontes/nekt/media/*.json` e os números originais de **criativos, posicionamento e idade**
  no deck vinham de um pull **parcial** (batiam em leads mas não em investimento total).
  Os números atuais no deck reconciliam 100% com o investimento total do Q2
  (Meta R$ 31.051,96); os JSONs em `fontes/` **não foram re-exportados** e ainda refletem
  os números antigos — se for reprocessar, prefira consultar o Nekt direto via
  `flow_media_query` em vez de confiar nesses JSONs.
- Slide de Julho em andamento (07): redesenhado (milestone cards + funil de estágios).
- Slide de Top 3 criativos (11): imagens reais dos 3 criativos vencedores inseridas
  (fornecidas pelo Felipe, `visual/assets/creative-ad0{2,4,8}.png`), com fundo desfocado
  (letterbox) pra mostrar o criativo inteiro sem cortar.
- Plano de ação: removido o item de "cadência de breakeven + Growth Pack" (era ação
  interna da V4, não fazia sentido pro cliente) e renumeradas as prioridades (agora 1–5).
- NPS: QR code do link Pipefy inserido no slide de encerramento.
- Capa: logo real da Elevate.

### KRs do Q2 usadas para calcular as metas (fornecidas pelo Felipe, 2026-07-28)

> Objetivo SMART Q2: Realizar a implementação do processo de vendas através de canais
> digitais, nos próximos 3 meses, construindo campanhas de marketing online e offline que
> vendem, otimizando via CPL/CPO/CPV/ROI.
> - KR1: 150 leads/mês, CPL máx. R$ 80,00
> - KR2: taxa Lead → Visita Agendada (V.A.) ≥ 15%
> - KR3: taxa V.A. → Visita Realizada (V.R.) ≥ 40%
> - KR4: taxa V.R. → Venda ≥ 30%

Mapeamento confirmado com o Felipe: no funil do deck, **MQL = Visita Agendada (V.A.)** e
**SQL/Visita = Visita Realizada (V.R.)**. Aplicando isso sobre a meta de 450 leads
(150×3): MQL meta = 68, SQL meta = 27, Venda meta = 8, Faturamento meta ≈ R$ 9,6M
(ticket médio R$ 1,2M/venda, mesmo ticket usado na projeção do Q3).

### ⚠️ Inconsistência conhecida, ainda não resolvida

O **slide 17 (Restrição Principal)** ainda cita "50 MQL qualificados" (número antigo).
Os **slides 26–27 (Objetivos Q3 SMART / Projeção Q3)** ainda usam a taxa Lead→MQL de
11,9% e a meta de "114 MQLs" — ambos calculados sobre o MQL antigo (50), não o corrigido
(25 realizado / taxa real 5,56%). Esses três slides **não foram atualizados** nas rodadas
de ajuste porque não estavam no escopo pedido pelo Felipe até agora. Antes de apresentar
o deck ao cliente, decidir com o Felipe se esses três slides devem ser recalculados com
os números corrigidos (Vendas=2, MQL=25) ou se a leitura antiga foi intencionalmente
mantida por algum motivo.

### Pendências reais que ainda dependem do Cliente
- Metas de MQL/SQL/Venda/Faturamento do Q3 (a meta do Q2 acima já foi resolvida via KR;
  a de Q3 segue em aberto — ver `blocos/projecao-proximo-quarter.md`).
- Fechamento da auditoria dos 238 leads abandonados no CRM (aberta desde 19/06).
- Motivo de desqualificação decomposto no CRM (76% dos leads marcados "não qualificado"
  sem motivo).
- Impacto quantificado da automação de cancelamento indevida (ativa até 25/06).
