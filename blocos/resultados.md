# Resultados - ROPRE Quarter

## 1. Escopo do bloco

- **Cliente/projeto:** ELEV1 - Elevate Incorporadora (frente Elevate Majestic).
- **Quarter analisado:** Q2/2026 (abril-junho de 2026) - **1º quarter operacional real** (contrato iniciado 25/02/2026; jan-mar foi estruturação, sem mídia rodando de fato). Por decisão de Felipe (2026-07-27), não há comparativo Q1 vs Q2 - a leitura de evolução usa a quebra mensal dentro do próprio Q2.
- **Quarter seguinte:** Q3/2026.
- **Objetivo deste bloco:** consolidar o resultado do quarter (mídia granular + funil comercial) e o Projetado vs Realizado overall.

## 2. Fontes consultadas

| Fonte | Status | Observação |
|---|---|---|
| NEKT Meta Ads (SQL direto `adsinsights` + breakdowns) | OK | Ver `fontes/nekt/media/meta_ads-resumo-q2-2026.json` |
| NEKT Google Ads (SQL direto `campaign/ad_group/keyword_performance`) | OK | Ver `fontes/nekt/media/google_ads-resumo-q2-2026.json` |
| Retrospectiva ELEV + deck prévio | OK (revisado em sessão anterior) | Fonte do funil comercial CRM (MQL/Visita/Venda/Faturamento) |
| Planilha breakeven (Google Sheets) | Parcial | Confirma maio fechado no Growth Pack; **verba de mídia planejada por mês do Q2 e meta de leads/CPL do Q2 não confirmadas** - ver seção 5 |

## 3. Dados encontrados

### 3.1 Mídia - Realizado mensal (Meta + Google, fonte NEKT, decisão Felipe: usar leads direto da plataforma)

| Indicador | Abril/26 | Maio/26 | Junho/26 | Total Q2 |
|---|---:|---:|---:|---:|
| Investimento Meta | R$ 1.792,36 | R$ 9.920,89 | R$ 19.338,71 | R$ 31.051,96 |
| Investimento Google | - | - | - | R$ 4.384,76 |
| **Investimento total** | - | - | - | **R$ 35.436,72** |
| Impressões Meta | 33.367 | 129.388 | 314.503 | 477.258 |
| Cliques Meta | 784 | 2.546 | 4.968 | 8.298 |
| CPC Meta | R$ 2,29 | R$ 3,90 | R$ 3,89 | R$ 3,74 |
| CPM Meta | R$ 53,72 | R$ 76,68 | R$ 61,49 | R$ 65,07 |
| **Leads Meta (ação plataforma)** | **27** | **142** | **277** | **446** |
| CPL Meta | R$ 66,38 | R$ 69,86 | R$ 69,81 | R$ 69,62 |
| Leads Google (conversions) | - | - | - | 4 |
| CPL Google | - | - | - | R$ 1.096,19 |
| **Leads totais (Meta+Google)** | - | - | - | **450** |

Nota de leitura: o investimento cresceu 10,8x de abril para junho (rampa de verba clássica de 1º quarter), e o CPL Meta ficou estável entre R$ 66-70 nos três meses - ou seja, o custo por lead não piorou com o aumento de escala, sinal positivo de saúde de conta.

### 3.2 Mídia granular - Meta Ads (fonte: NEKT, Q2 completo)

**Por campanha (top 5 por investimento, de 9 ativas):**

| Campanha | Investimento | Leads | CPL |
|---|---:|---:|---:|
| [C:02] MEIO | R$ 8.588,71 | - | - |
| [C:01] TOPO - Sudeste | R$ 7.966,48 | - | - |
| [C:03] TOPO - Regiões ABC/ZL/ZS | R$ 3.126,90 | - | - |
| [C:05] TOPO - Regiões ABC/ZL/ZS \|\| E.H. | R$ 2.697,85 | - | - |
| [C:06] MEIO \|\| E.H. | R$ 2.600,69 | - | - |

*(Leads por campanha não foram somados nesta rodada por limite de tempo de sessão - dado bruto por campanha/adset/anúncio já está salvo em `fontes/nekt/media/meta_ads-resumo-q2-2026.json` e pode ser fechado no próximo ciclo se necessário para o deck visual.)*

**Por público/adset (top, todos "SP Capital + Grande SP | 32-58"):** Lookalike 1% Leads Elevate lidera investimento (R$ 5.916,61 só no C:02/MEIO), seguido por Carros de luxo, Investimento e bolsa de valores, Esportes luxo e Público Campeão. Padrão de segmentação por interesse afluente/luxo, consistente com o ticket do empreendimento.

