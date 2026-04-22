---
title: Push da Web no AJO
description: Este tutorial demonstra como implementar notificações por push da Web usando o Adobe Journey Optimizer (AJO). Você aprenderá a capturar a aceitação de usuários com o Web SDK, enviar notificações por meio de campanhas agendadas e acionar mensagens de push em tempo real usando um evento price.drop personalizado com tags do AEP.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 45f86aeb8fca071436785cc55225d853bb21998f
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Push da Web no Adobe Journey Optimizer

As notificações por push da Web são uma maneira avançada de reengajar os usuários em tempo real, e este tutorial o orienta a implementá-las usando o Adobe Journey Optimizer (AJO). Você começará usando o Web SDK para capturar as preferências de aceitação do usuário para notificações por push, garantindo uma experiência de assinatura contínua e em conformidade. Em seguida, você criará uma campanha para enviar notificações por push aos usuários que aceitaram, permitindo o engajamento com base no público-alvo. Por fim, você aprenderá a usar as tags do AEP para acionar um evento personalizado de queda de preço, que inicia uma jornada no AJO e fornece notificações por push personalizadas e oportunas com base no comportamento do usuário em tempo real.

Exemplo de página da Web para permitir que os usuários aceitem notificações

![habilitar-notificações](assets/enable-notifications.png)

Exemplo de página da Web para acionar o evento de queda de preço

![acionar queda de preço](assets/trigger-price-drop-event.png)

## Pré-requisitos

Este tutorial foi projetado para ser prático e fácil de seguir. Embora não seja necessária uma especialização profunda, será útil ter uma familiaridade básica com os seguintes conceitos:

- Adobe Journey Optimizer (criação de jornadas ou campanhas)
- Coleção de dados do AEP (tags) e a Web SDK
- Conceitos básicos do Adobe Experience Platform, como esquemas e eventos
- Alguns conceitos gerais de desenvolvimento para JavaScript e Web
- Conhecimento básico do Node.js (para gerar chaves VAPID e servir um terminal de configuração simples)

Se você é novo em qualquer uma dessas áreas, não se preocupe. O tutorial guiará você pelas etapas principais ao longo do caminho.
Este tutorial tem como foco a implementação de um caso de uso de notificação por push da Web completo. Portanto, se você tiver conhecimento prático das ferramentas e dos conceitos acima, poderá acompanhá-lo de maneira eficaz.


## 🔔 Habilitar Notificações do Navegador

Se as notificações estiverem bloqueadas ou não aparecerem, talvez seja necessário ativá-las nas configurações do navegador. Consulte as guias abaixo:

- **Google Chrome (Windows/macOS)**\
  <https://support.google.com/chrome/answer/3220216>

- **Microsoft Edge (Windows)**\
  <https://support.microsoft.com/en-us/microsoft-edge/manage-website-notifications-in-microsoft-edge>

- **Safari (macOS)**\
  <https://support.apple.com/guide/safari/customize-website-notifications-sfri40734/mac>

- **Safari (iPhone/iPad)**\
  <https://support.apple.com/en-us/HT213893>


## Aplicativo de amostra


Para ajudá-lo a seguir, um aplicativo de amostra completo está disponível.

- [Demonstração ao Vivo - Aceitar:](https://ajo-web-push.onrender.com/)

- [Evento de Descarte de Preço de Gatilho:](https://ajo-web-push.onrender.com/price-drop-trigger.html)

- [Código Source:](https://github.com/gbedekar489/ajo-web-push)

Você pode explorar a demonstração ao vivo para ver o fluxo em ação ou clonar o repositório para executar o projeto localmente.

