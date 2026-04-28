---
title: Configurar e iniciar
description: Configure os canais móveis no Adobe Journey Optimizer (AJO) e Adobe Experience Platform (AEP), integre-se a aplicativos móveis e garanta a preparação para a execução da campanha de marketing.
feature: Overview
role: Developer, Admin
level: Beginner, Intermediate
hide: false
index: true
jira: KT-19869
last-substantial-update: 2025-12-18T00:00:00Z
exl-id: d8ffe406-b54b-455f-bd41-7d1fef0a4714
source-git-commit: 3917e11cdf8c0450c19ce653a0964f6dc9da6a3c
workflow-type: tm+mt
source-wordcount: '2976'
ht-degree: 23%

---


# Configurar e iniciar

Para **administradores** e **desenvolvedores de aplicativos móveis**, esta seção mostra como configurar e iniciar canais móveis e da Web no Adobe Journey Optimizer. Ele aborda os pré-requisitos, as permissões e o suporte à plataforma e orienta você na criação de configurações específicas do aplicativo.

>[!IMPORTANT]
>
> Se você é novo no Journey Optimizer e no Experience Platform, familiarize-se com os conceitos principais do gerenciamento de dados no Journey Optimizer fazendo este curso: [Dados do engenheiro para ativação de Jornada inteligente no Adobe Journey Optimizer](https://experienceleague.adobe.com/en/courses/ajo-engineer-data-for-intelligent-journey-activation){target="_blank"}
>

## Recursos para dispositivos móveis no Adobe Journey Optimizer

Entenda quais recursos de publicações de conteúdo para dispositivos móveis a Adobe Journey Optimizer oferece para desenvolvedores, profissionais de marketing e equipes de produtos, incluindo mensagens por push, mensagens no aplicativo e personalização de conteúdo.

>[!VIDEO](https://video.tv.adobe.com/v/342103?quality=12&learn=on){transcript=true}


## Configuração de canais

### Push para dispositivo móvel e no aplicativo

As implementações móveis no Journey Optimizer começam com a integração do **Adobe Experience Platform Mobile SDK** no seu aplicativo. Os SDKs são essenciais para a coleta de dados e a interação com o Adobe Experience Platform (AEP) e seus aplicativos, como o Adobe Journey Optimizer (AJO).

#### O que é o SDK móvel:

O SDK móvel:

* Coleta eventos de aplicativos (exibições de tela, toques, compras, eventos de ciclo de vida etc.) e os envia para a **Adobe Experience Platform Edge Network**.
* Gerencia a **identidade** e o **consentimento**, para que a Journey Optimizer possa criar e usar com segurança perfis de clientes.
* Registers and updates **push tokens**, and sends **push and in‑app tracking events** back to Adobe Experience Platform.
* Integrates with the **[Journey Optimizer mobile extension](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer)** so messages can be delivered, rendered, and measured end‑to‑end.

Without the Mobile SDK integrated in your app, Journey Optimizer cannot reliably:

* Deliver and track mobile push and in‑app messages.
* Render and track content cards.
* Use real‑time in‑app behavior to trigger journeys and personalize experiences.

#### Guided channel setup for new implementations

For new Mobile In-App and Push implementations, Guided Channel Setup is the recommended starting point. It reduces the risk of misconfigured datastreams or missing extensions and walks you through SDK validation with Assurance.

>[!PREREQUISITES]
>
>Make sure you have:
>
> * **Adobe Journey Optimizer** (AJO) provisioned for your org.
> * Adobe Experience Platform access with [Data Collection and Journey Optimizer permissions](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/guided-setup/set-mobile-config#:~:text=Required%20permissions).
> * Admin rights in AJO for channel and configuration setup.
> * Access to your mobile app&#39;s source code (iOS, Android, or cross‑platform framework).
> * Your app has the required OS‑level capabilities enabled (for example, push permissions, notification service extensions, background modes).
> * If you are using the existing configuration option, please ensure that you are using the [current Adobe Experience Platform Mobile SDK versions](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}


>[!VIDEO](https://video.tv.adobe.com/v/3433053/?learn=on)

For more information see [Get started with guided channel setup](https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/guided-setup/set-mobile-config.html?lang=pt-BR){target="_blank"}


#### Manual configuration of the push channel

This following guides walk you through everything you need to manually configure and use push notifications effectively, from understanding the data flow and integrating with services like Firebase and Apple Push Notification Service (APNs) to setting up mobile apps and testing notifications.

<!--
CARDS
* https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs
{title = Push notification data flow and components}
{description = Learn how to setup and understand key services and workflows involved with push notifications in Journey Optimizer.}
{image = https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/media_1f6e99fa57e318230d92f5dde619c450690b5d27a.png?width=2000&format=webply&optimize=medium}
{target = _blank}

* https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-configuration
{image = https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/media_1134ddf9b0f7d39bb365d4884a1d603fd4aa5bbdf.png?width=2000&format=webply&optimize=small}
{target = _blank}
* https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/overview 
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Push notification data flow and components">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs" title="Push notification data flow and components" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/media_1f6e99fa57e318230d92f5dde619c450690b5d27a.png?width=400&format=webply&optimize=medium" alt="Push notification data flow and components"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs" target="_blank" rel="referrer" title="Push notification data flow and components">Push notification data flow and components</a>
                    </p>
                    <p class="is-size-6">Saiba como configurar e entender os principais serviços e fluxos de trabalho envolvidos com notificações por push no Journey Optimizer.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Saiba mais</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Push notification configuration">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-configuration" title="Configuração da notificação por push" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/media_1134ddf9b0f7d39bb365d4884a1d603fd4aa5bbdf.png?width=400&format=webply&optimize=small" alt="Configuração da notificação por push"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-configuration" target="_blank" rel="referrer" title="Configuração da notificação por push">Configuração de notificação por push</a>
                    </p>
                    <p class="is-size-6">Saiba como configurar seu ambiente para enviar notificações por push com o Journey Optimizer</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-configuration" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Saiba mais</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Implement Adobe Experience Cloud in mobile apps tutorial">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/overview" title="Tutorial Implementar o Adobe Experience Cloud em aplicativos para dispositivos móveis" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/overview./media_1c75750ec1be623e56a379ca69ef6c495799e52a5.png?width=400&format=png&optimize=medium" alt="Tutorial Implementar o Adobe Experience Cloud em aplicativos para dispositivos móveis"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/overview" target="_blank" rel="referrer" title="Tutorial Implementar o Adobe Experience Cloud em aplicativos para dispositivos móveis">Tutorial: Implementar a Adobe Experience Cloud em aplicativos para dispositivos móveis</a>
                    </p>
                    <p class="is-size-6">Saiba como implementar os aplicativos móveis do Adobe Experience Cloud. Este tutorial o orienta por uma implementação de aplicativos Experience Cloud em um aplicativo Swift ou Android de amostra.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/overview" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Saiba mais</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

#### Recursos adicionais


<!--
CARDS
* https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk
{target = _blank}
* https://developer.adobe.com/client-sdks/home/base/assurance
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Get the Adobe Experience Platform Mobile SDK">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk" title="Obter o Adobe Experience Platform Mobile SDK" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://developer.adobe.com/shared/images/adobe-social-share.png" alt="Obter o Adobe Experience Platform Mobile SDK"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk" target="_blank" rel="referrer" title="Obter o Adobe Experience Platform Mobile SDK">Obter o Adobe Experience Platform Mobile SDK</a>
                    </p>
                    <p class="is-size-6">Um guia que explica como instalar o Adobe Experience Platform Mobile SDK em seu aplicativo.</p>
                </div>
                <a href="https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Saiba mais</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Experience Platform Assurance overview">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/client-sdks/home/base/assurance" title="Visão geral do Adobe Experience Platform Assurance" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://developer.adobe.com/shared/images/adobe-social-share.png" alt="Visão geral do Adobe Experience Platform Assurance"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/client-sdks/home/base/assurance" target="_blank" rel="referrer" title="Visão geral do Adobe Experience Platform Assurance">visão geral do Adobe Experience Platform Assurance</a>
                    </p>
                    <p class="is-size-6">Uma visão geral da extensão para dispositivos móveis do Adobe Experience Platform Assurance.</p>
                </div>
                <a href="https://developer.adobe.com/client-sdks/home/base/assurance" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Saiba mais</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

#### Lista de verificação de preparação para o Mobile SDK

Antes de entregar o aplicativo aos profissionais de marketing, confirme no **[Assurance](https://developer.adobe.com/client-sdks/home/base/assurance/){target="_blank"}** que:

>[!SUCCESS]
> 
> [ ] Extensões do Core SDK + Journey Optimizer foram carregadas,\
> [ ] Eventos estão fluindo na sequência de dados e nos conjuntos de dados corretos,\
> [ ]A identidade e o consentimento estão presentes em todos os eventos principais,\
> [ ] tokens de push e interações são rastreados e\
> [ ] Pelo menos uma mensagem no aplicativo de teste ou cartão de conteúdo foi exibido e gravado como uma impressão.


### Cartões de conteúdo

<!--
CARDS
* https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp
{title = Configure content cards support in Mobile SDK}
{description = Learn how to integrate content cards in your mobile application using Messaging SDK.}
{image = https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/media_17623afb1c5e280b7fb6861b4003d0ef8f8bea24d.jpg?width=2000&format=webply&optimize=medium}
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure content cards support in Mobile SDK">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp" title="Configurar o suporte a cartões de conteúdo no SDK móvel" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/media_17623afb1c5e280b7fb6861b4003d0ef8f8bea24d.jpg?width=400&format=webply&optimize=medium" alt="Configurar o suporte a cartões de conteúdo no SDK móvel"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp" target="_blank" rel="referrer" title="Configurar o suporte a cartões de conteúdo no SDK móvel">Configurar suporte a cartões de conteúdo no Mobile SDK</a>
                    </p>
                    <p class="is-size-6">Learn how to integrate content cards in your mobile application using Messaging SDK.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Saiba mais</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

### WhatsApp

Understand how to configure the **WhatsApp channel**:

<!--
CARDS
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up the WhatsApp channel">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel" title="Configurar o canal do WhatsApp" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3470268/?format=jpeg&nocache=1765310599408" alt="Configurar o canal do WhatsApp"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel" target="_blank" rel="referrer" title="Configurar o canal do WhatsApp">Configurar o canal do WhatsApp</a>
                    </p>
                    <p class="is-size-6">Este tutorial apresentará a configuração do canal do WhatsApp no Adobe Journey Optimizer para habilitar mensagens comerciais em tempo real.</p>
                </div>
                <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

### SMS/MMS/RCS

Configure **SMS/MMS/RCS channels** with the standard providers (Twilio,Synch or Infobip) or using a custom SMS provider:

<!--
CARDS
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-sms-channel
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-custom-sms-provider
{description = Learn how to configure custom SMS providers in Journey Optimizer, set up API credentials and webhooks, manage opt-in/opt-out keywords, and launch personalized campaigns.}
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-mms-api-credentials-and-channel-surfaces
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-rcs
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure SMS API credentials and channel surfaces">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-sms-channel" title="Configurar credenciais da API de SMS e superfícies de canal" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3413355?format=jpeg&nocache=1765310599850" alt="Configurar credenciais da API de SMS e superfícies de canal"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-sms-channel" target="_blank" rel="referrer" title="Configurar credenciais da API de SMS e superfícies de canal">Configure SMS API credentials and channel surfaces</a>
                    </p>
                    <p class="is-size-6">Saiba como conectar o Journey Optimizer a um provedor de serviços de SMS e como criar uma superfície de canal de SMS.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-sms-channel" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure a custom SMS provider">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-custom-sms-provider" title="Configurar um provedor de SMS personalizado" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3431625/?format=jpeg&nocache=1765310599834" alt="Configurar um provedor de SMS personalizado"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-custom-sms-provider" target="_blank" rel="referrer" title="Configurar um provedor de SMS personalizado">Configurar um provedor de SMS personalizado</a>
                    </p>
                    <p class="is-size-6">Learn how to configure custom SMS providers in Journey Optimizer, set up API credentials and webhooks, manage opt-in/opt-out keywords, and launch personalized campaigns.</p>
                </div>
                <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-custom-sms-provider" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure MMS API credentials and channel surfaces">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-mms-api-credentials-and-channel-surfaces" title="Configurar credenciais da API de MMS e superfícies de canal" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3428872/?format=jpeg&nocache=1765310599863" alt="Configurar credenciais da API de MMS e superfícies de canal"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-mms-api-credentials-and-channel-surfaces" target="_blank" rel="referrer" title="Configurar credenciais da API de MMS e superfícies de canal">Configurar credenciais da API de MMS e superfícies de canal</a>
                    </p>
                    <p class="is-size-6">Saiba como conectar o Journey Optimizer a um provedor de serviços de MMS e como criar uma superfície de canal de MMS.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-mms-api-credentials-and-channel-surfaces" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up RCS in Journey Optimizer">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-rcs" title="Configurar RCS no Journey Optimizer" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3464755/?format=jpeg&nocache=1765310600192" alt="Configurar RCS no Journey Optimizer"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-rcs" target="_blank" rel="referrer" title="Configurar RCS no Journey Optimizer">Configurar RCS no Journey Optimizer</a>
                    </p>
                    <p class="is-size-6">Saiba como configurar e enviar mensagens RCS interativas e da marca no Adobe Journey Optimizer, usando um provedor de SMS personalizado. Este tutorial explica a configuração de credenciais de API, webhooks e configurações de canal, e, em seguida, como criar uma jornada para fornecer experiências de mensagens complexas e personalizadas, tudo dentro do aplicativo de mensagens nativo.</p>
                </div>
                <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-rcs" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Ensure compliance with privacy laws and platform guidelines.

<!--
CARDS
* https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/consent
* https://experienceleague.adobe.com/en/docs/journey-optimizer/using/privacy/privacy-landing-page{image=../mobile-learning-hub/assets/privacy.webp}{title = Privacy Features in Adobe Journey Optimizer}{description = Learn how to process privacy requests, audit user actions, manage consent, apply governance rules, and leverage advanced security options like Customer Managed Keys.}
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/data-governance-framework
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/classify-data-using-lables
{cta = Watch}
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/create-data-usage-policies
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Implement consent for Platform Mobile SDK implementations">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/consent" title="Implement consent for Platform Mobile SDK implementations" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/consent./media_12356d2400b5ad641e8356a6883441b38a129c968.png?width=400&format=png&optimize=medium" alt="Implement consent for Platform Mobile SDK implementations"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/consent" target="_blank" rel="referrer" title="Implement consent for Platform Mobile SDK implementations">Implementar consentimento para implementações do Platform Mobile SDK</a>
                    </p>
                    <p class="is-size-6">Saiba como implementar o consentimento em um aplicativo móvel.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/consent" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Saiba mais</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Privacy Features in Adobe Journey Optimizer">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/privacy/privacy-landing-page" title="Recursos de privacidade do Adobe Journey Optimizer" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../mobile-learning-hub/assets/privacy.webp" alt="Recursos de privacidade do Adobe Journey Optimizer"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/privacy/privacy-landing-page" target="_blank" rel="referrer" title="Recursos de privacidade do Adobe Journey Optimizer">Recursos de privacidade no Adobe Journey Optimizer</a>
                    </p>
                    <p class="is-size-6">Saiba como processar solicitações de privacidade, auditar ações do usuário, gerenciar o consentimento, aplicar regras de governança e aproveitar opções avançadas de segurança, como Chaves gerenciadas pelo cliente.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/privacy/privacy-landing-page" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Saiba mais</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Data Governance Framework Overview">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/data-governance-framework" title="Visão geral da estrutura de governança de dados" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/29708/?format=jpeg&nocache=1765310600883" alt="Visão geral da estrutura de governança de dados"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/data-governance-framework" target="_blank" rel="referrer" title="Visão geral da estrutura de governança de dados">Visão geral da estrutura de governança de dados</a>
                    </p>
                    <p class="is-size-6">Compreenda os recursos de governança da Adobe Experience Platform.</p>
                </div>
                <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/data-governance-framework" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Classify data using labels">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/classify-data-using-lables" title="Classificar dados usando rótulos" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/29709?format=jpeg&nocache=1765310600887" alt="Classificar dados usando rótulos"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/classify-data-using-lables" target="_blank" rel="referrer" title="Classificar dados usando rótulos">Classificação de dados usando rótulos</a>
                    </p>
                    <p class="is-size-6">Saiba como aplicar rótulos a esquemas e conjuntos de dados.</p>
                </div>
                <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/classify-data-using-lables" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Create Data Usage Policies">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/create-data-usage-policies" title="Criar políticas de uso de dados" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/32977/?format=jpeg&nocache=1765310600676" alt="Criar políticas de uso de dados"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/create-data-usage-policies" target="_blank" rel="referrer" title="Criar políticas de uso de dados">Criar políticas de uso de dados</a>
                    </p>
                    <p class="is-size-6">Saiba como criar e gerenciar políticas de uso de dados.</p>
                </div>
                <a href="https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/create-data-usage-policies" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->


## Armadilhas comuns na implementação e como evitá-las

A maioria dos problemas de publicação de conteúdo para dispositivos móveis tem origem no **SDK ou na configuração da coleção de dados**, não nas jornadas ou campanhas do Journey Optimizer propriamente ditas. Use a tabela abaixo para identificar o que está errado e, em seguida, expanda a seção correspondente para obter detalhes.

### Principais armadilhas

| # | Problema/sintoma | Armadilha comum | Visão geral das correções |
|---|----------------------------------------------|-----------------------------------------------------|------------------------------------------|
| 1 | Falha na configuração do canal guiado; sem tráfego ou com tráfego baixo | [Versões ou extensões do SDK não alinhadas](#1-sdk-versions-and-extensions-not-aligned-with-channel-requirements) | Atualizar versões do SDK/extension; validar no Assurance |
| 2 | Falha no rastreamento de lotes; erros no AEP | [Datastreams ou conjuntos de dados configurados incorretamente](#2-misconfigured-datastreams-or-datasets) | Mapear eventos para conjunto de dados de evento e perfis para conjunto de dados de perfil |
| 3 | As jornadas não são acionadas; personalização estranha | [Identidade ou consentimento ausente/inconsistente](#3-missing-or-inconsistent-identity-and-consent) | Implementar a verificação de identidade e consentimento do Edge no Assurance |
| 4 | Nenhuma entrega por push ou abertura em relatórios | [Registro do token de push ou rastreamento interrompido](#4-push-token-registration-and-tracking-not-wired-correctly) | Corrigir o registro de token e o rastreamento de interação por meio do SDK |
| 5 | Não há impressões no aplicativo apesar das campanhas ativas | [Mensagens no aplicativo ou cartões de conteúdo não são exibidos](#5-in-app-messages-or-content-cards-not-displaying) | Verificar extensões de mensagens, acionadores e respostas de decisões da Assurance |

### Orientação detalhada por armadilha

Abra a armadilha que corresponde aos seus sintomas para ver o que verificar e como corrigi-la.

+++ &#x200B;1. Versões e extensões do SDK não alinhadas aos requisitos do canal
**O que você observará**

* As atividades de push ou no aplicativo não chegam ao dispositivo.
* Falha na Configuração de Canal Guiado ou na validação de canal.
* O Assurance mostra o Journey Optimizer, o Edge ou as extensões de identidade ausentes.

**O que verificar**

* Você está usando as versões mínimas de extensão do **Mobile Core** e do **Journey Optimizer** necessárias para a Configuração de Canal Guiado?
* Em **Assurance**, em extensões e eventos:
   * Você vê as extensões esperadas carregadas?
   * Os eventos estão sendo enviados para a Edge Network e confirmados?

**Como corrigir**

* Atualize para as versões compatíveis da extensão do Mobile SDK e do Journey Optimizer.
* Recrie o aplicativo, reconecte-se ao Assurance e execute novamente a Configuração de canal guiada.

Consulte: [Configurar dispositivos móveis e a Web](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/configuration/guided-setup/set-mobile-config){target="_blank"}

+++

+++ &#x200B;2. Sequências de dados ou conjuntos de dados configurados incorretamente
**O que você observará**

* Eventos ou lotes de rastreamento de push falham em conjuntos de dados da plataforma.
* Erros de assimilação de dados (por exemplo, &quot;Atualizações não são compatíveis com eventos&quot;).
* Relatórios por push ou no aplicativo mostram pouco ou nenhum rastreamento.

**O que verificar**

* Alguém alterou **esquemas do sistema ou conjuntos de dados** criados para rastreamento do Journey Optimizer?
* Na sua **sequência de dados**:
   * Os eventos de experiência estão mapeados para um **conjunto de dados de evento**?
   * Os atributos de perfil estão mapeados para um **conjunto de dados de perfil**?

**Como corrigir**

* Não edite conjuntos de dados/esquemas do sistema criados pela AJO.
* Corrija o mapeamento do fluxo de dados (eventos → conjunto de dados do evento, perfis → conjunto de dados do perfil).
* Prefira a Configuração de canal guiada ou as etapas de sequência de dados documentadas em vez de alterações ad hoc.

Consulte: [Fluxo de notificação por push no Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs){target="_blank"}

+++

+++ &#x200B;3. Identidade e consentimento ausentes ou inconsistentes
**O que você observará**

* O Jornada não é acionado conforme esperado pelos usuários do aplicativo.
* O Personalization não corresponde ao comportamento do usuário em outros canais.
* Os eventos aparecem no Experience Platform, mas os perfis parecem fragmentados.

**O que verificar**

* A **Identidade do Edge Network** foi implementada e está enviando uma ID primária estável (por exemplo, ID de logon)?
* O **Consentimento para o Edge Network** é implementado e atualizado quando as preferências são alteradas?
* Em **Assurance**:
   * Do outbound events include consent values?
   * Do they include ECID and your primary IDs consistently?

**Como corrigir**

* Implement or correct **Identity for Edge Network** in the app.
* Implement **Consent for Edge Network** and connect it to your app&#39;s consent UI.
* Retest in Assurance until identity and consent appear on all relevant events.

See: [Implement consent for Platform Mobile SDK implementations](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/consent){target="_blank"}

+++

+++ 4. Push token registration and tracking not wired correctly
**O que você observará**

* Users never receive push notifications, even though campaigns or journeys run.
* Push reports show no opens, dismisses, or interactions.

**O que verificar**

* Does the app register the push token with the Journey Optimizer extension:
   * On first install?
   * After each app update?
   * Whenever the OS refreshes the token?
* When a user opens or dismisses a notification, do you see tracking events in Assurance?

**Como corrigir**

* Add or correct the code that:
   * Registers the token via the Journey Optimizer mobile extension whenever it is created or refreshed.
   * Sends push interaction events (open, dismiss, custom actions) via the Mobile SDK.
* Use Assurance to confirm registration and tracking events are firing as expected.

Consulte: [Fluxo de notificação por push no Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs){target="_blank"}

+++

+++ 5. In‑app messages or content cards not displaying
**O que você observará**

* As mensagens no aplicativo ou os cartões de conteúdo nunca aparecem, apesar das campanhas ou jornadas ativas.
* Os relatórios mostram 0 impressões.

**O que verificar**

* A **Journey Optimizer mobile messaging / extensão no aplicativo** e a **Messaging SDK** estão instaladas e registradas no aplicativo?
* Na configuração de **tags**:
   * Você tem regras que acionam solicitações nos eventos corretos (por exemplo, exibições de tela ou eventos personalizados)?
* Em **Assurance**:
   * Quando esses eventos são acionados, você vê solicitações de decisão no aplicativo ou no cartão de conteúdo sendo enviadas?
   * Você vê respostas vindas da Edge Network?

**Como corrigir**

* Instale e registre as extensões de mensagens necessárias.
* Adicione ou corrija regras que acionam decisões nos eventos de destino (telas, eventos personalizados).
* Para cartões de conteúdo, certifique-se de:
   * Busque cartões por meio das APIs do Messaging SDK.
   * Renderizá-los na interface do usuário.
   * Rastrear interações por meio da SDK.

Consulte:
* [Criar e enviar mensagens no aplicativo](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/experience-cloud/journey-optimizer/journey-optimizer-inapp){target="_blank"}
* [Configurar o suporte a cartões de conteúdo no SDK móvel](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp){target="_blank"}

+++

## Recursos adicionais

* [Usar a personalização do lado do cliente (ODD) baseada em CDN em dispositivos móveis para personalizações mais rápidas (Blog)](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/using-cdn-based-client-side-personalization-odd-on-mobile-for/ba-p/761626){target="_blank"}
* [O segredo para o próximo nível do engajamento e crescimento do aplicativo móvel (sessão de cúpula)](https://business.adobe.com/summit/2025/sessions/the-secret-to-nextlevel-mobile-app-engagement-s603.html)
