---
title: Criar canal de push
description: A configuração do canal de push define como as notificações por push da Web são entregues, incluindo as configurações do aplicativo e os detalhes específicos da plataforma. Ele também vincula sua configuração de push às credenciais necessárias, como as chaves VAPID, permitindo que o AJO envie notificações para os usuários inscritos.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00Z
jira: KT-20879
source-git-commit: 3d342c5c4de4dda221ce4427b1e4aef7ef8c22cc
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Criar canal de push

A primeira etapa é criar um Canal por push no Adobe Journey Optimizer. Como parte dessa configuração, você precisará gerar chaves VAPID, que são necessárias para autenticar e habilitar as notificações por push da Web. Essas chaves são usadas na configuração do canal de push, permitindo que o AJO envie notificações com segurança para os usuários inscritos.

## Gerar chaves VAPID

VAPID (Voluntary Application Server Identification, Identificação voluntária do servidor de aplicações) é um padrão de push da Web que permite que o servidor se identifique para enviar serviços (como Chrome, Edge etc.) usando pares de chaves públicas/privadas, para que o provedor de push saiba quem está enviando a notificação.

Ele é gerado usando uma ferramenta como web-push generate-vapid-keys, que cria uma chave pública (compartilhada com o navegador) e uma chave privada (mantida em seu servidor) usadas juntas para autenticar e enviar mensagens de push com segurança.

Para este tutorial, usamos Node.js para gerar as chaves VAPID.

Verifique se o Node.js está instalado. Em seguida, execute o seguinte comando
```npm install web-push -g ```

![push-da-Web](assets/install-web-push.png)

```web-push generate-vapid-keys```

![vapid](assets/vapid-keys.png)

## Criar credencial de push

* Fazer logon no Journey Optimizer

* Navegue até Administração | Canais | CONFIGURAÇÕES DE PUSH | Credenciais de push | Criar credencial de push

* ![credencial de push](assets/push-credential.png)

## Criar configuração de canal

* Fazer logon no Journey Optimizer

* Navegue até Administração | Canais | Criar configuração de canal
  ![configuração-canal](assets/push-channel.png)
