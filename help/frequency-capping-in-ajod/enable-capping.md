---
title: Ativar o limite de frequência para uma campanha do AJO
description: O limite de frequência no Adobe Journey Optimizer é aplicado no nível da oferta individual e depende da captura de eventos de impressão e clique na oferta. Isso requer o rastreamento de eventos decisioning.propositionDisplay e decisioning.propositionInteract usando o Adobe Web SDK e mapeando-os para um esquema XDM Experience Event atualizado no Adobe Experience Platform.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00Z
jira: KT-18526
source-git-commit: bef6d831c639d40514552dae3ff20132626a4a09
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Ativar o limite de frequência para uma campanha do AJO

Para aplicar o limite de frequência às ofertas, conclua as seguintes etapas:

## Atualizar o esquema de evento

* Atualize o esquema de evento existente adicionando o grupo de campos como mostrado
* ![esquema-evento](assets/schema.png)

## Atualizar o limite de frequência da oferta


* ![oferta](assets/offer-capping.png)

## Adicionar token de rastreamento à oferta

Edite a política de decisão usada na campanha adicionando uma oferta substituta
![fallback](assets/fallback.png)

O trackingToken e o ItemID podem ser adicionados clicando no ícone da política de decisão na navegação à esquerda e detalhando a árvore de decisão para selecionar o itemID e o trackingToken.

Adicione a ID do item e o token de rastreamento à div que contém a oferta, conforme mostrado abaixo
![id-and-tracking-token](assets/id-and-tracking-token.png)

Isso garante que cada oferta renderizada inclua um token de rastreamento de dados, essencial para garantir uma impressão precisa e um rastreamento de eventos de cliques.


Ative a campanha modificada.


## Enviar eventos de impressão e rastreamento

Modifique o código JavaScript existente para capturar e enviar eventos de impressão e interação da oferta para a Adobe Experience Platform usando o Adobe Web SDK. Consulte o [código de amostra fornecido aqui.](capture-impression-click-events.md)


