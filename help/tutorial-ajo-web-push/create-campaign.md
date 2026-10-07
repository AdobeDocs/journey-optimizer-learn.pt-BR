---
title: Criar campanha
description: Crie uma campanha para direcionar os usuários que optaram por receber notificações por push e entregar a mensagem no horário agendado.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00.000Z
jira: KT-20879
exl-id: 94fda23f-e26a-494b-8e5c-6c442bae61c4
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
source-wordcount: '218'
ht-degree: 1%
---
# Criar campanha

Nesta etapa, você criará uma campanha no Adobe Journey Optimizer para enviar notificações por push agendadas da Web aos usuários que aceitaram. A campanha é direcionada a um público elegível e entrega mensagens em um horário predefinido, permitindo um engajamento planejado e baseado no público.

* Fazer logon no Journey Optimizer
* Navegue até Gerenciamento de Jornadas | Campanhas | Criar campanhas

## Especificar Configurações de Campanha

Especificar o nome da campanha

![nome-da-campanha](assets/campign-push-notification.png)

## Associar ação à campanha

Associar a configuração de canal de push criada anteriormente neste tutorial

![ação-campanha](assets/campign-push-notification-action.png)

## Associar público-alvo à campanha

Associar a audiência `AudienceForPush` à campanha

![público-alvo](assets/campign-push-notification-audience.png)

## Criar conteúdo para a notificação por push

Crie conteúdo básico de push para testar a notificação por push. Especifique o título e o corpo da mensagem conforme mostrado abaixo

![notificação de conteúdo por push](assets/campign-push-notification-content.png)

## Agendar a campanha

Programe a campanha de acordo com suas necessidades

![campanha-agendada](assets/campign-push-notification-schedule.png)

Por fim, ative a campanha.

## Testar a campanha

Para testar a campanha, primeiro habilite as notificações na [página da Web optando por ](http://localhost:3000) quando solicitado. Depois de aceitar, aguarde a campanha ser executada no horário agendado. Quando a campanha for executada, você deverá receber a notificação por push em seu navegador.
