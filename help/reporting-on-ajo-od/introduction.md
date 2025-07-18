---
title: Rastrear e relatar ofertas do Adobe Journey Optimizer (AJO) entregues via AJO Offer Decisioning
description: Este tutorial estende uma implementação existente do Adobe Journey Optimizer (AJO) que fornece ofertas personalizadas com base em dados contextuais, como temperatura. Ele descreve como capturar eventos de impressão e interação e preparar os dados para relatórios no Journey Optimizer.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-07-18T00:00:00Z
jira: KT-18526
source-git-commit: 23832f2e59ca7558fd403f0a9753db3923023e6d
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Rastrear e relatar ofertas do Adobe Journey Optimizer (AJO) entregues via AJO Offer Decisioning

Esse caso de uso se concentra em permitir a emissão de relatórios e a análise de desempenho para ofertas entregues por meio do Adobe Journey Optimizer (AJO). Quando as ofertas são personalizadas e entregues com base em sinais contextuais (como clima ou localização), é essencial rastrear as impressões e as interações do usuário para avaliar sua eficácia.

Ao capturar eventos decisioning.propositionDisplay e decisioning.propositionInteract por meio do Adobe Web SDK e mapeá-los para esquemas XDM estruturados no Adobe Experience Platform (AEP), os dados de envolvimento no nível da oferta ficam disponíveis para análise. Esses dados podem ser usados no Customer Journey Analytics (CJA) para criar painéis, medir métricas principais, como a taxa de cliques (CTR), e comparar o desempenho da oferta em diferentes segmentos de público-alvo e condições contextuais.

O objetivo é fornecer insights claros e orientados por dados sobre o desempenho das ofertas personalizadas e informar sobre estratégias de decisão futuras.




![painel-de-relatórios](assets/dashboard-reporting.png)



## Pré-requisitos para este tutorial

Antes de começar, complete o [tutorial Personalizar Ofertas com Dados Climáticos em Tempo Real.](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/introduction) Estabelece todos os componentes fundamentais, incluindo:

- Integração com o Web SDK

- Configuração de oferta no Adobe Journey Optimizer (AJO)

- Decisão usando atributos contextuais, como clima e temperatura

- Renderização da oferta em tempo real em uma página da Web

Este tutorial se baseia diretamente nessa implementação e se concentra especificamente na captura de impressões e interações de ofertas para relatórios e análises no Journey Optimizer.

