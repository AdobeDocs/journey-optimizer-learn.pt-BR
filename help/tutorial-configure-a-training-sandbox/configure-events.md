---
title: Configurar eventos
description: Configure três eventos necessários para enfrentar os desafios do Journey Optimizer
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
recommendations: noDisplay, noCatalog
exl-id: c7826818-c28a-493b-8aba-9d8a8102336d
source-git-commit: 08dfd48d34fac09d05e57438728e1afa5f6cdef9
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 8%

---

# Configurar eventos

Nesta seção, você configura os três eventos necessários para os exercícios práticos no [Desafios da Journey Optimizer](/help/challenges/introduction-and-prerequisites.md).

Assista ao vídeo [Criar eventos](/help/set-up-journeys/create-events.md) para obter orientação sobre como criar eventos.

## Crie o evento de compra online Luma

1. Na navegação à esquerda, navegue até [!UICONTROL ADMINISTRAÇÃO] e selecione *[!UICONTROL Configuração]*
1. No [!UICONTROL Painel], selecione *[!UICONTROL Gerenciar*]* Eventos

![Gerenciar eventos](assets/create-events.png)

1. Clique em *[!UICONTROL Criar evento]*
1. Preencha os detalhes e parâmetros do evento:

   | [!UICONTROL Parâmetro] | [!UICONTROL Valor] |
   |-------------|-----------|
   | [!UICONTROL NOME] | `LumaOnlinePurchase` |
   | [!UICONTROL TIPO] | [!UICONTROL Unitário] |
   | [!UICONTROL Tipo de ID do evento] | [!UICONTROL Baseado em regras] |
   | [!UICONTROL Esquema] | Interações do produto Luma |
   | [!UICONTROL Campos] | EventType <br>Order.priceTotal<br>purchaseOrderNumber<br>productListItems.quantity<br><b>Em Itens da Lista de Produtos > Esquema do Catálogo de Produtos Luma > _*[!DNL yourOrganizationID]* > Produto:</b> <br> Nome<br>Preço<br>ProductImageURL<br>ProductURL |

1. Adicione o [!UICONTROL Condição de ID de evento]: **[!DNL LumaOnlinePurchase.eventType is commerce.purchases]**

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

## Criar *[!DNL Luma Product Restock] Evento

| [!UICONTROL Parâmetro] | [!UICONTROL Valor] |
|-------------|-----------|
| [!UICONTROL NOME] | `LumaProductRestock` |
| [!UICONTROL TIPO] | [!UICONTROL Business] |
| [!UICONTROL Esquema] | [!DNL Luma Product Inventory Events] |
| [!UICONTROL Campos] | productID <br> stockEventType<br><b>Em Produto > Produtos Luma > *[!DNL yourOrganizationID]* > Produto:</b> <br>Nome<br>Preço<br> ProductImageURL<br>Descrição |
| [!UICONTROL Condição] | LumaProductRautomaticamente._`your organization's ID`.inventoryEvent.stockEventType é restock |

## Parabéns

Sua sandbox está pronta para ser usada!
