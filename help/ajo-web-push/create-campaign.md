---
title: Criar campanha
description: Crie uma campanha para direcionar os usuários que optaram por receber notificações por push e entregar a mensagem no horário agendado.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
exl-id: 94fda23f-e26a-494b-8e5c-6c442bae61c4
source-git-commit: c339fe796af1e691cd3b1c98cd6ba8a8772551e4
workflow-type: tm+mt
source-wordcount: '208'
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

Para testar a campanha, primeiro habilite as notificações na [página da Web optando por &#x200B;](http://localhost:3000) quando solicitado. Depois de aceitar, aguarde a campanha ser executada no horário agendado. Quando a campanha for executada, você deverá receber a notificação por push em seu navegador.
