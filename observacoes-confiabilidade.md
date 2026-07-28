# Observações de Confiabilidade - ROPRE Quarter ELEV1 Q2/2026

## Lacunas registradas

- MQL/SQL mês a mês (abril e junho) não confirmados fora do trimestre fechado - só maio está "fechado" no Growth Pack conforme a planilha de breakeven.
- Leads por campanha (contagem, não só investimento) não foi somada nesta rodada - dado bruto está salvo em `fontes/nekt/media/meta_ads-resumo-q2-2026.json`, pode ser fechado depois se o storyboard visual exigir.
- Elevate Praiê sem funil real no Q2 - tratado como "fora do funil por decisão de fase" (pré-lançamento).
- Ekyte não expõe data de conclusão explícita via MCP - "entregas por mês" usa o projeto mensal Ekyte como proxy.
- Verba de mídia planejada para agosto/setembro do Q3 não confirmada - só julho (R$ 25.000) foi informado; projeção mês a mês assume repetição desse valor.

## Conflitos registrados e como foram resolvidos

- Leads Meta Q2: 446 (plataforma) vs 417 (CRM/deck prévio) - **resolvido por decisão de Felipe: usar 446** (2026-07-27).
- Breakeven/faturamento acumulado projetado: 3 leituras divergentes da mesma planilha via WebFetch (R$ 92,5M / R$ 71,9M / R$ 16,5M) - **resolvido: 2ª releitura reconfirmou R$ 16.478.179,54, tratado como mais confiável por repetição**.
- Breakeven mensal: 1ª leitura trouxe R$ 267.077,59, que não fecha com a fórmula (Fee+Mídia)/Margem - **descartado, recalculado para R$ 131.689,64, que bate com o deck prévio**.
- Verba de mídia mensal: R$ 12.443,02 (1ª leitura) vs R$ 25.000,00 "a partir de ago/26" (2ª leitura) - **resolvido: Felipe confirmou R$ 15.000 (maio) e R$ 25.000 (julho/regime) diretamente**, sem depender mais da leitura da planilha.

## Premissas assumidas (marcadas como hipótese no conteúdo)

- Projeção do Q3 assume CPL estável (base: junho/26) e mix de canal Meta/Google similar ao Q2.
- Cenários Realista/Otimista assumem melhora da taxa MQL→Visita motivada pelo plano de ação (CRM) - ainda não confirmada pelo Cliente.
- Verba de mídia de agosto/setembro assumida igual à de julho (R$ 25.000/mês), não confirmada individualmente.

## Decisões de seguir mesmo com lacuna

- Seguir sem MQL/SQL mensal granular (abril/junho), usando apenas o total trimestral - autorizado implicitamente ao não bloquear o fluxo após o diagnóstico de fontes.
- Seguir sem fechar a contagem de leads por campanha nesta rodada - dado bruto preservado para fechamento posterior.
