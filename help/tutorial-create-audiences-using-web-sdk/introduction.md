---
title: Criar públicos usando o Web SDK
description: Neste tutorial, você aprenderá a capturar as preferências do usuário por meio de um formulário web, enviar esses dados para o Adobe Experience Platform (AEP) em tempo real e qualificar usuários dinamicamente em públicos-alvo direcionados com base em suas seleções. Ao combinar Tags do Adobe (Launch), o AEP Web SDK (Alloy.js) e a Segmentação do Edge, você permite oportunidades imediatas de personalização para clientes interessados em Ações, Títulos ou Certificados de depósito (CDs).
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00.000Z
jira: KT-17923
exl-id: ebaa3aa5-0a08-43fd-8d06-8e4b5d8dee05
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d2971708-e780-44bb-9e2a-72f139796afd
    internal-label: Customer
subfeature_v2:
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%
---
# Criar públicos usando o Web SDK

Neste tutorial, você aprenderá a capturar as preferências do usuário por meio de um formulário web, enviar esses dados para o Adobe Experience Platform (AEP) em tempo real e qualificar usuários dinamicamente em públicos-alvo direcionados com base em suas seleções. Ao combinar Tags do Adobe (Launch), o AEP Web SDK (Alloy.js) e a Segmentação do Edge, você permite oportunidades imediatas de personalização para clientes interessados em Ações, Títulos ou Certificados de depósito (CDs).

## Pré-requisitos para este tutorial

* Acesso ao Adobe Experience Platform

* Noções básicas sobre conceitos do Adobe Experience Platform (Perfis, Públicos-alvo, Conjuntos de dados)

* Familiaridade com tags do Adobe (Launch) — configuração de elementos de dados e regras

* Conhecimento básico do JavaScript (ler e escrever funções simples)

* Capacidade de usar DevTools do navegador (guias Console e Rede)


## META

O objetivo deste tutorial é criar e qualificar três públicos-alvo distintos no Adobe Experience Platform (AEP):

* Clientes interessados em Ações

* Clientes interessados em Títulos

* Clientes interessados em CDs

Os usuários enviam suas preferências por meio de um formulário da Web e essas preferências são assimiladas por meio do AEP Web SDK usando o Adobe Launch, permitindo a qualificação de público-alvo em tempo real.

## Ferramentas usadas

* Adobe Experience Platform (AEP)

* Tags do Adobe Experience Platform

* AEP Web SDK (Alloy.js)

* Segmentação do AEP Edge

* Uma página da Web com um formulário de preferência
