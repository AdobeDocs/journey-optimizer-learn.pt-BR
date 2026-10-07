---
title: Acionar a Jornada do Adobe Journey Optimizer usando o Adobe Web SDK
description: Saiba como iniciar uma jornada do Adobe Journey Optimizer a partir de eventos do site, como logons de usuário, usando o SDK da web da AEP configurado por meio de tags da Adobe Experience Platform
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-09-24T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-19287
exl-id: c6d4f720-3780-4012-a2bd-8eae23599144
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d2971708-e780-44bb-9e2a-72f139796afd
    internal-label: Customer
subfeature_v2:
  - id: ef9a83ca-eefa-47cf-aa34-f1a34715583a
    internal-label: Profiles
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 10%
---
# Acionar a Jornada do Adobe Journey Optimizer usando o Adobe Web SDK

Nesta extensão do tutorial de Compilação de identidade, a jornada do Adobe Journey Optimizer é acionada para enviar um email ao usuário conectado usando seu perfil compilado. **Este artigo supõe que você esteja familiarizado com o canal de email e com a criação de conteúdo para o canal de email.**

## Criar configuração de canal de email

* Fazer logon no _**Journey Optimizer**_
* Navegue até _**Administração -> Canais -> Criar configuração de canal**_
* Selecione **Email** na lista de canais. Forneça um nome e uma descrição significativos.
* Preencha as configurações de email.
* Forneça os detalhes da execução conforme mostrado abaixo. O email é enviado para o endereço de email do perfil armazenado no campo
* ![canal-email](assets/email-channel-execution.png)
* Ativar a configuração do canal de email

## Criar evento

* Fazer logon no _**Journey Optimizer**_
* Navegue até _**Administração -> Configurações**_
* Clique no botão Gerenciar do cartão Eventos e clique em Criar evento. Especifique os valores conforme mostrado abaixo
* ![jornada-evento](assets/journey-event1.png)

* Verifique se eventType do evento é igual a LoginEvent. O tipo `LoginEvent` está definido na Marca Adobe Experience Platform.
* Salvar o evento

## Criar Jornada

* Fazer logon no _**Journey Optimizer**_
* Navegue até _**Gerenciamento de Jornadas > Jornadas > Criar Jornada**_
* Arraste e solte o evento _**UserLoggedIn**_ na tela
* Arraste e solte Email no menu de ações. Configure a ação de email para usar a configuração de canal de email criada anteriormente.
* Publique a jornada.

## Como a jornada é acionada

A jornada é acionada quando a carga do evento enviada via Web SDK corresponde ao que está configurado na jornada. Neste exemplo, o tipo de evento é `UserLoggedIn` e é `LoginEvent`.

* Verifique isso exibindo o relatório de jornada
* ![relatório-jornada](assets/journey-triggered-report.png)
