---
title: Configurar eventos
description: Configure os três eventos necessários para os desafios práticos do Journey Optimizer
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
recommendations: noDisplay, noCatalog
exl-id: c7826818-c28a-493b-8aba-9d8a8102336d
source-git-commit: b2afc28f82967324ebed0ee17e291e83c85c3a4c
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# Configurar eventos

Nesta seção, você configurará os três eventos necessários para os exercícios práticos dos [Desafios do Journey Optimizer](/help/challenges/introduction-and-prerequisites.md).

O vídeo a seguir explica como criar eventos:

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12&learn=on)

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

## Crie o evento *[!DNL Luma Wishlist Add]*

| [!UICONTROL Parâmetro] | [!UICONTROL Valor] |
|-------------|-----------|
| [!UICONTROL NOME] | `LumaWishlistAdd` |
| [!UICONTROL TIPO] | [!UICONTROL Unitário] |
| [!UICONTROL Tipo de ID de evento] | [!UICONTROL Baseado em regras] |
| [!UICONTROL Esquema] | `Luma Product Interactions` |
| [!UICONTROL Campos] | EventType<br>productListItem.quantity<br><b>Em Itens da lista de produtos > Produtos Luma > _*[!DNL yourOrganizationID]* > Produto:</b> <br>Nome<br>Preço<br> ProductImageURL<br>ProductURL |
| [!UICONTROL Condição] | [!DNL LumaWishlistAdd.eventType is commerce.saveForLaters] |
| [!UICONTROL Namespace] | Email(EMail) |

## Crie o evento *[!DNL Luma Product Restock]*

| [!UICONTROL Parâmetro] | [!UICONTROL Valor] |
|-------------|-----------|
| [!UICONTROL NOME] | `LumaProductRestock` |
| [!UICONTROL TIPO] | [!UICONTROL Business] |
| [!UICONTROL Esquema] | [!DNL Luma Product Inventory Events] |
| [!UICONTROL Campos] | SKU <br> stockEventType<br><b> yourOrganizationID > produto:</b> <br>nome<br>preço<br> ImageURL<br>descrição |
| [!UICONTROL Condição] | LumaProductRestock._`your organization's ID`.inventoryEvent.stockEventType foi reabastecido |

Parabéns! Sua sandbox agora está pronta para uso.
