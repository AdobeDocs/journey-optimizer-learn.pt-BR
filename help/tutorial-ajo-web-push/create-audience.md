---
title: Criar público-alvo
description: Defina um segmento no Adobe Experience Platform que direcione os usuários qualificados para receber notificações por push.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00.000Z
jira: KT-20879
exl-id: 427bb35a-d607-48be-845d-9587c4cad86b
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: 66e1fd99-672d-5d64-aa58-eca107f0fbae
    internal-label: Push
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%
---
# Criar público-alvo

Para criar um público-alvo para a campanha, defina um segmento no Adobe Experience Platform que direcione os usuários qualificados a receber notificações por push. Neste tutorial, os usuários que têm uma assinatura de push ativa (o token de push existe), que não recusaram notificações (o sinalizador de Inclui na lista de bloqueios é falso) e estão associados à configuração de aplicativo especificada (o Identificador do aplicativo é igual a `my-first-push`). Esses usuários estão totalmente qualificados para receber notificações por push da Web por meio de campanhas ou jornadas no Adobe Journey Optimizer.Depois de criar o público-alvo, verifique se ele foi avaliado para que os perfis sejam preenchidos e estejam prontos para o direcionamento.
Esse público-alvo é usado na campanha para enviar mensagens de push da Web programadas somente para usuários inscritos.

![criar-público](assets/push-audience.png)
