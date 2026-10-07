---
title: Usar o Decisioning para personalizar ofertas da Web
description: Saiba como usar o Journey Optimizer (AJO) Decisioning para fornecer ofertas personalizadas em uma página da Web aproveitando a segmentação de público incorporada no Experience Platform (AEP).
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00.000Z
jira: KT-17728
exl-id: 382ee746-e8cd-4843-bfe9-913df8914136
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
source-wordcount: '239'
ht-degree: 7%
---
# Usar o Decisioning para personalizar ofertas da Web

Este tutorial se baseia em uma configuração de segmentação de público-alvo criada anteriormente usando o Adobe Experience Platform (AEP) Web SDK. No [tutorial anterior](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/create-audiences-using-web-sdk/introduction), as preferências do usuário, como interesse em Ações, Títulos ou Certificados de Depósito (CDs), foram capturadas e usadas para segmentar indivíduos em públicos-alvo direcionados no Experience Platform. Este tutorial se baseia nessa base usando o Adobe Journey Optimizer (AJO) Decisioning para fornecer ofertas financeiras personalizadas a esses públicos em tempo real, melhorando os resultados de engajamento e conversão.


## Pré-requisitos para este tutorial

* Acesso ao Experience Platform

* Noções básicas sobre conceitos do Experience Platform (Perfis, Públicos-alvo, Conjuntos de dados)

* Familiaridade com o Journey Optimizer

* Conhecimento básico do JavaScript (ler e escrever funções simples)

* Capacidade de usar as DevTools do navegador (guias Console e Rede)


## Meta

Este tutorial o orienta por meio do delivery de ofertas de investimento personalizadas, como Ações, Títulos ou CDs, em um site usando o Journey Optimizer. Ao aproveitar a segmentação de público e as estratégias de decisão, você aprende a garantir que cada visitante veja a oferta mais relevante com base em suas preferências.

## Ferramentas usadas

* Adobe Experience Platform (AEP)
* Adobe Journey Optimizer (AJO)
* Tags do Adobe Experience Platform
* AEP Web SDK (`Alloy.js`)
* Segmentação do AEP Edge
* Uma página da Web para exibir as ofertas
