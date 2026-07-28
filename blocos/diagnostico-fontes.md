# Diagnóstico de Fontes - ROPRE Quarter

## 1. Escopo do bloco

- **Cliente/projeto:** ELEV1 - Elevate Incorporadora e Construtora Ltda (squad Invictus). Frente ativa no quarter: **Elevate Majestic** (lançamento imobiliário, Massaguaçu/Caraguatatuba). **Elevate Praiê** existe como segunda frente, mas sem mídia/CRM real rodando no Q2 (pré-lançamento).
- **Quarter analisado:** Q2/2026 (abril-junho de 2026).
- **Quarter seguinte:** Q3/2026 (julho-setembro de 2026).
- **Tipo de projeto:** Inside sales (funil imobiliário: Lead → MQL → Visita/SQL → Venda → Faturamento).
- **Objetivo deste bloco:** consolidar todas as fontes de dado disponíveis para o ROPRE, registrar o que foi confirmado via MCP (NEKT/Ekyte), o que veio de material já revisado (deck prévio, retrospectiva, planilha de breakeven) e as lacunas/conflitos que precisam de decisão humana antes de seguir para os blocos de resultados e gargalos.

## 2. Fontes consultadas

| Fonte | Status | Observação |
|---|---|---|
| Cockpit MCP (grade Strapi, `cockpit_list_projects`/`cockpit_get_project`) | Não encontrado | ELEV1 não está registrado na grade Cockpit consultável por este MCP (org "Colli&Co", 19 projetos). Projeto é operado pela squad Invictus via Growth Pack/Ekyte, fora do Cockpit central. |
| Flow MCP - `bigquery-calls` localizador | OK | Confirmou `projectDocumentId: bsbatk7lemxb9j20e3y8n279`, ticker ELEV1, integrações ativas: `ekyte`, `hops`, `nekt-meta-ads`, `nekt-google-ads`, `whatsapp-group`, `csat-matriz`. |
| Flow/NEKT MCP - Meta Ads (`flow_media_query`, `flow_media_query_reports`, `flow_media_creative_summary`) | OK | Conta `act_1312693780484270`, `status: connected`, `queryable: true`, última sincronização 27/07/2026. Consulta SQL direta às tabelas `adsinsights`, `adsinsights_by_age_and_gender`, `adsinsights_by_device_platform`. |
| Flow/NEKT MCP - Google Ads (`flow_media_query`) | OK | Conta `6333476896`, `status: connected`, `queryable: true`, última sincronização 27/07/2026. Tabelas `campaign_performance`, `ad_group_performance`, `keyword_performance`. |
| Ekyte MCP (`list_time_trackings`, `list_tasks`) | OK | Workspace 135598 `[INVICTUS] [ELEV1] Elevate Incorporadora`. 218 apontamentos de horas e 64 tarefas concluídas no período. |
| Deck HTML prévio (`rafaelclarindo.github.io/elev-ropre-q2-2026`) | Revisado (sessão anterior) | Material humano já construído para este quarter; usado como base e cruzado com os dados MCP. |
| Retrospectiva ELEV (`minhas-retrospectivas.vercel.app/ELEV/`) | Revisado (sessão anterior) | Fonte primária do funil comercial consolidado (Lead→Qualificado→Visita→Venda) e dos problemas de CRM (leads abandonados, tracking). |
| Planilha de breakeven (Google Sheets, aba Breakeven Realista/Cenários) | Parcial / conflitante | Dois fetches na mesma planilha retornaram números diferentes para faturamento acumulado projetado e fee (ver seção 6 - Conflitos). Maio/26 confirmado como "funil real fechado no Growth Pack": 142 leads, 15 MQL, 1 SQL, 1 venda, R$ 1.200.000 - **bate exatamente com os 142 leads Meta apurados via NEKT para maio**. |
| Growth Pack (Google Sheets, aba "2.2 Acompanhamento Mensal") | Não acessado diretamente | Fonte canônica do funil comercial mês a mês segundo `build_growthpack_inside_sales_config.py` (perfil `elevate`), mas o link direto da planilha GP não foi fornecido nesta sessão. Abril e junho não aparecem "fechados" na leitura da planilha de breakeven. |

## 3. Dados encontrados

