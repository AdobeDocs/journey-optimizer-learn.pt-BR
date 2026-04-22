---
title: Criar sequência de dados
description: Esta página orienta você na criação de um fluxo de dados no Adobe Experience Platform, que é necessário para coletar dados do Web SDK e roteá-los para o AEP e o Adobe Journey Optimizer. A sequência de dados atua como a conexão entre o aplicativo web e os serviços da Adobe, permitindo que a subscrição por push e os dados do evento sejam processados.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 45f86aeb8fca071436785cc55225d853bb21998f
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Criar sequência de dados

Uma sequência de dados no Adobe Experience Platform (AEP) atua como o endpoint que recebe dados enviados do Web SDK. Ele roteia esses dados para serviços configurados, como AEP, Adobe Analytics ou Adobe Journey Optimizer. Neste tutorial, a sequência de dados é usada para enviar dados de assinatura push da Web e eventos price.drop para ativação no AEP.

## Criar esquema de evento para rastrear notificações por push

Crie um novo esquema XDM ExperienceEvent chamado `SchemaForPushNotification`. Adicionar os grupos de campos `Push Notification Tracking` e `Commerce Details` a este esquema. Os campos do grupo de campos Detalhes do Commerce serão usados para capturar informações do produto e acionar o evento price.drop personalizado.

![esquema-evento](assets/event-schema.png)

## Criar esquema de perfil para salvar o consentimento do usuário

Para este tutorial, usamos o `AJO Push Profile Schema` pronto para uso. Este esquema armazena os detalhes da assinatura push do usuário, incluindo o token push necessário para fornecer notificações por push na Web.

![perfil_esquema](assets/profile-schema.png)

## Criar conjuntos de dados para o esquema

Crie um conjunto de dados chamado `DataSetForPushNotification` usando o esquema de evento criado anteriormente. Para dados de perfil, use o `AJO Push Profile Dataset` pronto para uso, que está associado ao esquema de perfil de push. Anote a ID `DataSetForPushNotification`, que será necessária posteriormente no tutorial ao configurar o aplicativo por meio do arquivo .env.

## Criar sequência de dados usando o evento e o conjunto de dados do perfil

Crie um novo fluxo de dados chamado WebPushDataStream usando os conjuntos de dados de evento e perfil criados na etapa anterior. Anote a ID de sequência de dados, pois ela será necessária posteriormente no tutorial ao configurar o aplicativo por meio do arquivo .env.

![sequência de dados](assets/datastream.png)