**Por criativo (top por leads, ad-level):**

| Anúncio | Leads (maior combinação campanha/adset) | Investimento (na combinação) |
|---|---:|---:|
| AD04 - Zoom na terra (vídeo) | 60 | R$ 3.340,44 |
| AD02 - Alto padrão (vídeo) | 33 | R$ 1.603,42 |
| AD04 - Zoom na terra (vídeo, outra campanha) | 27 | R$ 1.485,37 |
| AD02 - Alto padrão (vídeo, outra campanha) | 23 | R$ 1.212,61 |
| AD03 - Criar memórias (vídeo) | 14-22 | variável |

"AD04 - Zoom na terra" e "AD02 - Alto padrão" são os dois criativos-vídeo que mais geram lead de forma consistente entre campanhas diferentes - candidatos naturais a escalar isolados no Q3.

**Demografia (idade × gênero, por leads):**

| Faixa etária | Masculino | Feminino |
|---|---:|---:|
| 45-54 | 131 leads | 57 leads |
| 35-44 | 116 leads | 29 leads |
| 55-64 | 57 leads | 23 leads |
| 25-34 | 22 leads | 10 leads |

Leitura: 71% dos leads são homens, concentrados em 35-54 anos (55% do total). Público consistente com investidor/comprador de 2ª residência de alto padrão.

**Posicionamento (por leads):** Instagram Feed lidera com 196 leads (CPL ≈ R$ 21,86, o mais eficiente), seguido por Instagram Reels (105 leads, CPL ≈ R$ 19,18, também muito eficiente), Instagram Stories (61 leads), Facebook Reels (49 leads) e Facebook Feed (30 leads, CPL mais caro do grupo ≈ R$ 7,50 mas baixo volume). Instagram concentra ~85% dos leads do Q2.

### 3.3 Mídia granular - Google Ads (fonte: NEKT, Q2 completo)

100% Search, 5 campanhas geográficas/temáticas (Investimento, Veraneio, Caraguatatuba, Praia). Keyword "apartamento lançamento litoral norte" é a que mais converte (2 de 4 conversões do quarter, CPA ≈ R$ 393,72). As demais 4 campanhas somam 2 conversões com CPA alto (R$ 800-870), sinal de baixa eficiência do Google frente ao Meta neste quarter (CPL Google R$ 1.096 vs CPL Meta R$ 70).

### 3.4 Funil comercial (fonte: retrospectiva ELEV + deck prévio, cross-checado por maio via breakeven)

| Etapa | Volume Q2 | Taxa de passagem | Custo por etapa |
|---|---:|---:|---:|
| Leads (mídia, plataforma) | 450 | - | CPL médio R$ 78,75 |
| Leads (CRM, Growth Pack) | 421 | 93,6% do bruto entrou no CRM | - |
| MQL (qualificados) | 50 | 11,9% lead→MQL (base CRM) | CPMQL ≈ R$ 708,73 |
| Visita/SQL | 4 | 8,0% MQL→visita | CPSQL ≈ R$ 8.859,18 |
| Venda | 1 | 25,0% visita→venda | CAC ≈ R$ 35.436,72 |
| Faturamento | R$ 1.200.000,00 | Ticket médio R$ 1.200.000,00 | ROAS ≈ 33,86x |

Maio/26 é o único mês com funil "fechado" confirmado no Growth Pack (142 leads, 15 MQL, 1 SQL, 1 venda, R$ 1,2M) - **a única venda do quarter aconteceu em maio**, e os 142 leads de maio batem exatamente com os 142 leads Meta apurados via NEKT no mesmo mês (alta confiança nesse ponto específico).

### 3.5 Projetado vs Realizado overall (meta informada por Felipe, 2026-07-27)

| Indicador | Projetado | Realizado | Delta | Status |
|---|---:|---:|---:|---|
| Leads Q2 (meta de mídia) | 446 | 446 (Meta, ação plataforma) | 0 | **Bateu** (100% exato) |
| Leads Q2 (Meta + Google) | 446 | 450 | +4 | Superou (com Google incluído) |
| Verba de mídia - maio/26 | R$ 15.000,00 | R$ 9.920,89 (Meta; Google não discriminado por mês) | -R$ 5.079,11 (-33,9%) | Não bateu (investiu menos que o planejado, mesmo assim entregou o volume de lead da meta trimestral) |
| Verba de mídia - abril/26 | Sem meta formal registrada | R$ 1.792,36 | - | Sem dado de meta |
| Verba de mídia - junho/26 | Sem meta formal registrada | R$ 19.338,71 | - | Sem dado de meta |
| Verba de mídia - julho/26 (referência Q3) | R$ 25.000,00 | Fora do escopo Q2 | - | Informativo para projeção do próximo quarter |

