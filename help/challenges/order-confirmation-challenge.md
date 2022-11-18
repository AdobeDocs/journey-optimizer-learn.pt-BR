---
title: Criar uma confirmação de pedido
description: Testar seu conhecimento sobre como criar e personalizar mensagens transacionais
kt: 7531
feature: Journeys
role: User
level: Beginner
hide: true
source-git-commit: dd2832c1e99ed9b8407a0aa9356335d3bce40622
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 4%

---


# Criar um email transacional de confirmação de pedido

![Confirmação de pedido](/help/challenges/assets/email-assets/luma-transactional-order-confirmation.png)

| Desafio | Criar um email transacional de confirmação de pedido |
|---|---|
| Perfil | Gerenciador de jornadas |
| Competências necessárias | <ul><li>[Criar conteúdo de email com o editor de mensagens](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-email-content-with-the-message-editor.html?lang=en)</li> <li>[Usar informações de evento contextual para personalização](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-contextual-event-information-for-personalization.html?lang=en)</li><li>[Usar funções auxiliares para personalização](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-helper-functions-for-personalization.html?lang=en)</li></ul> |
| Ativos para baixar | [Ativos de confirmação de pedido](/help/challenges/assets/email-assets/order-confirmation-assets.zip) |

## A História

A Luma está lançando sua loja online e deseja garantir uma boa experiência do cliente, fornecendo um email de confirmação de pedido depois que o cliente fizer um pedido.

Crie e personalize uma mensagem de confirmação de pedido transacional.

## Você tem tudo de que precisa?

## Seu desafio

Crie um email de confirmação de pedido acionado quando um cliente Luma conclui um pedido online.

### Criar o email de confirmação do pedido

Crie uma nova mensagem de email chamada &quot;(seu nome)_Luma - Confirmação do pedido&quot;. A linha de assunto deve ser personalizada com o nome dos recipients e deve incluir a frase &quot;obrigado pela sua compra&quot;

De acordo com a diretriz da marca Luma, o email deve ser estruturado da seguinte maneira:

<table>
<tr>
<td>
  <div>
     <strong> Seção do cabeçalho</strong>
      </div>
  </td>
  <td>
    <strong>Logotipo Luma</strong>
      <p>
     <li>luma_logo.png</li>
    <li>Tamanho 35%, fundo branco centralizado </li>
    <li>Ele deve ter um link para o site do luma: https://publish1034.adobedemo.com/content/luma/us/en.html</li>
    <p>
    Dica: Você encontrará todas as imagens na pasta de ativos chamadas mensagens de imagens. <p>
    </td>
  </tr>
  <tr>
  <td>
  <div>
    <strong>Seção de Confirmação de Pedido
    </strong>
  </td>
  <td>
    <strong>Imagem</strong><p>
    <li>luma-transactional-order-confirmation-2.jpg </li>
    <li>Margem: Superior, inferior (10)<div>
    <p>
    <strong>Texto</strong><p>
    <em>Obrigado pela compra!</em><p>
    <li>Alinhamento: left  </li>
   <li>Cor do texto: rgb(101, 106, 119); tamanho da fonte:14px</li>
    <li>Preenchimento: esquerda (95), direita (95)</li><div>
    <p>
     <em>Seu pedido foi feito.
    <p>Quando o pacote for enviado, enviaremos um email com um número de rastreamento para que você possa rastrear seu pedido.</p></em>
    </strong><p>
    <li>Alinhamento: left  </li>
    <li>Cor do texto: rgb(101, 106, 119); tamanho da fonte:14px </li>
    <li>Preenchimento: esquerda (95), direita (95)</li><div>
    </a>
    <p>
    <strong>Botão:</strong>
   <p><em>Veja seu pedido</em></p>
      <li>Cor do plano de fundo: rgb(25, 121, 195)</li>
      <li>Cor do texto: Branco</li>
      <li>Sem borda</li>
      <li>Altura: 40º</li>
      <li>Adicionar um link a um site de sua escolha </li>
      <li>Alinha à esquerda com o texto acima (dica: usar a margem do contêiner)</li>
  </td>
 <tr>
<td>
  <div>
     <strong>Seção Detalhes do Pedido</strong>
      </div>
      <p>Dicas:
      <li>Essas são informações de evento contextual. Você só poderá adicionar a mensagem no contexto depois de adicioná-la à jornada (consulte a etapa 2). Não publique seu email antes de adicioná-lo à Jornada e modificá-lo com as informações do evento contextual!</li>
      <li>Use a função auxiliar: Cada</li>
      <li>Use o editor de HTML para formatar os dados contextuais.Coloque as informações em contêineres usando tags DIV.</li>
  </td>
  <td>
    <strong>Header</strong>
    <p>
    <em>Pedido {Número do Pedido de Compra}</em>
    </p>
    <strong>Lista de produtos encomendados:
  </strong>
  <p>Cada um dos itens deve ser formatado desta forma:
   <img alt="pedido" src="./assets/c2-order.png"> 
