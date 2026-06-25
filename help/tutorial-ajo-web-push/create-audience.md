---
title: Criar público-alvo
description: Defina um segmento no Adobe Experience Platform que direcione os usuários qualificados para receber notificações por push.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
exl-id: 427bb35a-d607-48be-845d-9587c4cad86b
source-git-commit: 676c21ca09e0df8d404b05081d71b147755d65d5
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 9%

---

# Criar público-alvo

Para criar um público-alvo para a campanha, defina um segmento no Adobe Experience Platform que direcione os usuários qualificados a receber notificações por push. Neste tutorial, os usuários que têm uma assinatura de push ativa (o token de push existe), que não recusaram notificações (o sinalizador de Inclui na lista de bloqueios é falso) e estão associados à configuração de aplicativo especificada (o Identificador do aplicativo é igual a `my-first-push`). Esses usuários estão totalmente qualificados para receber notificações por push da Web por meio de campanhas ou jornadas no Adobe Journey Optimizer.Depois de criar o público-alvo, verifique se ele foi avaliado para que os perfis sejam preenchidos e estejam prontos para o direcionamento.
Esse público-alvo é usado na campanha para enviar mensagens de push da Web programadas somente para usuários inscritos.

![criar-público](assets/push-audience.png)