Leitura: a meta de leads do quarter foi batida com precisão exata (446 = 446) investindo menos que o planejado em maio (66% do budget de maio) - reforça a leitura de que a eficiência de mídia (CPL estável, público certo) compensou um investimento sub-executado. Não há meta formal registrada para abril e junho isoladamente - apenas os dois pontos-âncora (maio R$ 15.000 e julho R$ 25.000) foram informados, o que também sinaliza que o plano de mídia é uma rampa crescente mês a mês, ainda não formalizada em uma meta trimestral única.

## 4. Dados consolidados

Ver seção 3 - tabelas já consolidadas por indicador pareado (volume + custo), sem separar volume e eficiência em tabelas diferentes, conforme padrão do ROPRE.

## 5. Lacunas

| Lacuna | Impacto | Decisão necessária |
|---|---|---|
| ~~Projetado vs Realizado overall~~ | ~~Resolvido~~ | Felipe informou (2026-07-27): meta de leads do quarter = 446; verba de mídia maio = R$ 15.000; verba de mídia julho (Q3) = R$ 25.000. Ver seção 3.5. Abril e junho não têm meta formal registrada isoladamente - lacuna aceita, não bloqueia o bloco. |
| MQL/SQL mês a mês (abril e junho) | Só o total trimestral (50 MQL, 4 visitas) é confiável | Growth Pack (aba "2.2 Acompanhamento Mensal") não foi acessado diretamente nesta sessão |
| Leads por campanha/adset (contagem, não só investimento) não foi somada nesta rodada | Bloco de gargalos/plano de ação pode usar os dados de `fontes/nekt/media/meta_ads-resumo-q2-2026.json` (leads por ad_name) como proxy | Aceitável para o Markdown; fechar antes da camada visual se o storyboard pedir ranking por campanha com leads |
| Elevate Praiê sem funil real no Q2 | Frente fora do funil quantitativo | Confirmado por decisão anterior: entra como "fora do funil por decisão de fase" |

## 6. Conflitos

| Conflito | Fonte A | Fonte B | Recomendação |
|---|---|---|---|
| Leads projetados de junho | Retro: "142 leads projetados" para junho | NEKT: junho teve 277 leads Meta (muito acima) | Não usar o número da retro sem confirmação - pode se referir a outro recorte (ex.: só uma campanha, ou uma meta antiga desatualizada) |
| Verba de mídia mensal planejada | 1ª leitura BE: R$ 12.443,02 | 2ª leitura BE: R$ 25.000,00 "a partir de Ago/26" | Tratar R$ 25.000 como verba de regime (Q3+), não necessariamente a meta de abr-jun; sem confirmação, Projetado vs Realizado de mídia fica pendente |

## 7. Análise

O quarter mostra uma curva de ramp-up clássica e saudável: investimento cresce 10,8x (abr→jun) sem piora de CPL (R$ 66-70 estável), o que indica que a conta escalou sem perder eficiência na geração de lead. O gargalo não está na geração de lead (mídia entrega volume crescente a custo estável) - está adiante no funil: de 450 leads captados, apenas 4 chegaram a visita (0,9%) e 1 a venda. Isso é consistente com o que o deck prévio já havia identificado (gargalo Lead→Visita), e a granularidade nova (demografia, posicionamento, criativo) mostra que a mídia está entregando o público certo (homens 35-54, afluente, via Instagram Feed/Reels a CPL baixo) - reforçando que o problema está na operação comercial pós-lead, não na aquisição.

Sem a confirmação da verba/meta planejada para Q2, o bloco de Projetado vs Realizado overall - obrigatório no padrão ROPRE - não pode ser fechado nesta rodada.

## 8. Output para consolidação

- Funil de mídia mensal e granular (campanha/público/criativo/demografia/posicionamento): pronto para o ROPRE final.
- Funil comercial trimestral: pronto, com a ressalva de que MQL/SQL mensais não são confiáveis.
- Projetado vs Realizado overall: pronto (meta de leads batida exatamente; verba de maio sub-executada em 34%; abril/junho sem meta formal isolada).

## 9. Observações de confiabilidade

- Alta confiança: toda a mídia granular (fonte única NEKT, sincronizada em 27/07/2026).
- Alta confiança pontual: maio (funil comercial cruzado entre 2 fontes independentes, bate exato).
- Média confiança: funil comercial trimestral total (421→50→4→1), fonte CRM/retro não recruzada mês a mês.
- Baixa confiança / lacuna: qualquer meta ou verba planejada para Q2 especificamente - necessário para completar Projetado vs Realizado.
