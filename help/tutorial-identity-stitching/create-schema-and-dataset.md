---
title: Configurar esquema XDM, conjunto de dados e fluxo de dados no AEP
description: Criação de esquema XDM, conjunto de dados e fluxo de dados
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-18089
exl-id: 8bb85ba7-3c50-4596-88f8-e112c48a8253
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d2971708-e780-44bb-9e2a-72f139796afd
    internal-label: Customer
subfeature_v2:
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%
---
# Configurar esquema XDM, conjunto de dados e fluxo de dados no AEP

## Criar esquema XDM

Para usar o Adobe Experience Platform Web SDK (Alloy.js) em uma página da Web, as tags do AEP devem ser associadas a um fluxo de dados mapeado para um esquema de evento XDM. O Web SDK (alloy.sendEvent) envia dados para o AEP como Eventos de Experiência, que devem estar em conformidade com um esquema XDM com base na classe XDM ExperienceEvent.

Para criar um esquema XDM

* Fazer logon no Adobe Experience Platform
* Gerenciamento de dados -> Esquemas -> Criar esquema

* Crie um esquema baseado em eventos XDM chamado **_Supervisores Financeiros_**. Se você não estiver familiarizado com a criação de um esquema, siga esta [documentação](https://experienceleague.adobe.com/pt-br/docs/experience-platform/xdm/tutorials/create-schema-ui)


* Verifique se o esquema está ativado para o perfil.

## Criar um conjunto de dados com base no esquema

Um **conjunto de dados na Adobe Experience Platform (AEP)** é um contêiner de armazenamento estruturado usado para assimilar, armazenar e ativar dados com base em um esquema XDM definido.


* Gerenciamento de dados -> Conjuntos de dados -> Criar conjunto de dados
* Crie um conjunto de dados chamado **_Conjunto de dados de Supervisores Financeiros_** com base no esquema XDM (Supervisores Financeiros) criado na etapa anterior.

* Verifique se o conjunto de dados está habilitado para o perfil

## Criar um fluxo de dados

Um fluxo de dados no Adobe Experience Platform é como um pipeline seguro (ou rodovia) que conecta seu site ou aplicativo aos serviços da Adobe, permitindo que os dados fluam e o conteúdo personalizado flua de volta.

* Navegue até Coleção de dados > Fluxos de dados e clique em Novo fluxo de dados. Nomeie o fluxo de dados **_Fluxo de Dados de Consultores Financeiros_**

* Forneça os detalhes a seguir, como mostrado na captura de tela abaixo
  ![sequência de dados](assets/datastream.png)
* Clique em Salvar, em Adicionar mapeamento e adicione o serviço Adobe Experience Platform e o conjunto de dados do evento conforme mostrado
  ![datastream-mapping](assets/datastream-service.png)

* Escolha o conjunto de dados de evento apropriado (criado anteriormente).

* Salve o fluxo de dados.
