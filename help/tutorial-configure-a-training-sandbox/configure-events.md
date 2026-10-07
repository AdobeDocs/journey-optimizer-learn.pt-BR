---
title: Configurar eventos
description: Configure os três eventos necessários para os desafios práticos do Journey Optimizer
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
jira: KT-9382
role: Admin
level: Beginner
recommendations: noDisplay, noCatalog
exl-id: c7826818-c28a-493b-8aba-9d8a8102336d
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
    internal-label: Data management activity
  - id: d556b755-390a-43f0-be32-a08cf6236126
    internal-label: Configuration
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
    internal-label: Sandboxes
  - id: efb19423-4da4-4fd1-88d8-5ee8c71ae766
    internal-label: Application settings
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 100%
---
# Configurar eventos

Nesta seção, você configurará os três eventos necessários para os exercícios práticos dos [Desafios do Journey Optimizer](/help/challenges/introduction-and-prerequisites.md).

O vídeo a seguir explica como criar eventos:

>[!VIDEO](https://video.tv.adobe.com/v/3431510?captions=por_br&quality=12&learn=on){transcript=true}

## Criar o evento de compra online da Luma

Ao usar esse evento, o Journey Optimizer recebe informações quando uma pessoa compra produtos da Luma na loja online.

1. Crie um evento com os seguintes parâmetros:

   | [!UICONTROL Parâmetro] | [!UICONTROL Valor] |
   |-------------|-----------|
   | [!UICONTROL NOME] | `LumaOnlinePurchase` |
   | [!UICONTROL TIPO] | [!UICONTROL Unitário] |
   | [!UICONTROL Tipo de ID de evento] | [!UICONTROL Baseado em regras] |
   | [!UICONTROL Esquema] | `Luma Web Events Schema` |
   | [!UICONTROL Campos] | `eventType` <br>`commerce.order.priceTotal`<br>`commerce.order.purchaseOrderNumber`<br>`commerce.shipping.adress.street1`<br>`commerce.shipping.adress.city`<br>`commerce.shipping.adress.postalCode`<br>`commerce.shipping.adress.state`<br>`productListItems.quantity`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.name`<br>`productListItems.Luma Product Catalog Schema._your Organization_IDprice`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.imageURL`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.url` |

1. Adicione a [!UICONTROL Condição de ID de evento]: `LumaOnlinePurchase.eventType is commerce.purchases`:

   1. Clique no ícone de lápis para editar o campo.

   1. No modal **[!UICONTROL Adicionar uma condição de ID de evento]**, arraste e solte o `eventType` sobre a tela.
   1. Selecione `commerce.purchases`.
   1. Clique em **[!UICONTROL OK]** na tela.
   1. Clique em **[!UICONTROL OK]** no modal.

   ![Adicionar condição de evento](/help/tutorial-configure-a-training-sandbox/assets/Event-lumaOnlinePurchase-condition-1.png)

1. Selecione o [!UICONTROL NAMESPACE]: `Luma CRM ID (lumaCrmId)`

1. Selecione **[!UICONTROL Salvar]**.

## Crie o evento *[!DNL Luma Product Restock]*

| [!UICONTROL Parâmetro] | [!UICONTROL Valor] |
|-------------|-----------|
| [!UICONTROL NOME] | `LumaProductRestock` |
| [!UICONTROL TIPO] | [!UICONTROL Business] |
| [!UICONTROL Esquema] | [!DNL Luma Product Inventory Event Schema] |
| [!UICONTROL Campos] | SKU <br> stockEventType<br><b>LumaProductCatalogSchema._yourOrganizationID.product :</b> <br>nome<br>preço<br> ImageURL<br>descrição |
| [!UICONTROL Condição] | LumaProductRestock._`your organization's ID`.inventoryEvent.stockEventType foi reabastecido |

Parabéns! Sua sandbox agora está pronta para uso.
