---
title: Usar o Decisioning para personalizar ofertas da Web
description: Saiba como usar o Journey Optimizer (AJO) Decisioning para fornecer ofertas personalizadas em uma página da Web aproveitando a segmentação de público incorporada no Experience Platform (AEP).
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00Z
jira: KT-17728
exl-id: 382ee746-e8cd-4843-bfe9-913df8914136
source-git-commit: 7d812f589172c5052a1e9bfcf6a99d0769a6c2c7
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 2%

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
