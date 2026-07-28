# Projeção do Próximo Quarter - ROPRE Quarter

## 1. Escopo do bloco

- **Cliente/projeto:** ELEV1 - Elevate Incorporadora (Elevate Majestic).
- **Quarter analisado:** Q2/2026 (base). **Quarter projetado:** Q3/2026 (julho-setembro).
- **Objetivo deste bloco:** projetar volume, custo e faturamento esperado do Q3 com base na verba planejada, no unit economics real do Q2 e no plano de ação aprovado.

## 2. Fontes consultadas

| Fonte | Status | Observação |
|---|---|---|
| `blocos/resultados.md` | OK | Unit economics real (CPL, taxas de conversão) |
| `blocos/plano-acao.md` | OK | Ações que podem alterar as taxas de conversão no Q3 |
| Verba informada por Felipe (2026-07-27) | OK | R$ 25.000/mês de mídia a partir de julho (regime) |
| Breakeven reconciliado (`diagnostico-fontes.md`) | OK | R$ 131.689,64/mês |

## 3. Dados encontrados

Premissas base (todas marcadas como **hipótese**, extrapolação a partir do unit economics de junho/26 - mês mais recente e de maior volume/maturidade de conta):

- CPL Meta estável: R$ 69,62 (média Q2) a R$ 69,81 (junho, mês mais maduro) - assume-se manutenção dessa faixa.
- Mix de canal similar ao Q2: ~88% Meta / ~12% Google por verba.
- Taxas de funil Q2 como piso (Pessimista): Lead→MQL 11,9% / MQL→Visita 8,0% / Visita→Venda 25,0%.
- Cenário Realista assume melhora parcial em MQL→Visita (de 8,0% para ~12%) por conta das ações 3, 4 e 5 do plano de ação (CRM/SLA/qualificação), que são de responsabilidade do Cliente e começam a rodar já nas primeiras semanas do Q3.
- Cenário Otimista assume melhora mais forte em MQL→Visita (~18%), equivalente a resolver a maior parte do gargalo de CRM ainda no Q3.

## 4. Dados consolidados

### Projeção trimestral (Q3/2026)

| Indicador | Pessimista | Realista | Otimista | Fonte/Premissa |
|---|---:|---:|---:|---|
| Verba de mídia (3 meses) | R$ 75.000 | R$ 75.000 | R$ 75.000 | Informado por Felipe (R$ 25.000/mês) |
| Fee V4 (3 meses) | R$ 23.767,23 | R$ 23.767,23 | R$ 23.767,23 | Planilha breakeven reconciliada |
| Leads totais | 850 | 955 | 1.050 | Extrapolação de CPL de junho/26 (hipótese) |
| CPL médio | R$ 88,24 | R$ 78,53 | R$ 71,43 | Assume alguma perda de eficiência com escala maior (hipótese conservadora no pessimista) |
| MQL (11,9%) | 101 | 114 | 145 (13,8%*) | Taxa Q2 no pessimista/realista; leve melhora de mix no otimista |
| Visita/SQL | 8 (8,0%) | 14 (12,0%*) | 26 (18,0%*) | *Taxas melhoradas via plano de ação nos cenários realista/otimista - hipótese |
| Venda (25,0%) | 2 | 3-4 | 6 | Taxa Visita→Venda mantida constante (sem evidência para alterar) |
| Faturamento (ticket R$ 1.200.000) | R$ 2.400.000 | R$ 3.600.000-4.800.000 | R$ 7.200.000 | Ticket médio Q2 mantido |
| Breakeven mensal | R$ 131.689,64 | R$ 131.689,64 | R$ 131.689,64 | Reconciliado |

### Projeção mês a mês (Realista)

| Indicador | Julho | Agosto | Setembro | Total Q3 |
|---|---:|---:|---:|---:|
| Verba de mídia | R$ 25.000 | R$ 25.000 | R$ 25.000 | R$ 75.000 |
| Leads (CPL ~R$ 78,53) | 318 | 318 | 319 | 955 |
| MQL (11,9%) | 38 | 38 | 38 | 114 |
| Visita (12,0%, pós-plano de ação) | 5 | 5 | 4 | 14 |
| Venda (25,0%) | 1 | 1 | 1-2 | 3-4 |

## 5. Lacunas

| Lacuna | Impacto | Decisão necessária |
|---|---|---|
| Melhora de taxa MQL→Visita nos cenários Realista/Otimista é hipótese, não fato validado | Projeção de venda/faturamento do Q3 pode ficar otimista demais se o Cliente não executar as ações 3-5 do plano de ação | Validar com Felipe se os cenários Realista/Otimista devem assumir essa melhora, ou se o objetivo SMART do Q3 deve ser mais conservador (baseado só no cenário Pessimista) até o CRM mostrar sinal real de melhora |
| Verba de mídia julho R$ 25.000/mês é a única confirmada - agosto e setembro foram extrapolados como iguais | Se a verba crescer ou cair nos meses seguintes, a projeção muda | Confirmar se R$ 25.000/mês é o valor fixo para o Q3 inteiro ou só o ponto de partida de julho |

## 6. Conflitos

Nenhum novo.

## 7. Análise

A projeção do Q3 tem uma característica que já apareceu nos resultados do Q2: o lado de mídia é previsível e de baixo risco (CPL estável, canal maduro, ação de baixo esforço já priorizada no plano - escalar os criativos campeões). O lado de incerteza real está no funil comercial - o volume de venda projetado (2 a 6 vendas, dependendo do cenário) varia por um fator de 3x só em função de o Cliente executar ou não as correções de CRM do plano de ação. Isso deve ficar explícito na apresentação: a meta de mídia é de baixo risco para a V4 entregar; a meta de venda depende de uma variável fora do controle direto da V4.

## 8. Output para consolidação

Projeção pronta com 3 cenários e premissas explícitas. Objetivo SMART e OKRs do Q3 devem se ancorar no cenário Realista, com o Pessimista como piso de segurança.

## 9. Observações de confiabilidade

Toda a projeção de MQL/Visita/Venda é hipótese extrapolada, não meta confirmada pelo Cliente - marcar como tal na apresentação e pedir validação/commit do Cliente no check-in.
