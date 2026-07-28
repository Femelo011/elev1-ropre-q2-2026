# Preview de Consolidação - ROPRE Quarter ELEV1 Q2/2026

Status: aguardando aprovação humana. Comando para consolidar: `aprovado, consolidar`.

## Resumo executivo preliminar

Q2/2026 é o **primeiro quarter operacional real** da Elevate (contrato iniciado 25/02/2026). A mídia paga entregou exatamente a meta de leads combinada (446 = 446, Meta Ads) mesmo investindo 34% a menos que o planejado em maio, com CPL estável (R$ 66-70) ao longo de uma escala de investimento 10,8x entre abril e junho. A granularidade de mídia (campanha, público, criativo, demografia, posicionamento) confirma que a aquisição está saudável e entregando o público certo (homens 35-54, afluentes, via Instagram). O gargalo do quarter está inteiramente na camada comercial/CRM pós-lead: de 421-450 leads, só 4 chegaram a visita (0,95%) e 1 a venda (R$ 1.200.000 de faturamento), com causa evidenciada em três frentes de CRM do Cliente (leads abandonados, qualificação sem motivo decomposto, automação de cancelamento indevida).

## Resultados principais

- Investimento total Q2: R$ 35.436,72 (Meta R$ 31.051,96 + Google R$ 4.384,76).
- Leads: 446 Meta + 4 Google = 450 (CPL Meta R$ 69,62).
- Funil comercial: 421 leads (CRM) → 50 MQL (11,9%) → 4 visitas (8,0%) → 1 venda (25,0%) → R$ 1.200.000.
- Maio é o único mês com funil comercial 100% cruzado entre mídia e CRM (142=142) - e foi o mês da única venda.

## Projetado vs Realizado

| Indicador | Projetado | Realizado | Status |
|---|---:|---:|---|
| Leads Q2 | 446 | 446 (450 com Google) | Bateu / superou |
| Verba maio/26 | R$ 15.000 | R$ 9.920,89 | Não bateu (investiu menos, ainda assim bateu a meta de lead) |

## Restrição principal e gargalos priorizados

**Restrição principal:** Lead→Visita 0,95% (MQL→Visita 8,0%, pior degrau). Causa provável tripla: 238 leads abandonados sem contato, 76% dos leads marcados "não qualificado" sem motivo decomposto, automação de cancelamento indevida ativa até 25/06. Confiança média-alta.

6 gargalos secundários priorizados em `blocos/gargalos.md`, incluindo ineficiência do Google Ads (CPL 15,7x maior que Meta) e breakeven desatualizado o quarter inteiro.

## Plano de ação recomendado

6 ações com Score (Impacto/(Esforço+Dependência)):

1. Escalar os 2 criativos-vídeo campeões (Score 2,00) - V4, baixo esforço.
2. Cadência de atualização do breakeven + conectar Growth Pack (Score 1,00) - V4.
3. Auditoria + SLA dos 238 leads abandonados (Score 0,71) - **Cliente**.
4. Padronizar motivo de desqualificação + auditar amostra (Score 0,67) - **Cliente**.
5. Levantar impacto da automação de cancelamento indevida (Score 0,60) - **Cliente**.
6. Revisar keywords Google Ads ineficientes (Score 0,50) - V4.

## Projeção do próximo quarter (Q3/2026)

3 cenários (Pessimista/Realista/Otimista), verba R$ 75.000 (3 meses × R$ 25.000), leads projetados 850-1.050, vendas projetadas 2-6, faturamento R$ 2,4M-7,2M. Cenário Realista: 955 leads, 14 visitas, 3-4 vendas, R$ 3,6M-4,8M - condicionado à execução das ações de CRM pelo Cliente.

## Objetivos e OKRs

Objetivo SMART Q3 ancorado no cenário Realista (ver `blocos/objetivos.md`), com 5 OKRs - 3 de responsabilidade do Cliente (CRM/comercial), 2 da V4 (mídia).

## Premissas e riscos

6 premissas registradas, 4 com dono no Cliente, 2 na V4 (ver `blocos/premissas-riscos.md`).

## Entregas do quarter

146,6h alocadas (abr 42,9h / mai 41,3h / jun 62,3h), 64 tarefas concluídas, 6 pessoas envolvidas.

## Lacunas e conflitos ainda presentes

- MQL/SQL mensal (abril/junho) não confirmado fora do trimestre fechado.
- Verba de mídia de agosto/setembro do Q3 não confirmada individualmente (assumida igual a julho).
- Melhora de taxa MQL→Visita nos cenários Realista/Otimista é hipótese, não commit do Cliente.
- Contagem de leads por campanha (Meta) não fechada nesta rodada (dado bruto disponível em `fontes/`).

Ver `observacoes-confiabilidade.md` para lista completa.

## Decisões já tomadas por Felipe (não pendentes)

- Deck prévio usado como base, elevado ao padrão outlier.
- Breakeven da planilha ao vivo como fonte de verdade (não o número do deck).
- Granularidade de mídia buscada via NEKT antes de seguir.
- Q2 tratado como 1º quarter operacional (sem Q1 vs Q2).
- Leads Meta: usar número da plataforma (446), não o do CRM (417).
- Breakeven: repuxado da planilha, 2ª leitura confirmada por repetição.
- Meta Q2: 446 leads / verba maio R$ 15.000 / verba julho R$ 25.000.

## Decisões pendentes do humano (para aprovar agora)

1. Validar a restrição principal e a causa provável tripla (CRM) - `gargalos.md`.
2. Validar o plano de ação e o Score de cada ação - `plano-acao.md`.
3. Validar os cenários de projeção do Q3 (especialmente a hipótese de melhora de MQL→Visita) - `projecao-proximo-quarter.md`.
4. Validar o objetivo SMART e os OKRs propostos - `objetivos.md`.
5. Confirmar se pode seguir com as lacunas listadas acima (MQL/SQL mensal, verba ago/set) sem bloquear a consolidação.

Se tudo estiver de acordo, responda **"aprovado, consolidar"** para eu gerar `ropre-quarter-final.md`, `memoria-proximo-quarter.md` e atualizar a memória longitudinal do cliente. Se algo precisar de ajuste, aponte o bloco e eu corrijo antes de consolidar.
