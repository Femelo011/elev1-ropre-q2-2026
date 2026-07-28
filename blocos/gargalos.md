# Gargalos - ROPRE Quarter

## 1. Escopo do bloco

- **Cliente/projeto:** ELEV1 - Elevate Incorporadora (Elevate Majestic).
- **Quarter analisado:** Q2/2026.
- **Quarter seguinte:** Q3/2026.
- **Objetivo deste bloco:** identificar a restrição principal do quarter e os gargalos secundários, com evidência quantitativa por camada do funil.

## 2. Fontes consultadas

| Fonte | Status | Observação |
|---|---|---|
| `blocos/resultados.md` (já consolidado) | OK | Base quantitativa deste bloco |
| Retrospectiva ELEV | Revisado (sessão anterior) | Fonte dos achados de CRM (leads abandonados, automação de cancelamento, breakeven desatualizado) |
| NEKT Meta/Google | OK | Confirma que aquisição e conversão inicial (lead) estão saudáveis - gargalo não está aí |

## 3. Dados encontrados

Funil Q2 (de `resultados.md`): 450 leads (mídia) → 421 leads (CRM) → 50 MQL (11,9%) → 4 visitas/SQL (8,0%) → 1 venda (25,0%). Compondo Lead→Visita: **0,95%** - a queda mais severa da cadeia, de longe.

Achados de CRM (retrospectiva ELEV, não re-apurados nesta sessão, tratados como já validados):
- 238 leads abandonados no CRM, auditoria aberta em 19/06 sem resultado até 30/06.
- 76% (186/413) dos leads marcados "NÃO QUALIFICADO" - sem decomposição por motivo/origem/vendedor.
- Automação de cancelamento indevida no CRM, corrigida só em 25/06 - impacto quantitativo sobre quantos leads válidos foram descartados por engano ainda é desconhecido.
- Breakeven desatualizado o quarter inteiro (task de atualização só aberta em 10/06).
- Google Ads: maio teve um sub-período "cego" de tracking (~R$ 2.522 investidos sem lead rastreado), somado à ineficiência geral do canal (CPL R$ 1.096 vs Meta R$ 70 - 15,7x mais caro).

## 4. Dados consolidados

### Restrição principal do quarter

- **Restrição:** conversão Lead → Visita de 0,95% (MQL→Visita especificamente em 8,0%, o pior degrau da cadeia).
- **Evidência:** de 421 leads no CRM e 50 MQL qualificados, apenas 4 chegaram a visita agendada/realizada - mesmo com a mídia entregando o público certo (71% homens 35-54, afluentes, via Meta a CPL estável R$ 66-70) e batendo a meta de leads do quarter (446 = 446).
- **Causa provável:** falha operacional na cadência de contato/agendamento pós-MQL, agravada por (a) 238 leads abandonados sem contato registrado, (b) critério de qualificação que descarta 76% dos leads como "não qualificado" sem decomposição de motivo - o que pode estar descartando leads recuperáveis, não só leads de má qualidade, e (c) automação de cancelamento indevida ativa até 25/06, que pode ter fechado leads válidos por engano em parte do quarter.
- **Confiança:** média-alta - o sintoma (0,95%) está bem evidenciado por múltiplas fontes cruzadas (deck, retro, mídia); a causa raiz específica (qual dos três fatores pesa mais) ainda não foi decomposta quantitativamente.
- **Validação humana:** pendente.

### Gargalos secundários

