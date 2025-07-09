---
title: Captura de interações de oferta com o Adobe Web SDK para treinamento do modelo de IA
description: Este artigo se concentra na captura de dados de interação do usuário — como impressões de ofertas e cliques — usando o Adobe Experience Platform Web SDK (alloy.js). Esses dados servem como base para treinar modelos de IA no Adobe Journey Optimizer (AJO) para classificar ofertas de forma inteligente com base no comportamento do usuário e em sinais contextuais.
feature: Decisioning
topic: Integrations
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2025-07-08T00:00:00Z
jira: KT-18451
source-git-commit: dfb280df3453e7811dffd95b9af664b873a9af31
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---


# Captura de interações de oferta com o Adobe Web SDK para treinamento do modelo de IA

Este artigo demonstra como capturar eventos de interação de oferta (como impressões ou cliques) usando o Adobe Experience Platform Web SDK chamando alloy(&quot;sendEvent&quot;, ...) diretamente no código JavaScript. Os dados serão assimilados na AEP e usados para treinar modelos de IA no Adobe Journey Optimizer (AJO) para uma classificação de ofertas mais inteligente com base no comportamento em tempo real.

## Pré-requisitos

Antes de começar, verifique se o seguinte está em vigor:

- Uma propriedade do Adobe Launch em funcionamento com a extensão Adobe Experience Platform Web SDK instalada.

- Uma [sequência de dados](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/decisioning/experience-decisioning/collect-event-data/create-dataset) configurada e mapeada para a sandbox da AEP.

- Um site em que o Launch é implantado.


## Criar esquema e conjunto de dados para eventos de interação de oferta

Para coletar eventos de experiência, primeiro é necessário criar um conjunto de dados para onde esses eventos serão enviados.

Siga as etapas mencionadas neste [artigo para criar o esquema e o conjunto de dados necessários](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/decisioning/experience-decisioning/collect-event-data/create-dataset)

## Criar uma sequência de dados no AEP

![fluxo de dados](assets/ai-model-data-stream.png)
Adicionar o serviço Adobe Experience Platform à sequência de dados
![serviço-fluxo-dados](assets/data-stream-service.png)

## Configurar a tag do Adobe Experience Platform com o Web SDK

Nas configurações de extensão:

Configurar a extensão Adobe Experience Platform Web SDK para usar o fluxo de dados criado
