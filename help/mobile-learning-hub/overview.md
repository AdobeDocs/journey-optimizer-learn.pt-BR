---
title: Hub de aprendizagem móvel
description: The mobile learning hub equips developers, administrators, marketers, and analysts with everything needed to configure inbound and outbound mobile channels and integrate them seamlessly into powerful cross-channel campaigns and journeys in Journey Optimizer.
feature: Overview
role: User, Admin, Developer
hide: false
index: true
jira: KT-19860
last-substantial-update: 2025-12-18T00:00:00Z
exl-id: f0612a1d-f919-4b67-9e33-a9fb623062dc
source-git-commit: 3917e11cdf8c0450c19ce653a0964f6dc9da6a3c
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 5%

---

# Journey Optimizer - Mobile Learning Hub

Acelere ou aprimore sua estratégia de engajamento móvel com o Adobe Journey Optimizer. Este centro de aprendizagem para dispositivos móveis fornece a desenvolvedores, admins, profissionais de marketing e analistas tudo o que é necessário para configurar canais móveis de entrada e saída e integrá-los perfeitamente a campanhas e jornadas avançadas entre canais.

Explore best practices, learn how to drive adoption, and setup centralized reporting workflows — all in one place — to deliver impactful, data-driven mobile experiences that reach customers anytime, anywhere.

