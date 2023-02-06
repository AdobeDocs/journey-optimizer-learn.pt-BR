---
title: Configurar eventos
description: Configure três eventos necessários para os desafios práticos do Journey Optimizer
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
recommendations: noDisplay, noCatalog
hide: true
exl-id: c7826818-c28a-493b-8aba-9d8a8102336d
source-git-commit: 7ecbed1b722d7f05ffd4a7c7071358d993cb1392
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 10%

---

# Configurar eventos

Nesta seção, você configura os três eventos necessários para os exercícios práticos no [Desafios da Journey Optimizer](/help/challenges/introduction-and-prerequisites.md).

O vídeo a seguir explica como criar eventos:

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

## Crie o evento de compra online Luma

Ao usar esse evento, o Journey Optimizer recebe informações quando uma pessoa compra produtos luma online.

1. Crie um evento com os seguintes parâmetros:

   | [!UICONTROL Parâmetro] | [!UICONTROL Valor] |
   |-------------|-----------|
   | [!UICONTROL NOME] | `LumaOnlinePurchase` |
   | [!UICONTROL TIPO] | [!UICONTROL Unitário] |
   | [!UICONTROL Tipo de ID do evento] | [!UICONTROL Baseado em regras] |
   | [!UICONTROL Esquema] | `Luma Web Events Schema` |
   | [!UICONTROL Campos] | `eventType` <br>`commerce.order.priceTotal`<br>`commerce.order.purchaseOrderNumber`<br>`commerce.shipping.adress.street1`<br>`commerce.shipping.adress.city`<br>`commerce.shipping.adress.postalCode`<br>`commerce.shipping.adress.state`<br>`productListItems.quantity`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.name`<br>`productListItems.Luma Product Catalog Schema._your Organization_IDprice`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.imageURL`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.url` |

2. Adicione o [!UICONTROL Condição de ID de evento]: `LumaOnlinePurchase.eventType is commerce.purchases`

   1. Selecione o ícone de lápis para editar o campo
   2. No [!UICONTROL Adicionar uma condição de ID de evento] modal, arraste e solte a variável `eventType` sobre a tela
   3. Selecione `commerce.purchases`
   4. Selecione ok na tela
   5. Selecione ok no modal

![Adicionar condição de evento](/help/tutorial-configure-a-training-sandbox/assets/Event-lumaOnlinePurchase-condition-1.png)

1. Selecionar [!UICONTROL NAMESPACE]: `Luma CRM ID (lumaCrmId)`

2. Selecione **[!UICONTROL Salvar]**.

## Criar *[!DNL Luma Wishlist Add]* Evento

| [!UICONTROL Parâmetro] | [!UICONTROL Valor] |
|-------------|-----------|
| [!UICONTROL NOME] | `LumaWishlistAdd` |
| [!UICONTROL TIPO] | [!UICONTROL Unitário] |
| [!UICONTROL Tipo de ID do evento] | [!UICONTROL Baseado em regras] |
| [!UICONTROL Esquema] | `Luma Product Interactions` |
| [!UICONTROL Campos] | EventType<br>productListItem.quantity<br><b>Em Itens da lista de produtos > Produtos Luma > _*[!DNL yourOrganizationID]* > Produto:</b> <br>Nome<br>Preço<br> ProductImageURL<br>ProductURL |
| [!UICONTROL Condição] | [!DNL LumaWishlistAdd.eventType is commerce.saveForLaters] |
| [!UICONTROL Namespace] | Email(Email) |

## Criar *[!DNL Luma Product Restock]* Evento

| [!UICONTROL Parâmetro] | [!UICONTROL Valor] |
|-------------|-----------|
| [!UICONTROL NOME] | `LumaProductRestock` |
| [!UICONTROL TIPO] | [!UICONTROL Business] |
| [!UICONTROL Esquema] | [!DNL Luma Product Inventory Events] |
| [!UICONTROL Campos] | SKU <br> stockEventType<br><b> yourOrganizationID > produto:</b> <br>name<br>preço<br> ImageURL<br>descrição |
| [!UICONTROL Condição] | LumaProductRautomaticamente._`your organization's ID`.inventoryEvent.stockEventType é restock |

## Parabéns

Sua sandbox está pronta para ser usada!
