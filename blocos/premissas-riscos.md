# Premissas e Riscos - ROPRE Quarter

## 1. Escopo do bloco

- **Cliente/projeto:** ELEV1 - Elevate Incorporadora (Elevate Majestic).
- **Quarter seguinte:** Q3/2026.
- **Objetivo deste bloco:** registrar as premissas que sustentam a projeção/objetivo do Q3 e os riscos associados, com dono e plano de resposta.

## 2. Fontes consultadas

`blocos/plano-acao.md`, `blocos/projecao-proximo-quarter.md`, `blocos/gargalos.md`.

## 3-4. Dados consolidados

| Tipo | Premissa | Risco se falhar | Sinal de alerta | Plano de resposta | Dono |
|---|---|---|---|---|---|
| Comercial | Cliente audita e reativa os 238 leads abandonados no CRM ainda no Q3 | Gargalo Lead→Visita persiste; projeção cai para o cenário Pessimista (2 vendas em vez de 3-4) | Nenhuma atualização de status dos 238 leads até metade de julho | Escalar via CS; revisar objetivo do quarter para o cenário Pessimista | Cliente (comercial) |
| Comercial | Cliente padroniza campo de "motivo de desqualificação" no CRM | Taxa de 76% "não qualificado" continua opaca, sem diagnóstico se é tráfego ou processo | Campo não implementado até final de julho | V4 oferece apoio de configuração/consultoria de CRM | Cliente |
| Dados | Automação de cancelamento indevida (corrigida 25/06) não volta a ocorrer | Nova falha descarta leads válidos sem detecção | Queda abrupta e não explicada de leads ativos no CRM | QA mensal da automação de CRM | Cliente (CRM) / V4 (acompanhamento) |
| Mídia | Verba de R$ 25.000/mês se mantém estável nos 3 meses do Q3 (só julho foi formalmente confirmado) | Volume de lead cai proporcionalmente se a verba cair em agosto/setembro | Budget mensal divergente do combinado | Replanejar a projeção assim que houver confirmação mensal | V4 / Cliente (financeiro) |
| Cliente | Elevate Praiê permanece fora do funil do Q3 (pré-lançamento) ou entra com go/no-go formalmente comunicado | Funil fica misto sem preparo prévio de tracking/CRM se Praiê entrar sem aviso | Início de mídia/CRM para Praiê sem handoff formal | Pedir confirmação de go/no-go com antecedência mínima de 2 semanas | Cliente |
| Operação V4 | Breakeven passa a ser atualizado mensalmente a partir do Q3 (ação 2 do plano) | Decisão financeira do Cliente fica descolada da realidade, como ocorreu no Q2 | Mês fecha sem atualização registrada | Checkpoint fixo de CS na virada do mês | V4 |

## 5. Lacunas

Nenhuma nova além das já registradas em `projecao-proximo-quarter.md`.

## 6. Conflitos

Nenhum.

## 7. Análise

Das 6 premissas, 4 têm dono no Cliente (comercial/CRM/financeiro) e só 2 têm dono primário na V4 (mídia estável, breakeven atualizado) - reforça o padrão já identificado no plano de ação: o risco do Q3 está concentrado na execução do Cliente, não na entrega de mídia.

## 8. Output para consolidação

6 premissas/riscos prontos, todas com dono e plano de resposta.

## 9. Observações de confiabilidade

Alta - premissas derivadas diretamente de gargalos e ações já evidenciados, não são hipóteses novas.