| Gargalo | Camada | Evidência | Impacto | Hipótese | Ação sugerida | Prioridade |
|---|---|---|---|---|---|---|
| 238 leads abandonados sem contato no CRM | Comercial/Visibilidade | Auditoria aberta 19/06, sem resultado até 30/06 (fim do quarter) | Alto - pode conter parte dos leads que explicariam a queda MQL→Visita | Falta de SLA formal de contato/agendamento após qualificação | Fechar a auditoria dos 238 leads abandonados e implantar SLA de contato com prazo definido | 1 |
| 76% dos leads marcados "NÃO QUALIFICADO" sem motivo decomposto | Qualificação | 186/413 leads (retro) | Alto - pode mascarar tanto problema de qualidade de tráfego quanto critério excessivamente restritivo | Critério de qualificação manual/subjetivo sem padronização de motivo | Implantar campo obrigatório de "motivo de desqualificação" no CRM e auditar uma amostra manualmente | 2 |
| Automação de cancelamento indevida no CRM | Visibilidade/Operação | Corrigida só em 25/06 (retro) | Médio-alto, mas não quantificado | Falha de configuração de automação, não intencional | Levantar quantos leads foram cancelados indevidamente entre início do quarter e 25/06, e tentar reativar os recuperáveis | 3 |
| Google Ads 15,7x mais caro que Meta (CPL R$ 1.096 vs R$ 70), com sub-período sem tracking em maio | Aquisição/Conversão inicial | R$ 4.384,76 investidos, só 4 conversões no Q2 (fonte NEKT) | Baixo em valor absoluto (12% da verba), mas ineficiente | Campanhas de Search genéricas competindo com Meta muito mais barato para o mesmo público | Reduzir ou realocar verba de Google Search para Meta enquanto o tracking de Search não for resolvido, ou revisar a estratégia de keyword | 4 |
| Breakeven desatualizado o quarter inteiro | Visibilidade | Task de atualização aberta só em 10/06 (retro) | Médio - limita a capacidade de decisão financeira em tempo real durante o quarter | Processo de atualização não priorizado/lembrado | Definir cadência fixa de atualização do breakeven (ex.: toda virada de mês) | 5 |
| MQL/SQL mês a mês (abril e junho) sem fonte confiável fora do Growth Pack | Visibilidade | Só maio está "fechado" na planilha de breakeven (ver `resultados.md`) | Médio - limita a granularidade de acompanhamento intra-quarter | Growth Pack não foi consultado diretamente nesta sessão (link não fornecido) | Conectar a leitura direta do Growth Pack (aba "2.2 Acompanhamento Mensal") no próximo ciclo | 6 |

## 5. Lacunas

| Lacuna | Impacto | Decisão necessária |
|---|---|---|
| Decomposição da causa raiz da restrição principal (qual dos 3 fatores pesa mais: SLA, critério de qualificação, ou automação indevida) | Plano de ação pode acabar atacando os 3 ao mesmo tempo sem saber o de maior alavancagem | Aceitar atacar os 3 em paralelo (são baratos de corrigir) ou pedir ao cliente uma decomposição manual da amostra de 238 leads abandonados antes do plano de ação |

## 6. Conflitos

Nenhum conflito novo identificado neste bloco - os achados de CRM vêm de uma única fonte (retrospectiva ELEV), sem contraponto a outra fonte estruturada.

## 7. Análise

O quarter tem uma característica pouco comum e importante para a narrativa do ROPRE: a mídia não é o problema. Ela entrega volume dentro da meta, ao público certo, a custo estável mesmo escalando 10,8x. O gargalo está inteiramente na camada comercial/CRM pós-lead, e há evidência concreta de três causas operacionais específicas (não hipóteses vagas) que compõem esse gargalo: leads abandonados sem contato, critério de qualificação sem decomposição de motivo, e uma automação de cancelamento que rodou errada por boa parte do quarter. Isso torna o plano de ação natural: as ações não são de mídia, são de CRM/operação comercial - e majoritariamente de responsabilidade do Cliente (time comercial/CRM), não da V4.

## 8. Output para consolidação

- Restrição principal: Lead→Visita (0,95%), causa provável tripla (CRM abandono + qualificação sem motivo + automação indevida).
- 6 gargalos secundários priorizados, prontos para gerar o plano 5W1H.

## 9. Observações de confiabilidade

- Sintoma (conversão baixa) tem alta confiança, cruzado por múltiplas fontes.
- Causa raiz tem confiança média - decomposta em hipóteses plausíveis e evidenciadas, mas sem quantificação exata de qual pesa mais.
