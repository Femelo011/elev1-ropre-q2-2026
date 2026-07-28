# Memória Longitudinal - ELEV1 Elevate Incorporadora

Mapa/README dos ciclos de ROPRE Quarter do cliente. Squad Invictus. Frentes: Elevate Majestic (ativa) e Elevate Praiê (pré-lançamento, ainda sem funil real).

## Q2/2026 (abril-junho)

- **Planejamento:** 1º quarter operacional real (contrato iniciado 25/02/2026; jan-mar foi estruturação/onboarding).
- **ROPRE gerado:** 2026-07-27, com fase de revisão prévia de referências outlier (Creamy, Prevent Audio, VCMU/2FUN) e do deck já construído por Rafael Clarindo (rafaelclarindo.github.io/elev-ropre-q2-2026), elevado ao padrão outlier com granularidade de mídia via NEKT (Meta+Google) que o material prévio não tinha.
- **Plano aprovado internamente:** sim, por Felipe ("pode seguir", 2026-07-27).
- **Apresentação ao cliente:** pendente.
- **Commit do cliente:** pendente (objetivo SMART/OKRs do Q3 ainda não commitados formalmente).
- **Bateu a meta?** Mídia sim (446 leads projetados = 446 entregues, mesmo com verba de maio 34% abaixo do planejado). Comercial não decomposto por meta formal - só 1 venda no quarter, concentrada em maio.
- **Gap real:** funil comercial pós-lead (Lead→Visita 0,95%), causa em 3 frentes de CRM do Cliente (leads abandonados, qualificação sem motivo, automação de cancelamento indevida).
- **Ações executadas no Q2 (identificadas na retro, não neste ROPRE):** auditoria de leads abandonados aberta 19/06 (não fechada), correção da automação de cancelamento em 25/06, task de atualização do breakeven aberta 10/06 (não fechada).
- **Aprendizados:** mídia bem operada não compensa CRM quebrado - a V4 pode bater toda meta de aquisição e o negócio não fechar se o pós-lead falhar. Fontes de dado do squad Invictus (Growth Pack, planilha de breakeven) não estão no Cockpit central - usar NEKT direto via `flow_media_query` (documentId `bsbatk7lemxb9j20e3y8n279`) para mídia granular, e ter cautela com WebFetch em Google Sheets (mostrou leituras inconsistentes 3x na mesma planilha).
- **Planejado para o Q3:** ver `2026/Q2/ropre-quarter/memoria-proximo-quarter.md`.

## Referências de fonte de dado (para próximos ciclos)

- **Flow/NEKT:** `projectDocumentId: bsbatk7lemxb9j20e3y8n279`. Meta Ads `accountId: act_1312693780484270`. Google Ads `accountId: 6333476896`. Ambos conectados e queryable.
- **Ekyte:** `workspaceId: 135598` (`[INVICTUS] [ELEV1] Elevate Incorporadora`).
- **Cockpit central (Strapi):** ELEV1 **não está registrado** - projeto é operado via Growth Pack/Ekyte, fora do Cockpit central.
- **Breakeven:** planilha Google Sheets `1VXX4N-UpI6HK3Zbk9GeCJrM6ObZ51zr5bdUNVk31yh0`, aba "Breakeven Realista". Growth Pack (aba "2.2 Acompanhamento Mensal") é a fonte canônica de funil comercial mensal, mas o link direto não foi obtido nesta rodada.
- **Retrospectiva:** minhas-retrospectivas.vercel.app/ELEV/.