</p>
<strong>Imagem do produto:</strong>
<li>classe: cadeira de itens do carrinho
<li>estilo: caixa de borda: altura mínima:40px</li>
<li>preenchimento superior e inferior:20px</li>
<li>preenchimento à esquerda:80px</li>
<li>border-radius:0px</li>
<li>Usar como imagem de plano de fundo para o contêiner</li>
<li>posição de fundo: 0% 50%</li>
<li>tamanho do plano de fundo: 60px</li>
<li>repetição em segundo plano: sem repetição</li>
<p>
<strong>Preço:</strong>
<li>Formato = H5</li>
<li>estilo = dimensionamento de caixa:caixa de borda</li>
<li>margem inferior:5 px</li>
<li>margem superior:0px;</li>
<p>
<strong>Nome e quantidade:</strong>
<li>class=text-small</li>
<li>style=box-sizing: border-box</li>
<li>tampa do preenchimento: 5px</li>
<li>cor: rgb(101, 106, 119)</li>
<li>tamanho da fonte:14px</li>
<p>
</td>
  </tr>
</table>

### Crie a jornada

1. Chame a jornada &quot;seu nome _Luma-Order Confirmation&quot;
1. Use o evento : LumaOnlinePurchase
1. Ação: Adicione a mensagem que você criou na etapa 1
1. Volte para a mensagem e adicione os atributos contextuais
1. Publicar o email

>[!TIP]
>
>Para permitir que você solucione problemas em suas jornadas, a prática recomendada é adicionar um caminho alternativo a todas as ações de mensagem em caso de tempo limite ou erro.

+++Critérios de sucesso

Acione a Jornada criada no modo de teste e envie o email para você mesmo:

1. Mostre os valores ocultos clicando no símbolo dos olhos:
   1. Nos Parâmetros de email, clique no símbolo T (ativar substituição de parâmetro)
      ![Substituir parâmetros de email](/help/challenges/assets/c3-override-email-paramters.jpg)
   2. Clique no campo Endereço
   3. Na próxima tela, adicione o endereço de email entre parênteses: *yourname@yourdomain* no editor de expressão e clique em ok.
2. Coloque a jornada no modo de teste
3. Acione o evento com os seguintes parâmetros:
   * Defina o identificador do perfil para: Jenna_Palmer9530@emailsim.io
   * Tipo de evento: commerce.purches
   * Nome: Sprite Yoga Companion Kit
   * Quantidade: 1
   * Preço total: 61º
   * Número do pedido: 6253728
   * SKU: 24-WG080
   * productImageURL: <https://publish1034.adobedemo.com/content/dam/luma/en/products/gear/fitness-equipment/luma-yoga-kit-2.jpg>

Você deve receber o email de confirmação de compra personalizado, com o produto especificado.

* A linha de assunto deve começar com o nome do seu perfil de teste: Jenna
* A seção de detalhes do pedido deve ser preenchida com os detalhes do pedido inseridos durante o teste
* As informações do cliente devem ter a cidade e o código postal do perfil de teste:

   43913 Thierer Terrace, Washington DC 2009

+++

+++Verifique seu trabalho

**Linha de assunto:**

{{ profile.person.name.firstName }}, obrigado pela sua compra!

**Seção Cabeçalho e confirmação:**

![Confirmação de cabeçalho e pedido](/help/challenges/assets/c2-header.png)

**Seção de detalhes da ordem:**

![Seção de detalhes do pedido](/help/challenges/assets/c2-order-detail-section.png)

Esta é a aparência do código:

Header:

```javascript
Order: {{context.journey.events.1627840522.commerce.order.purchaseOrderNumber}}
```

Lista de produtos:

Use a função auxiliar &quot;each&quot; para criar a lista de produtos. Esta é a aparência do código:

```javascript
{{#each context.journey.events.1911672547.productListItems as|product|}}
<div class="cart-item-chair" style="box-sizing:border-box;min-height:40px;padding-top:20px;padding-bottom:20px;padding-left:80px;border-radius:0px;background-image:url({{product._wwfovlab065.productImageURL}});background-position:0% 50%;background-size:60px;background-repeat:no-repeat;">
<h5 style="box-sizing:border-box;margin-bottom:5px;font-size:16px;line-height:20px;margin-top:0px;">${{product.priceTotal}}.00</h5>
<div class="text-small" style="box-sizing:border-box;padding-top:5px;color:rgb(101, 106, 119);font-size:14px;">{{product.name}}</div><div class="text-small" style="box-sizing:border-box;padding-top:5px;color:rgb(101, 106, 119);font-size:14px;">Quantity: {{product.quantity}}</div></div><div class="divider-small" style="box-sizing:border-box;height:1px;margin-top:10px;margin-bottom:10px;background-color:rgb(209, 213, 223);"> </div>
{{/each}}

Total: ${{context.journey.events.1627840522.commerce.order.priceTotal}} 
```

**Seção de informações do cliente**

![Endereço do cliente](assets/c2-customer-information.png)

A personalização deve ter esta aparência:

```javascript
{{profile.homeAddress.street1}}
{{profile.homeAddress.city}},{{profile.homeAddress.state}} {{profile.homeAddress.postalCode}}
```

**Rodapé:**
![rodapé](/help/challenges/assets/c2-footer.png)

**Jornada**

![Jornada](/help/challenges/assets/c2-journey.png)

+++

