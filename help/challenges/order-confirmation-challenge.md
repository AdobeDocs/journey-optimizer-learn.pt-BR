---
title: Criar email de confirmação de pedido
description: Teste o seu conhecimento sobre como criar e personalizar mensagens transacionais
kt: 7531
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: ec86e2ac-081d-47aa-a948-007107baa2b4
source-git-commit: e377ddb8b84dccd503274caf9ffa3d4c73eedc28
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 50%

---


# Criar email de confirmação de pedido

![Confirmação de pedido](/help/challenges/assets/email-assets/luma-transactional-order-confirmation.png)

| Desafio | Criar um email transacional de confirmação de pedido |
|---|---|
| Perfil | Gerenciador de Jornadas |
| Competências necessárias | <ul><li>[Criar conteúdo de email com o editor de mensagens](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/create-content-with-the-email-designer.html?lang=en)</li> <li>[Usar informações de evento contextual para personalização](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-contextual-event-information-for-personalization.html?lang=pt-BR)</li><li>[Usar funções auxiliares para personalização](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-helper-functions-for-personalization.html?lang=pt-br)</li></ul> |
| Ativos para baixar | [Ativos de confirmação de pedido](/help/challenges/assets/email-assets/order-confirmation-assets.zip) |

## A História

A Luma está lançando sua loja online e deseja garantir uma boa experiência do cliente ao enviar um email de confirmação de pedido assim que um pedido for feito.



## Seu desafio

Crie uma jornada que envia um email de confirmação de pedido quando um cliente da Luma conclui um pedido online.

>[!BEGINTABS]

>[!TAB Tarefa]

1. Crie uma jornada chamada `Luma - Order Confirmation`
2. Use o evento : `LumaOnlinePurchase`
3. Crie um **transacional**  email chamado `Luma - Order Confirmation`
* A linha de assunto &quot;Obrigado pela sua compra, `FirstName`&quot;
* Use o modelo `Luma - Order summary` e modifique-o:
   * Remova o `You may also like` seções
   * Adicione o link de cancelamento de subscrição na parte inferior do email

O objeto deve ser estruturado da seguinte maneira:
<table>
<tr>
<td>
  <div>
     <strong> Seção cabeçalho</strong>
      </div>
  </td>
  <td>
      <p>
     <li>luma_logo.png</li>
    <li>O link para o site do luma deve ser enviado: https://luma.enablementadobe.com/content/luma/us/en.html</li>
    <p>
    </td>
  </tr>
  <tr>
  <td>
  <div>
    <strong>Seção Confirmação de pedido
 </strong>
  </td>
  <td>
    <p>
    <strong>Texto</strong><p>
    <em>Ei {firstName},</em><p>
   <div>
    <p>
     <em>Seu pedido foi feito.
    <p>Quando o pacote for enviado, enviaremos um email com um número de rastreamento para que você possa rastrear seu pedido.</p></em>
    </strong>
    </tr>
  </td>
 <td>
  <div>
     <strong> Seção Enviar para</strong>
      </div>
      <p>
      <li>O nome e o sobrenome são do perfil
      <li>Substitua o endereço codificado no modelo pelo <b>endereço de entrega</b>
      <li>Os detalhes do endereço são atributos contextuais do evento (rua 1, cidade, código postal, estado)
      <li> Remover <i>Desconto, Total, Chegando</i></p>
  </td>
  <td>
  <p> Enviar para:</p>
      <em>{firstName} {lastName}<br>
     {Rua 1}<br>
     {City}, {State} {postalCode}<br></em></p>
  </td>
 <tr>
<td>
  <div>
     <strong>Seção Detalhes do pedido</strong>
      </div>
       <p><li>Adicione esta seção abaixo do <b>Entregar para</b> seção.
      </p><br>
      <p><b>Dicas:</b>
      <li>Usar o componente de estrutura <b>Coluna 1:2 esquerda</b> para esta seção
      <li>Essas são informações de evento contextual.
      <li>Use a [!UICONTROL helper function]: [!UICONTROL Each]
      <li>Alterne para o formato do editor de códigos para adicionar os dados contextuais.
  </td>
  <td>
    <strong>Cabeçalho</strong>
    <p>
  Pedido: <em>{purchaseOrderNumber}</em>
    </p>
    <strong>Lista de produtos encomendados:
 </strong>
  <p>Liste cada produto na ordem com uma imagem, o preço e o nome.
  <p>O layout de cada item deve ser semelhante a:
   <img alt="pedido" src="./assets/c2-order.png"> 