**Mídia paga (NEKT, granularidade completa até criativo/demografia/posicionamento):**
- Meta Ads: overall mensal, por campanha (9), por adset/público (37), por anúncio/criativo (59 combinações com lead), por idade×gênero, por plataforma×posicionamento. Ação `lead` extraída via `UNNEST(actions)`.
- Google Ads: overall mensal, por campanha (5, todas Search), por ad group (10), por keyword (30 top).
- Snapshots salvos em `fontes/nekt/media/meta_ads-resumo-q2-2026.json` e `google_ads-resumo-q2-2026.json`.

**Entregas (Ekyte):**
- 146,6h totais no Q2 (abr 42,9h / mai 41,3h / jun 62,3h), 6 pessoas, 64 tarefas concluídas.
- Snapshot em `fontes/ekyte-entregas-q2-2026.json`.

**Comercial (retrospectiva + breakeven + deck prévio):**
- Funil Q2 consolidado (fonte: retro + deck): 421 leads → 50 qualificados (MQL) → 4 visitas → 1 venda → R$ 1.200.000 faturamento.
- Maio/26 fechado no Growth Pack (fonte: planilha breakeven): 142 leads, 15 MQL, 1 SQL, 1 venda, R$ 1.200.000 - a venda do quarter aconteceu em maio.
- Fee V4 mensal: R$ 7.922,41. Verba de mídia mensal prevista: R$ 12.443,02 (compatível com a média real de gasto Meta+Google no Q2, ≈ R$ 11,8k/mês, apesar de abril/maio/junho terem sido muito desiguais - ver bloco de resultados).
- Margem de contribuição: 25%. Breakeven mensal (recalculado e reconciliado, ver nota): **R$ 131.689,64/mês** = (Fee R$ 7.922,41 + Mídia regime R$ 25.000,00) / 25%.
- **Nota de correção:** a 1ª leitura WebFetch da planilha havia trazido "Breakeven mensal: R$ 267.077,59", mas esse valor não fecha com a fórmula (Fee+Mídia)/Margem usando nenhuma das verbas de mídia lidas (nem R$ 12.443,02 nem R$ 25.000,00) - foi tratado como leitura incorreta e descartado. O valor de R$ 131.689,64/mês recalculado bate quase exato com o "R$ 131.690/mês de competência" já citado no deck prévio, o que dá confiança cruzada nesse número.

## 4. Dados consolidados

| Indicador Q2/2026 | Meta (NEKT) | Google (NEKT) | Total mídia | CRM/Retro |
|---|---:|---:|---:|---:|
| Investimento | R$ 31.051,96 | R$ 4.384,76 | R$ 35.436,72 | - |
| Impressões | 477.258 | 10.415 | 487.673 | - |
| Cliques | 8.298 | 887 | 9.185 | - |
| Leads (ação plataforma) | 446 | 4 | 450 | 421 (deck/retro) |

**Leitura:** o total de leads apurado direto na plataforma de anúncios (446 Meta + 4 Google = 450) é maior que os 421 leads reportados no deck/retrospectiva (fonte CRM/Growth Pack). Ver conflito na seção 6 - não escolher automaticamente qual número usar no ROPRE final.

## 5. Lacunas

| Lacuna | Impacto | Decisão necessária |
|---|---|---|
| Sem quarter anterior comparável (Q1/2026 foi estruturação/onboarding, contrato iniciou 25/02/2026) | Não é possível montar "Q1 vs Q2" no padrão outlier | Já resolvida com Felipe: tratar como 1º quarter operacional, sem comparativo Q1 vs Q2 (decisão registrada em `decisoes-humanas.md`) |
| MQL/SQL mês a mês (abril e junho) não confirmados em nenhuma fonte lida nesta sessão - só maio está "fechado" na planilha de breakeven | Funil comercial só pode ser mostrado de forma confiável em granularidade trimestral (421→50→4→1), não mensal | Perguntar se há acesso direto à planilha Growth Pack (aba "2.2 Acompanhamento Mensal") para abril e junho, ou se o time confirma manualmente os números por mês |
| Link direto do Growth Pack não foi fornecido nesta sessão | Impede checar `paid_traffic_growthpack_updated_link` e reconciliar com a planilha de breakeven | Pedir o link do Growth Pack atualizado, se existir separado da planilha de breakeven já enviada |
| Elevate Praiê sem dado real de mídia/CRM no Q2 | Frente não pode entrar no funil quantitativo do quarter | Confirmar com Felipe se Praiê entra no ROPRE só como "fora do funil por decisão de fase" (pré-lançamento) |
| `list_tasks` do Ekyte não expõe data de conclusão explícita | Contagem de entregues por mês usa o projeto mensal Ekyte como proxy, não a data exata | Aceitar o proxy (mensal por projeto Ekyte) como suficiente para o bloco de entregas |

