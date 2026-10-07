---
title: Implementar o limite de frequência em ofertas do Adobe Journey Optimizer (AJO) fornecidas pelo AJO Decisioning
description: Este tutorial estende uma implementação existente do Adobe Journey Optimizer (AJO) habilitando o limite de frequência em ofertas fornecidas com o AJO Decisioning. Ele descreve como capturar eventos de impressão e interação usados no limite de frequência.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00.000Z
jira: KT-18526
exl-id: ae74485f-9ea1-428d-9c07-5db0c5cf93fb
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
source-wordcount: '214'
ht-degree: 7%
---
# Implementar o limite de frequência em ofertas do Adobe Journey Optimizer (AJO) fornecidas pelo AJO Decisioning

Este tutorial demonstra como aplicar o limite de frequência a ofertas no Adobe Journey Optimizer para controlar a frequência com que os usuários veem a mesma oferta ao longo do tempo.

Este tutorial presume que você já configurou uma campanha do AJO seguindo o [tutorial sobre como personalizar ofertas com base nas condições meteorológicas](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/introduction)

Ao capturar eventos decisioning.propositionDisplay e decisioning.propositionInteract por meio do Adobe Web SDK e mapeá-los para esquemas XDM no Adobe Experience Platform (AEP), o Adobe Journey Optimizer pode rastrear com precisão as impressões e interações da oferta, permitindo o limite de frequência para limitar a frequência com que uma oferta é exibida a um usuário.

## Pré-requisitos para este tutorial

Antes de continuar, verifique se você tem uma campanha válida do Adobe Journey Optimizer usando a Decisão que está oferecendo ofertas ativamente em uma superfície da Web.

Este tutorial presume que o delivery de ofertas já está funcionando e se concentra exclusivamente na configuração e validação do comportamento de limite de frequência.




