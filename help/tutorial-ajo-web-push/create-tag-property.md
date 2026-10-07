---
title: Criar propriedade de tag
description: A propriedade da tag envia os dados do navegador para a AEP por meio da Web SDK.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00.000Z
jira: KT-20879
exl-id: 108de002-f033-4b88-bee5-2b50463c345c
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
source-wordcount: '250'
ht-degree: 0%
---
# Criar propriedade de tag

Na segunda parte deste tutorial, você aprenderá a acionar notificações por push em tempo real, enviando manualmente um evento price.drop personalizado. Essa abordagem usa a Coleção de dados (tags) da AEP para capturar o evento da página da Web e enviá-lo para a Adobe Experience Platform. Depois que o evento é assimilado, ele aciona uma jornada no Adobe Journey Optimizer, permitindo enviar notificações por push sob demanda com base nas ações do usuário ou eventos comerciais.

Essa propriedade é configurada com o AEP Web SDK, que está conectado ao `WebPushDataStream` criado anteriormente no tutorial. A propriedade da marca escuta o evento `price.drop` na Camada de Dados do Adobe e mapeia os detalhes relevantes do produto atualizando o elemento de dados ProductListItems. Depois que os dados são preparados, uma regra na propriedade da tag é acionada e envia o evento price.drop para a AEP por meio da Web SDK. Esse evento serve como ponto de entrada para uma jornada no Adobe Journey Optimizer, permitindo a entrega imediata de notificações por push com base na queda de preço.

## Elementos de tag

ProductListItems para conter detalhes do produto

![elementos de marca](assets/product-list-items-element.png)

mapeamento de xdmvariable para o `schemaForPushNotification`

![variável-xdm](assets/xdmvariable-data-element.png)

## Criar regra

Ouça o evento price.drop
![evento-push-de-dados](assets/tag-rule-event.png)

Atualizar productListItems usando a variável de atualização
![variável-atualização](assets/update-variable.png)
Por fim, envie o evento price.drop para o AEP com a variável xd atualizada
![enviar-evento](assets/send-event.png)

O código javascript a seguir envia o evento price.drop para as Tags do AEP da página da Web

```javascript
 <script>
      window.adobeDataLayer.push({
        event: "price.drop",
        productListItems: productListItems
      });
  </script>
```
