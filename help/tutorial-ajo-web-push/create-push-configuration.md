---
title: Criar canal de push
description: A configuração do canal de push define como as notificações por push da Web são entregues, incluindo as configurações do aplicativo e os detalhes específicos da plataforma. Ele também vincula sua configuração de push às credenciais necessárias, como as chaves VAPID, permitindo que o AJO envie notificações para os usuários inscritos.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00.000Z
jira: KT-20879
exl-id: 0a8be7eb-9962-466a-9fcc-022cb84c7b0a
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: a984631b-2bae-4860-9b15-69c41a799dcb
    internal-label: APIs and SDKs
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
    internal-label: Decisioning API
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%
---
# Criar canal de push

A primeira etapa é criar um Canal por push no Adobe Journey Optimizer. Como parte dessa configuração, você precisará gerar chaves VAPID, que são necessárias para autenticar e habilitar as notificações por push da Web. Essas chaves são usadas na configuração do canal de push, permitindo que o AJO envie notificações com segurança para os usuários inscritos.

## Gerar chaves VAPID

VAPID (Voluntary Application Server Identification, identificação voluntária do servidor de aplicativos) é um padrão de push da Web que permite que o servidor se identifique para enviar serviços (como Chrome, Edge etc.) usando pares de chaves públicas/privadas, para que o provedor de push saiba quem está enviando a notificação.

Ele é gerado usando uma ferramenta como web-push generate-vapid-keys, que cria uma chave pública (compartilhada com o navegador) e uma chave privada (mantida em seu servidor) usadas juntas para autenticar e enviar mensagens de push com segurança.

Para este tutorial, usamos Node.js para gerar as chaves VAPID.

Verifique se o Node.js está instalado. Em seguida, execute o seguinte comando

`npm install web-push -g `

![push-da-Web](assets/install-web-push.png)

`web-push generate-vapid-keys`

![vapid](assets/vapid-keys.png)

## Criar credencial de push

* Fazer logon no Journey Optimizer

* Navegue até Administração | Canais | CONFIGURAÇÕES DE PUSH | Credenciais por push| Criar credencial por push

* ![credencial de push](assets/push-credential.png)

## Criar configuração de canal

* Fazer logon no Journey Optimizer

* Navegue até Administração | Canais | Criar configuração de canal
  ![configuração-canal](assets/push-channel.png)