<p><b>Adicionar o link ao carrinho</b>
<p>Substitua a ID do pedido no URL pelo número do pedido de compra:
   <i>https://luma.enablementadobe.com/content/luma/us/en/user/account/order-history/order-details.html?orderId=90845952-c2ea-4872-8466-5289183e4607</i>
</td>
  </tr>
</table>


>[!TIP]
>
>Para permitir que você solucione problemas em suas jornadas, a prática recomendada é adicionar um caminho alternativo a todas as ações de mensagem, se houver um tempo limite ou erro.

>[!TAB Critérios de sucesso]

Acione a Jornada criada no modo de teste e envie o email para você mesmo:

1. Antes de alternar para o modo de teste, substitua os parâmetros de email para enviar ao email de teste para seu endereço de email:
   1. Abra a visualização de detalhes do email.
   2. Na seção Parâmetros de email , clique no símbolo T (ativar substituição de parâmetro)
   3. Clique no campo Endereço
   4. Na próxima tela, adicione o endereço de email entre parênteses: *&quot;yourname@yourdomain&quot;* no editor de expressão e clique em ok.
2. Coloque a jornada no modo de teste
3. Acione o evento com os seguintes parâmetros:
   * Defina o identificador do perfil para: Valor de identidade:`a8f14eab3b483c2b96171b575ecd90b1`
   * Tipo de evento: Compras de comércio
   * `Quantity`: 1
   * `Price Total:` 69
   * `Purchase Order Number:` 90845952-c2ea-4872-8466-5289183e4607
   * `SKU:` LLMH09
   * `City:`San Jose
   * `Postal Code:` 95119
   * `State`: CA
   * `Street:` 245 Park Avenue

Você deve receber o email de confirmação de compra personalizado.

* A linha de assunto deve ter o nome do perfil de teste: Leora

* Este é o aspecto do corpo do email:

![Email](/help/challenges/assets/c2-email.png)

>[!TAB Verifique o seu trabalho]

**Jornada**

![Jornada](/help/challenges/assets/c2-journey.png)


**Email**

**Linha de assunto:**

Obrigado pela sua compra, {{ profile.person.name.firstName }}!

**Seção Enviar para:**

É assim que o código deveria parecer:

```javascript
{{ profile.person.name.firstName }} {{ profile.person.name.lastName }}
{{context.journey.events.454181416.commerce.shipping.address.street1}}
{{context.journey.events.454181416.commerce.shipping.address.city}}, {{context.journey.events.454181416.commerce.shipping.address.state}} {{context.journey.events.454181416.commerce.shipping.address.postalCode}}
```

*event.45481416* é um número diferente para você.

DICA: Personalize cada linha separadamente

**Seção Detalhes do pedido:**

É assim que o código deveria parecer:

Cabeçalho:

```javascript
Order #: {{context.journey.events.1627840522.commerce.order.purchaseOrderNumber}}
```

**Lista de produtos:**

Use a função auxiliar “cada” para criar a lista de produtos. Mostre-lhes em uma tabela. É com isso que o código deve ficar (com variáveis específicas, como a ID do evento - em vez de `454181416` e sua organização I em vez de `techmarketingdemos` ):

```javascript
{{#each context.journey.events.454181416.productListItems as |product|}}<tr> <th class="colspan33"><div class="acr-fragment acr-component image-container" data-component-id="image" style="width:100%;text-align:center;" contenteditable="false"><!--[if mso]><table cellpadding="0" cellspacing="0" border="0" width="100%"><tr><td style="text-align: center;" ><![endif]--><img src="{{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.imageUrl}}" style="height:auto;width:100%;" height="233" width="233"><!--[if mso]></td></tr></table><![endif]--></div></th> <th class="colspan66"><div class="acr-fragment acr-component" data-component-id="text" contenteditable="false"><div class="text-container" contenteditable="true"><p><span style="font-weight:700;">{{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.name}}</span></p></div></div><div class="acr-fragment acr-component" data-component-id="text" contenteditable="false"><div class="text-container" contenteditable="true"><p>${{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.price}}.00</p></div></div></th></tr> {{/each}}
```

**Botão Exibir pedido:**

`https://luma.enablementadobe.com/content/luma/us/en/user/account/order-history/order-details.html?orderId={{context.journey.events.454181416.commerce.order.purchaseOrderNumber}}`

**Preço total:**

Total:`${{context.journey.events.1627840522.commerce.order.priceTotal}}.00`


>[!ENDTABS]