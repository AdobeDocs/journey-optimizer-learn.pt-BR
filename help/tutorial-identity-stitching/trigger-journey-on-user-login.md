---
title: Acionar a Jornada do Adobe Journey Optimizer usando o Adobe Web SDK
description: Saiba como iniciar uma jornada do Adobe Journey Optimizer a partir de eventos do site, como logons de usuário, aproveitando o AEP Web SDK configurado por meio de Tags do Adobe Experience Platform
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-09-24T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-19287
source-git-commit: c9d62ef509d557b2dfa49c698580df7c4942d299
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 1%

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
* ![jornada-evento](assets/journey-event.png)

* Verifique se eventType do evento é igual a UserLoggedIn. Nesse caso, por questões de simplicidade, o nome e o tipo de evento são os mesmos.`in(@event{event1.eventType}, ['UserLoggedIn'])`
* Salvar o evento

## Criar jornada

* Fazer logon no _**Journey Optimizer**_
* Navegue até _**Gerenciamento de Jornadas > Jornadas > Criar Jornada**_
* Arraste e solte o evento _**UserLoggedIn**_ na tela
* Arraste e solte Email no menu de ações. Configurar a ação de email para usar a configuração de canal de email criada anteriormente
* Publicar a jornada

## Como a jornada é acionada

A jornada é acionada quando a carga do evento enviada via Web SDK corresponde ao que está configurado na jornada. Neste exemplo, o evento e o tipo de evento são **UserLoggedIn**



