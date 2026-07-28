# Guardrails - ROPRE Quarter ELEV1 Q2/2026

## Guardrails fixos (padrão da esteira ROPRE do Quarter)

1. Dado ausente vira lacuna explícita - nunca é preenchido por inferência silenciosa.
2. Dado declarado pelo cliente é marcado como `dado declarado pelo cliente`.
3. Inferência é marcada como `hipótese`.
4. Fonte conflitante exige decisão humana - a skill não escolhe sozinha.
5. Projetado vs Realizado overall é obrigatório - sem ele, o fluxo trava.
6. Sem preview aprovado, não existe `ropre-quarter-final.md`.
7. Sem `ropre-quarter-final.md` aprovado, não existe HTML visual.

## Guardrails acionados nesta execução

| Guardrail acionado | Onde | Como foi resolvido |
|---|---|---|
| Fonte conflitante (leads Meta: 446 plataforma vs 417 CRM) | `diagnostico-fontes.md`, `resultados.md` | Felipe decidiu usar o número da plataforma (446) |
| Fonte conflitante (breakeven: 3 leituras divergentes da planilha) | `diagnostico-fontes.md` | 2ª releitura confirmada por repetição (R$ 16.478.179,54); breakeven mensal recalculado via fórmula (Fee+Mídia)/Margem = R$ 131.689,64, cruzado com o deck prévio |
| Projetado vs Realizado overall ausente | `resultados.md` | Felipe informou meta de leads (446) e verba de mídia (maio R$ 15.000 / julho R$ 25.000) |
| Tipo de projeto e canais ativos | Maestro (implícito, já revisado com Felipe na fase de revisão de referências) | Confirmado: inside sales, canais Meta Ads + Google Ads via NEKT |
| Ausência de quarter anterior comparável | Alinhamento inicial (AskUserQuestion) | Felipe decidiu tratar Q2 como 1º quarter operacional, sem Q1 vs Q2 |

## Pausas não acionadas (verificadas e OK)

- Não houve canal pago ativo sem dado suficiente para funil (Meta e Google ambos com dado completo via NEKT).
- Não houve objetivo SMART/OKR sem fonte (todos derivados da projeção).
- Ekyte/timesheet teve dado confiável para entregas (146,6h, 64 tarefas).
