# Decisões humanas - ROPRE Quarter ELEV1 Q2/2026

| Data | Humano | Decisão | Motivo | Impacto |
|---|---|---|---|---|
| 2026-07-27 | Felipe | Usar o deck prévio (rafaelclarindo.github.io/elev-ropre-q2-2026) como base, elevando ao padrão outlier em vez de reconstruir do zero | Deck já tem estrutura, plano 5W1H e honestidade de dado no nível outlier; só falta granularidade de mídia/CRM | Resultados e gargalos partem dos números já validados do deck, complementados por NEKT/Ekyte |
| 2026-07-27 | Felipe | Usar a planilha de breakeven ao vivo como fonte de verdade em vez do número citado no deck prévio | Deck estava desatualizado (retro já sinalizava "BE desatualizado o quarter inteiro") | Fee V4 usado: R$ 7.922,41 (não R$ 7.500 do deck) |
| 2026-07-27 | Felipe | Buscar granularidade de mídia (campanha/público/criativo/demografia) via Cockpit/NEKT/Ads Manager antes de seguir | Fechar o gap #2 e #3 identificado na revisão de referências outlier | Diagnóstico de fontes rodou consultas SQL diretas às tabelas NEKT Meta+Google; dado disponível em `fontes/nekt/media/` |
| 2026-07-27 | Felipe | Tratar Q2/2026 como 1º quarter operacional, sem comparativo Q1 vs Q2 | Contrato iniciou 25/02/2026; Jan-Mar foi estruturação, sem mídia rodando de fato | Resultados usa comparação mensal (abr/mai/jun) dentro do próprio Q2 em vez de Q1 vs Q2; sinaliza fase do projeto explicitamente no texto |

## Pendente de decisão (levantado no diagnóstico de fontes) - RESOLVIDO em 2026-07-27

| Data | Humano | Decisão | Motivo | Impacto |
|---|---|---|---|---|
| 2026-07-27 | Felipe | Usar o número de leads Meta direto da plataforma (446, ação `lead` bruta via NEKT), não o número do CRM/Growth Pack (417) | "Usar o que está na plataforma" - maio bate exato (142=142) entre as duas fontes, reforçando confiança na leitura NEKT | Funil de mídia usa 446 leads Meta (450 com Google) como número oficial de leads gerados; CPL recalculado sobre a base NEKT (spend R$ 31.051,96) |
| 2026-07-27 | Felipe | Repuxar a planilha de breakeven em vez de omitir a projeção acumulada | "Puxa isso da planilha que te passei" | 2ª tentativa de WebFetch bateu com a 1ª leitura anterior (R$ 16.478.179,54 até dez/30, cenário Realista, fee R$ 7.922,41) - usar esse valor, tratando-o como confirmado por repetição (2 leituras independentes convergentes), não como 100% garantido |

Link do Growth Pack (aba "2.2 Acompanhamento Mensal") ainda não foi fornecido - MQL/SQL mês a mês (abril e junho) seguem como lacuna; usa-se o funil trimestral fechado (421 leads CRM → 50 MQL → 4 visitas → 1 venda, com a ressalva de que a base de leads de mídia agora é 446/450).
