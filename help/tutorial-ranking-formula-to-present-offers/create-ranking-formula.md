---
title: Criar fórmula de classificação
description: Uma fórmula de classificação no Adobe Journey Optimizer é usada durante o Offer Decisioning, especificamente em uma estratégia de seleção para determinar a ordem de prioridade das ofertas elegíveis.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-30T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-18188
exl-id: eee1b86e-b33f-408e-9faf-90317bc5e861
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: a984631b-2bae-4860-9b15-69c41a799dcb
    internal-label: APIs and SDKs
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
    internal-label: Decisioning API
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%
---
# Criar fórmula de classificação

Uma fórmula de classificação no Adobe Journey Optimizer é usada durante o Offer Decisioning, especificamente em uma estratégia de seleção para determinar a ordem de prioridade das ofertas elegíveis. A fórmula de classificação entra em ação após a filtragem de qualificação, quando várias ofertas se qualificam para um determinado perfil, mas somente a principal (ou algumas) deve ser apresentada com base na lógica de negócios ou no contexto do perfil.

* Fazer logon no Journey Optimizer

* Decisão ->Configuração da estratégia ->Fórmulas de classificação ->Criar fórmula

Fórmula de Classificação
![name_description](assets/formuala-ranking.png)

Um critério em uma fórmula de classificação refere-se a uma regra condicional usada para atribuir uma pontuação a uma oferta. Esses critérios comparam atributos da oferta e o perfil ou contexto para determinar a relevância de uma oferta para um indivíduo específico.



Critério 1

Esta condição filtra os itens de decisão (ofertas) **para incluir apenas** as ofertas marcadas com &quot;IncomeLevel&quot;.
Essas ofertas filtradas prosseguirão para a próxima etapa (como classificação ou entrega) com base na lógica adicional definida.
![critérios_um](assets/income-related-formula.png)


A expressão a seguir é usada para criar a pontuação de classificação

```pql
if(   offer._techmarketingdemos.offerDetails.zipCode = _techmarketingdemos.zipCode,   _techmarketingdemos.annualIncome / 1000 + 10000,   if(     not offer._techmarketingdemos.offerDetails.zipCode,     _techmarketingdemos.annualIncome / 1000,     -9999   ) )
```

O que a Fórmula Faz

* Se a oferta tiver o mesmo CEP do usuário, atribua a ele uma pontuação muito alta para que seja escolhido primeiro.

* Se a oferta não tiver um CEP (é uma oferta geral), atribua a ela uma pontuação normal com base na renda do usuário.

* Se a oferta tiver um CEP diferente do usuário, atribua a ela uma pontuação muito baixa para que não seja selecionada.

Dessa forma, o sistema:

* Sempre tenta mostrar uma oferta correspondente a um ZIP primeiro,

* Retorna a uma oferta geral se nenhuma correspondência for encontrada e evita mostrar ofertas destinadas a outros códigos postais.


Se um item de oferta não atender a nenhum dos critérios de filtro (como não ter a tag &quot;IncomeLevel&quot; ), a oferta receberá uma pontuação de classificação padrão de 10.