## 6. Conflitos

| Conflito | Fonte A | Fonte B | Recomendação |
|---|---|---|---|
| Leads Q2 (Meta) | NEKT (ação `lead` bruta): 446 | Deck/retro (CRM/Growth Pack): 417 | Usar 417 (CRM) como número oficial do funil comercial (é o que efetivamente chega em MQL/venda), e citar 446 como "leads brutos capturados na plataforma" com a diferença de 29 registrada como leads não sincronizados/duplicados/teste - **decisão de Felipe pendente sobre qual tratamento dar a essa diferença no texto final** |
| Faturamento acumulado projetado (breakeven, cenário Realista) | 1º fetch: R$ 92,5M (citado no deck prévio) | 2º fetch (WebFetch nesta sessão): R$ 71.868.000 na 1ª leitura, depois R$ 16.478.179,54 na 2ª leitura (linha "Resultado líquido acumulado" até dez/2030) | **Não usar nenhum dos três números até confirmação direta com quem mantém a planilha.** WebFetch em Google Sheets mostrou-se pouco confiável para números exatos (leituras diferentes da mesma planilha em momentos diferentes). Pedir export/print ou confirmação por texto do número correto de faturamento acumulado projetado antes de publicar no ROPRE. |
| Fee V4 mensal | Deck prévio: R$ 7.500 | Planilha breakeven (ambos fetches): R$ 7.922,41 | Usar R$ 7.922,41 (mais recente, confirmado 2x na mesma leitura) - divergência pequena, baixo risco |

## 7. Análise

O Q2/2026 é o primeiro quarter operacional real da Elevate (contrato iniciado 25/02/2026, mídia rodando de fato a partir de abril). A mídia paga tem fonte robusta e granular via NEKT (Meta + Google conectados e sincronizados), o que resolve o gap de granularidade identificado na revisão de referências (campanha → público → criativo → demografia → posicionamento, todos com contagem de leads, não só investimento). O funil comercial (MQL/SQL/Venda/Faturamento), por outro lado, depende de uma fonte externa ao NEKT (Growth Pack/planilha de breakeven) que não foi possível acessar com granularidade mensal confiável nesta sessão - maio está confirmado e bate com os dados de mídia (142 leads Meta = 142 leads Growth Pack em maio, um ponto forte de consistência), mas abril e junho não têm confirmação equivalente.

A divergência de leads (446 vs 417) e a inconsistência entre leituras da planilha de breakeven são o tipo de conflito que a esteira do ROPRE não deve resolver sozinha - ambos ficam registrados como pendência de validação humana antes da consolidação final.

## 8. Output para consolidação

- Prosseguir para o bloco de **resultados** usando: mídia mensal e granular 100% via NEKT (alta confiança); funil comercial trimestral (421→50→4→1→R$1,2M) via deck/retro (confiança média-alta, cross-checado parcialmente por maio); overall Projetado vs Realizado usando a verba prevista de R$ 12.443,02/mês e o breakeven de R$ 267.077,59/mês da planilha (confiança média, pendente reconciliação).
- Não publicar nenhum número de faturamento acumulado projetado (2026-2030) até resposta de Felipe sobre o conflito da seção 6.
- Registrar explicitamente no texto final a divergência de 446 vs 417 leads Meta, sem forçar uma escolha.

## 9. Observações de confiabilidade

- Alta confiança: dados de mídia paga (Meta/Google via NEKT), horas/entregas (Ekyte).
- Confiança média: funil comercial trimestral (cross-checado por maio, mas abril/junho não confirmados mês a mês).
- Baixa confiança: qualquer número de breakeven/projeção acumulada de longo prazo lido via WebFetch nesta sessão - tratar como hipótese até confirmação humana.