>[!VIDEO](https://video.tv.adobe.com/v/3477003?captions=por_br&quality=12&learn=on){transcript=true}


## Mobile channel overview

Journey Optimizer supports both inbound and outbound mobile channels:

### Canais de saída

Outbound channels let you proactively deliver messages to customers without requiring a prior interaction. These interactions are ideal for campaigns, promotions, or transactional events.

All outbound channels in Adobe Journey Optimizer enforce Custom Consent Policies at message send time. If consent is not granted for a specific marketing action, the message is automatically suppressed to ensure compliant delivery.

| ![Push Notifications](/help/mobile-learning-hub/assets/mobile-phone.webp){width=&quot;250&quot;, height=&quot;250&quot;}<br> **[Push Notifications](/help/mobile-learning-hub/channels/push-notifications-overview.md)** | ![SMS/MMS/RCS](/help/mobile-learning-hub/assets/SMS.png){width=&quot;250&quot;, height=&quot;250&quot;}<br> **[SMS / MMS / RCS](/help/mobile-learning-hub/channels/sms-mms-rcs-overview.md)** | ![WhatsApp](/help/mobile-learning-hub/assets/whatsapp.webp){width=&quot;250&quot;, height=&quot;250&quot;}<br> **[WhatsApp](/help/mobile-learning-hub/channels/whatsapp-overview.md)** |
|-------------------------------------|------------------------------------|-------------------------------|
| Sent outside the app, push messages grab attention immediately. They&#39;re ideal for time-sensitive updates and encouraging users to return to your app. | Direct messages sent to users&#39; mobile phones without needing the app. Great for urgent alerts, reminders, and rich media content like images or videos. | Conversational channel through a widely used messaging app, allowing personalized, two-way communication and interactive campaigns. |

### Canais de entrada

Inbound channels support customer-initiated interactions, allowing you to deliver personalized experiences the moment users engage with your brand. They enable real-time personalization and data capture—such as landing page forms or on-site behaviors—that feed directly into Adobe Experience Platform (AEP) for segmentation, targeting, and activation across journeys.


| ![In-App Messages](/help/mobile-learning-hub/assets/frescopa-in-app.png){width=&quot;250&quot;,height=&quot;50%&quot;}<br> **[In-App Messages](/help/mobile-learning-hub/channels/in-app-messages-overview.md)** | ![Content Cards](/help/mobile-learning-hub/assets/content-card.jpeg){width=&quot;250&quot;, height=&quot;250&quot;}<br> **[Content Cards](/help/mobile-learning-hub/channels/content-cards-overview.md)** | ![Code-Based Experience](/help/mobile-learning-hub/assets/code-based.png){width=&quot;250&quot;, height=&quot;250&quot;}<br> **[Code-Based Experience](/help/mobile-learning-hub/channels/code-based-experience-overview.md)** |
|-------------------------------------|------------------------------------|-------------------------------|
| Delivered while users are actively using your app, these messages are real-time and interactive. They&#39;re perfect for engaging customers in the moment. | Non-intrusive, persistent messages users can access anytime within the app. Content cards work well for sharing ongoing offers or helpful information. | Custom-coded messages enable highly personalized and dynamic campaigns, integrating real-time data and complex customer journeys. |


### How can mobile channels work together?

By combining these channels, you can create a seamless and effective customer experience:

1. Use [push notifications](/help/mobile-learning-hub/channels/push-notifications-overview.md) to quickly grab attention and bring users back to your app (e.g., &quot;Sale starts now!&quot;).

2. Once inside, deliver [in-app messages](/help/mobile-learning-hub/channels/in-app-messages-overview.md) with personalized promotions (e.g., &quot;Here&#39;s your 15% discount for today&#39;s sale&quot;).

3. Offer [content cards](/help/mobile-learning-hub/channels/content-cards-overview.md) so users can revisit the promotion anytime before it expires (e.g., &quot;Your 15% discount ends Friday&quot;).

4. Use [SMS/MMS/RCS](/help/mobile-learning-hub/channels/sms-mms-rcs-overview.md) to send timely reminders or rich media offers directly to users who may not be in the app.

5. Engage customers in meaningful conversations through [WhatsApp](/help/mobile-learning-hub/channels/whatsapp-overview.md), ideal for customer support or interactive campaigns.

6. Leverage [code-based experiences](/help/mobile-learning-hub/channels/code-based-experience-overview.md) to tailor every message based on user behavior and preferences, creating a truly personalized journey across channels.

## Build your foundation

Learn the concepts and how to

<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
    <a href="configure-and-launch.md"><img src="./assets/configure-message.jpg"></a>
    <div><strong>Configure &amp; Launch</strong><br/>Configure the mobile channeles and integrate with mobile apps.</div>
    </td>
    <td>
    <a href="design-and-deliver.md"><img src="./assets/create-message.webp"></a>
    <div><strong>Design &amp; Deliver</strong><br/>Use mobile channels to build personalized journeys and campaigns that engage customers in real time.</div>
    </td>
    <td>
    <a href="measure-and-optimize.md"><img src="./assets/reports.webp"></a>
    <div><strong>Measure &amp; Optimize</strong><br/>Access reports, analyze performance, and refine strategies for better outcomes.
    </div>
    </td>
  </tr>
</table>

## Common Mobile Business Use Cases

| Caso de uso | Descrição | Mobile Channel Usage |
|---------|-------------|----------------------|
| **App Onboarding and Adoption** | Guides new users through the initial stages of app engagement—installing the app, completing setup, and discovering key features. A meta é maximizar a retenção e o uso a longo prazo. | - Notificações por push e usuários de boas-vindas de SMS e confirmação do perfil.<br>- As mensagens no aplicativo destacam recursos e incentivam as primeiras ações.<br>- Os deep links em emails ou anúncios direcionam os usuários para telas de aplicativos específicas para integração contínua. |
| **Envolvimento Baseado Em Localização** | Fornece mensagens personalizadas e oportunas aos usuários com base em sua proximidade física com lojas, eventos ou outros locais relevantes. | - A delimitação geográfica e o beacon tech disparam notificações por push quando os usuários entram em zonas de destino.<br>- O SMS/MMS fornece ofertas e atualizações localizadas.<br>- Banners e cartões no aplicativo adaptam o conteúdo com base na localização em tempo real. |
| **Abandono do Reengajamento** | Direciona os usuários que abandonam carrinhos, formulários ou sessões de navegação, com o objetivo de trazê-los de volta e concluir a ação desejada. | - As notificações por push lembram os usuários de carrinhos abandonados ou ações incompletas.<br>- Os acompanhamentos por SMS incluem incentivos ou links diretos para serem retomados.<br>- Os prompts no aplicativo aparecem quando os usuários retornam, oferecendo recomendações personalizadas. |
| **Campanhas de venda adicional e venda cruzada** | Promove produtos adicionais ou atualizações para clientes existentes com base em seu comportamento, preferências ou histórico de compras. | - As notificações por push destacam oportunidades relevantes de venda adicional.<br>- As mensagens no aplicativo e os cartões de conteúdo exibem itens complementares.<br>- As campanhas SMS visam públicos segmentados com ofertas exclusivas. |
| **Prevenção de Churn** | Identifica os usuários que correm o risco de sair e os envolve com estratégias personalizadas de retenção para manter a fidelidade. | - A análise preditiva aciona alcance móvel para usuários em risco.<br>- Notificações por push e SMS oferecem recompensas de fidelidade ou conteúdo personalizado.<br>- As pesquisas no aplicativo coletam feedback para melhorar as estratégias de retenção. |
| **Mensagens multicanais** | Orquestra mensagens consistentes em vários canais móveis para garantir que os usuários recebam comunicações oportunas e relevantes. | - Push, no aplicativo, SMS e email são coordenados para a unificação de mensagens.<br>- Os SDKs permitem a personalização em tempo real entre canais.<br>- Os cartões de conteúdo persistem entre as sessões para reforçar as mensagens principais. |

## Casos de uso do cliente

* [Voar com personalização: como as companhias aéreas podem elevar ofertas com o Adobe Journey Optimizer (blog)](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/take-flight-with-personalization-how-airlines-can-elevate-offers/ba-p/767513?profile.language=pt)
