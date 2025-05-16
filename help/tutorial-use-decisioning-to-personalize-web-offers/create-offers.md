---
title: Criar uma oferta
description: Um item de oferta na decisão representa uma única parte do conteúdo personalizado, como uma mensagem, imagem, promoção ou recomendação, que pode ser entregue a um usuário com base em regras e condições definidas.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00Z
jira: KT-17728
exl-id: d705992a-0d47-4bb9-b3d8-b925974e64cb
source-git-commit: 502cdc41b666959141ff4dfc63608cc463009811
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---

# Criar uma oferta

Um item de oferta no AJO representa um único conteúdo personalizado. O conteúdo pode ser uma promoção, mensagem ou recomendação que é entregue a um usuário, com base na lógica de decisão.

Ao criar um item de oferta no AJO, ele deve ser baseado em um [!UICONTROL Esquema de decisão]. Esse esquema define a estrutura e os campos disponíveis na oferta, como title, description, imageURL, offerText e assim por diante.

Este esquema:

* Padroniza o modelo de conteúdo para todas as ofertas em uma coleção.

* Permite campos de personalização consistentes entre itens de oferta.

* Permite que as estratégias de seleção correspondam as regras ao conteúdo estruturado

## Modificar o esquema

1. Faça logon no Journey Optimizer.
1. Clique em **[!UICONTROL Decisão]** > **[!UICONTROL Catálogos]** > **[!UICONTROL Editar esquema]**.
1. Adicione um elemento do tipo `string` chamado `offerItem` como mostrado abaixo

   ![esquema de decisão](assets/offer-schema.png)

## Criar um item de oferta

1. Clique em **[!UICONTROL Decisão]** > **[!UICONTROL Catálogos]** > **[!UICONTROL Criar item]**.

1. Crie três ofertas: `Love Stocks`, `Love Bonds` e `Love CD`.

   Para cada oferta, copie e cole o texto de oferta correspondente fornecido no final deste artigo no item de oferta apropriado.

1. Adicione uma tag às ofertas com a tag criada na etapa anterior.
1. Adicione o público-alvo apropriado a cada oferta.
   ![qualificação para a oferta](assets/offer-eligibility.png)
1. Aprove as ofertas.

Oferta concluída com atributos padrão e personalizados definidos:

![oferta de ação de amor](assets/love-bonds.png)

**Texto da oferta Love Stocks**

```html
<div style="font-family: Arial, sans-serif; background-color: #f9f9f9; border: 1px solid #ddd; padding: 1.5rem; border-radius: 8px; max-width: 600px; margin: auto;">   <h3 style="color: #1a73e8; margin-top: 0;">📈 Open a Stock Trading Account & Get $100 in Bonus Stock</h3>   <p style="font-size: 1rem; color: #333;">     Ready to start building your portfolio? Open a new stock trading account with us and receive a      <strong>$100 bonus in stock</strong> — on us.   </p>   <ul style="padding-left: 1.25rem; color: #444;">     <li>🧾 No account minimums — start investing with as little as $1</li>     <li>📉 $0 commissions on online stock trades</li>     <li>📊 Access to powerful trading tools and real-time analytics</li>     <li>🎓 Free educational resources to help you invest confidently</li>   </ul>   <p style="color: #333;">     It's never been easier to start trading. Join thousands of investors who trust us to help them grow their wealth.   </p>   <a href="https://yourbrokerage.com/open-account"      style="display: inline-block; margin-top: 1rem; padding: 0.75rem 1.5rem; background-color: #1a73e8; color: white; text-decoration: none; border-radius: 5px; font-weight: bold;">      🚀 Open Your Account Today   </a> </div>
```

**OfferText de obrigações de amor**

```html
<div style="font-family: Arial, sans-serif; background-color: #f9f9f9; border: 1px solid #ddd; padding: 1.5rem; border-radius: 8px; max-width: 600px; margin: auto;">   <h3 style="color: #6c757d; margin-top: 0;">🏦 Invest in Stability: Explore Our Premium Bond Options</h3>   <p style="font-size: 1rem; color: #333;">     Looking for consistent income with lower risk? Our carefully selected bonds offer predictable returns and help balance your investment portfolio.   </p>   <ul style="padding-left: 1.25rem; color: #444;">     <li>📉 Lower volatility than stocks — ideal for income-focused investors</li>     <li>💵 Earn interest payments monthly, quarterly, or annually</li>     <li>🔍 Choose from government, municipal, or corporate bonds</li>     <li>🎁 Open a bond investment account today and receive a <strong>$50 interest credit</strong></li>   </ul>   <p style="color: #333;">     Whether you're preparing for retirement or just want a reliable stream of income, bonds offer a solid foundation for your financial strategy.   </p>   <a href="https://yourfirm.com/open-bond-account"      style="display: inline-block; margin-top: 1rem; padding: 0.75rem 1.5rem; background-color: #6c757d; color: white; text-decoration: none; border-radius: 5px; font-weight: bold;">      🧾 Open a Bond Account   </a> </div>
```

**Oferta de CD do LoveText**

```html
<div style="font-family: Arial, sans-serif; background-color: #f9f9f9; border: 1px solid #ddd; padding: 1.5rem; border-radius: 8px; max-width: 600px; margin: auto;">   <h3 style="color: #28a745; margin-top: 0;">💰 Lock in a 5.25% APY — Open Your CD Account Today</h3>   <p style="font-size: 1rem; color: #333;">     Secure your savings with a high-yield Certificate of Deposit. For a limited time, enjoy a      <strong>guaranteed 5.25% annual percentage yield (APY)</strong> on 12-month CDs.   </p>   <ul style="padding-left: 1.25rem; color: #444;">     <li>🔒 Guaranteed returns with FDIC insurance</li>     <li>📈 Lock in today's high rates before they change</li>     <li>💼 Flexible terms from 6 to 24 months</li>     <li>🎁 Open with just $500 and get a $50 bonus</li>   </ul>   <p style="color: #333;">     Whether you're saving for a short-term goal or building a conservative income strategy, our CDs offer peace of mind and predictable growth.   </p>   <a href="https://yourbank.com/open-cd"      style="display: inline-block; margin-top: 1rem; padding: 0.75rem 1.5rem; background-color: #28a745; color: white; text-decoration: none; border-radius: 5px; font-weight: bold;">      💼 Open a CD Account   </a> </div>
```
