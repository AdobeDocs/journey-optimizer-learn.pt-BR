---
title: Personalização de ofertas de página da Web com o AJO Decisioning com base no público-alvo
description: Saiba como usar o Adobe Journey Optimizer (AJO) Decisioning para fornecer ofertas personalizadas em uma página da Web aproveitando a segmentação de público incorporada no Adobe Experience Platform (AEP).
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00Z
jira: KT-17728
exl-id: 382ee746-e8cd-4843-bfe9-913df8914136
source-git-commit: 5ab637d9b9955ab334ee67ed887e34026b04206d
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---

# Personalização de ofertas de página da Web com o AJO Decisioning com base no público-alvo

Este tutorial se baseia em uma configuração de segmentação de público-alvo criada anteriormente usando o Adobe Experience Platform (AEP) Web SDK. No tutorial anterior, as preferências do usuário — como interesse em ações, títulos ou certificados de depósito (CDs) — foram capturadas e usadas para segmentar indivíduos em públicos-alvo direcionados no Adobe Experience Platform (AEP). Este tutorial se baseia nessa base usando o Adobe Journey Optimizer (AJO) Decisioning para fornecer ofertas financeiras personalizadas a esses públicos em tempo real, melhorando os resultados de engajamento e conversão.

Você pode testar as ofertas personalizadas do AJO ao vivo usando o link abaixo.
[Clique aqui para ver a demonstração ao vivo](https://gbedekar489.github.io/finwise/welcome.html) — a página exibirá ofertas em tempo real com base nas suas preferências de investimento.

## Pré-requisitos para este tutorial

* Acesso ao Adobe Experience Platform

* Noções básicas sobre conceitos do Adobe Experience Platform (Perfis, Públicos-alvo, Conjuntos de dados)

* Familiaridade com o Adobe Journey Optimizer

* Conhecimento básico do JavaScript (ler e escrever funções simples)

* Capacidade de usar as DevTools do navegador (guias Console e Rede)


## META

Este tutorial o orienta por meio da entrega de ofertas de investimento personalizadas, como Ações, Títulos ou CDs, em um site usando o Adobe Journey Optimizer (AJO). Ao aproveitar a segmentação de público e as estratégias de decisão, você aprende a garantir que cada visitante veja a oferta mais relevante com base em suas preferências.

## Ferramentas usadas

* Adobe Experience Platform (AEP)
* Adobe Journey Optimizer (AJO)
* Tags do Adobe Experience Platform
* AEP Web SDK (Alloy.js)
* Segmentação do AEP Edge
* Uma página da Web para exibir as ofertas
