---
title: Capturar permissão do usuário
description: Criar página da Web para capturar o consentimento do usuário para receber notificações por push.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00.000Z
jira: KT-20879
exl-id: 5897420a-7488-4d48-b56c-86a53d1d2395
TQID: 'https://experienceleague.adobe.com/O5xiLJ7UOQNYSkfpCa2umhCkxt1cKILsO4fOKxtVifM'
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
    internal-label: Configuration
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
    internal-label: Journeys
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
source-wordcount: '219'
ht-degree: 0%
---
# Capturar permissão do usuário

Esta página da Web captura o consentimento do usuário para receber notificações por push. Ele solicita que o usuário ative notificações usando a API de notificações do navegador e, após a aceitação, registra a subscrição de push com o Adobe Experience Platform usando a Web SDK. Isso garante que somente os usuários aceitos possam receber notificações por push por meio de campanhas e jornadas no Adobe Journey Optimizer.

Para ativar as notificações por push da Web, a página primeiro carrega um arquivo de configuração chamando fetch(&quot;/config&quot;) dentro de uma função de inicialização. Essa configuração é fornecida por um aplicativo Node.js e inclui valores-chave, como ID de sequência de dados, ID da organização, chave pública VAPID, ID do aplicativo e ID do conjunto de dados de rastreamento. Depois que a configuração é carregada, o Adobe Web SDK é inicializado e o service worker é registrado para dar suporte a mensagens de push. Quando um usuário clica em Ativar notificações, o navegador solicita permissão usando a API de notificações da Web. Se a permissão for concedida, o Web SDK enviará a assinatura por push para o Adobe Experience Platform e o usuário será marcado como aceito por 24 horas para evitar prompts repetidos. Você pode experimentar esse fluxo na página da Web local shop-smart.html incluída no [aplicativo de amostra](http://localhost:3000/) após iniciar o servidor.

![solicitação-permissões](assets/request-notifications.png)
