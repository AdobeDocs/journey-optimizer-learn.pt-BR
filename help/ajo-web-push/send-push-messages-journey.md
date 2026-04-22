---
title: Enviar mensagens por push em uma jornada
description: O limite de frequência no Adobe Journey Optimizer é aplicado no nível da oferta individual e depende da captura de eventos de impressão e clique na oferta. Isso requer o rastreamento de eventos decisioning.propositionDisplay e decisioning.propositionInteract usando o Adobe Web SDK e mapeando-os para um esquema XDM Experience Event atualizado no Adobe Experience Platform.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00Z
jira: KT-18526
source-git-commit: 3d342c5c4de4dda221ce4427b1e4aef7ef8c22cc
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Enviar mensagens por push em uma jornada

O acionamento de uma jornada com base em um evento de queda de preço permite um engajamento em tempo real e orientado por comportamento com os usuários. Em cenários do mundo real, esse evento normalmente é originado de um sistema de preços de back-end quando o preço de um produto é atualizado. Neste tutorial, simulamos esse comportamento enviando um evento price.drop personalizado pela Camada de dados do Adobe usando Tags da AEP, incluindo detalhes do produto, como nome e SKU. Esse evento é assimilado na Adobe Experience Platform e usado como um acionador de entrada para uma jornada no Adobe Journey Optimizer. Depois de recebida, a jornada pode enviar imediatamente uma notificação por push personalizada para usuários elegíveis, informando-os sobre a queda de preço e incentivando a ação oportuna.

O acionamento de uma jornada usando um evento personalizado envolve as seguintes etapas

## Criação de um evento personalizado no Journey Optimizer

Faça logon no Adobe Journey Optimizer, navegue até Administração → Configurações → Eventos e selecione Criar evento. Crie um novo evento chamado PriceDropEvent e associe-o ao esquema de evento SchemaForPushNotification criado anteriormente no tutorial. Verifique se as propriedades do evento estão configuradas conforme mostrado na imagem de referência.

![propriedades-evento](assets/price-drop-event.png)

No esquema, selecione os campos obrigatórios para disponibilizá-los para personalização. Especificamente, inclua `Name` e `SKU` do objeto ProductListItems, bem como o identificador do identityMap. Esses campos estarão acessíveis no editor de personalização, permitindo que você componha dinamicamente mensagens de notificação por push com base no produto e no contexto do usuário.

## Criação da propriedade de tag

Essa propriedade é configurada com o AEP Web SDK, que está conectado ao WebPushDataStream criado anteriormente no tutorial. A propriedade da tag acompanha o evento price.drop na Camada de dados do Adobe e mapeia os detalhes relevantes do produto atualizando o elemento de dados ProductListItems. Depois que os dados são preparados, uma regra na propriedade da tag é acionada e envia o evento price.drop para a AEP por meio da Web SDK. Esse evento serve como ponto de entrada para uma jornada no Adobe Journey Optimizer, permitindo a entrega imediata de notificações por push com base na queda de preço.



