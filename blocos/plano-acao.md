# Plano de Ação 5W1H - ROPRE Quarter

## 1. Escopo do bloco

- **Cliente/projeto:** ELEV1 - Elevate Incorporadora (Elevate Majestic).
- **Quarter analisado:** Q2/2026 → ações para Q3/2026.
- **Objetivo deste bloco:** transformar os gargalos identificados em ações priorizadas por Score = Impacto/(Esforço+Dependência), atacando causa provável, não sintoma.

## 2. Fontes consultadas

| Fonte | Status | Observação |
|---|---|---|
| `blocos/gargalos.md` | OK | Base de todas as 6 ações |

## 3. Dados encontrados

Ver `gargalos.md` - restrição principal (Lead→Visita 0,95%) com causa tripla (CRM abandono + qualificação sem motivo + automação indevida), mais 3 gargalos secundários (Google ineficiente, breakeven desatualizado, granularidade mensal do funil).

## 4. Dados consolidados / Plano principal

| Prioridade | Gap | Restrição/Causa Provável | What | Why | Where | When | Who | How | Esforço | Impacto | Dependência | Score |
|---:|---|---|---|---|---|---|---|---|---:|---:|---:|---:|
| 1 | Mídia entrega o público certo mas os criativos campeões não estão isolados/escalados | Oportunidade, não gargalo - "AD04 Zoom na terra" e "AD02 Alto padrão" performam em toda campanha onde aparecem | Escalar os 2 criativos-vídeo campeões em campanhas dedicadas isoladas, com verba própria | Concentrar verba onde já há prova de eficiência, em vez de diluir em 9 campanhas com variações do mesmo público | Meta Ads | Início Q3 | V4 (mídia) | Duplicar os 2 criativos em campanha isolada por público de maior volume (Lookalike 1%, Carros de luxo), manter budget CBO nas demais | 1 | 4 | 1 | 2,00 |
| 2 | Breakeven desatualizado o quarter inteiro + MQL/SQL mensal sem fonte confiável | Falta de cadência de atualização e de conexão direta com o Growth Pack | Definir cadência fixa de atualização do breakeven (toda virada de mês) e conectar leitura direta do Growth Pack (aba "2.2 Acompanhamento Mensal") no ciclo de reporte | Sem isso, decisão financeira e leitura mensal do funil comercial ficam sempre atrasadas/incompletas | Planilha breakeven + Growth Pack | Início Q3 | V4 (CS/Growth) | Agendar checkpoint mensal fixo de atualização; pedir link direto do Growth Pack ao time Invictus | 1 | 3 | 2 | 1,00 |
| 3 | 238 leads abandonados sem contato + SLA de agendamento ausente | Restrição principal - falha operacional de cadência de contato pós-lead | Fechar a auditoria dos 238 leads abandonados (reativar os recuperáveis) e implantar SLA formal de contato/agendamento (prazo máximo definido por etapa) | É o maior gargalo do funil (Lead→Visita 0,95%) e a causa mais diretamente acionável | CRM do Cliente | Q3, primeiras 3 semanas | **Cliente** (time comercial) | Auditoria manual da base de 238 + definição de SLA com alertas automáticos no CRM | 3 | 5 | 4 | 0,71 |
| 4 | 76% dos leads marcados "NÃO QUALIFICADO" sem motivo decomposto | Restrição principal - critério de qualificação sem padronização, pode estar descartando leads recuperáveis | Implantar campo obrigatório de "motivo de desqualificação" no CRM e auditar uma amostra dos "não qualificados" para separar má qualidade de tráfego vs. critério excessivo | Sem saber o motivo, não dá para saber se o problema é tráfego ou processo comercial | CRM do Cliente | Q3, primeiras 4 semanas | **Cliente** (time comercial) | Campo novo obrigatório + revisão manual de amostra de ~50 leads "não qualificados" | 2 | 4 | 4 | 0,67 |
| 5 | Automação de cancelamento indevida (corrigida 25/06) | Restrição principal - parte dos leads pode ter sido descartada por erro de automação, não por qualidade | Levantar quantos leads foram cancelados indevidamente entre início do quarter e 25/06, e tentar reativar os recuperáveis | Corrigir o sintoma retroativo antes de assumir que a causa foi só qualidade de lead/CRM | CRM do Cliente | Q3, primeira quinzena | **Cliente** (CRM) | Query/relatório de leads cancelados pela automação no período, reclassificação manual | 2 | 3 | 3 | 0,60 |
| 6 | Google Ads 15,7x mais caro que Meta, com sub-período sem tracking em maio | Ineficiência de canal secundário - baixo volume, mas mal aproveitado | Revisar estratégia de keyword (pausar termos genéricos de baixo CPA) e corrigir o gap de tracking de maio antes de decidir se mantém ou reduz o canal | Verba pequena (12% do total) mas 15,7x menos eficiente que Meta - vale correção rápida ou realocação | Google Ads | Início Q3 | V4 (mídia) | Pausar keywords sem conversão no Q2, validar tag de conversão, reavaliar em 30 dias | 2 | 2 | 2 | 0,50 |

Score recalculado automaticamente = Impacto / (Esforço + Dependência). Nenhuma ação é puramente paliativa - todas atacam causa provável ou uma oportunidade validada, não só sintoma.

## 5. Lacunas

| Lacuna | Impacto | Decisão necessária |
|---|---|---|
| Ações 3, 4 e 5 (CRM) dependem inteiramente de execução do Cliente, não da V4 | Risco de as ações de maior impacto na restrição principal não avançarem no ritmo esperado | Validar com o Cliente se há capacidade/dono definido para essas 3 ações antes de comprometer a projeção do Q3 com elas |

## 6. Conflitos

Nenhum.

## 7. Análise

O plano tem um padrão claro: a ação de maior Score (2,00) é uma ação de mídia rápida e de baixa dependência - escalar os criativos que já provaram funcionar. As três ações que atacam a restrição principal (Lead→Visita) têm Score menor não porque sejam menos importantes, mas porque dependem inteiramente de execução do Cliente no CRM/comercial (dependência 3-4) - a V4 não tem alavanca direta ali além de cobrar e acompanhar. Isso deve ficar explícito na apresentação ao cliente: o maior gargalo do quarter é dele, não da mídia.

## 8. Output para consolidação

6 ações priorizadas por Score, prontas para gerar a Projeção do Q3 (a ação 1, de baixo esforço e alto impacto, já pode ser assumida na projeção; as ações 3-5 são premissa/risco condicionado ao Cliente).

## 9. Observações de confiabilidade

Esforço/Impacto/Dependência atribuídos por estimativa própria (sem benchmark do cliente) - sujeitos a validação humana, conforme padrão do ROPRE.
