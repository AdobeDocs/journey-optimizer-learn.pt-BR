---
title: Configurar esquema, conjunto de dados e fluxo de dados XDM no AEP
description: Criação de esquema XDM, conjunto de dados e fluxo de dados
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00.000Z
jira: KT-17923
exl-id: 0efa418a-5b4f-4012-a6fc-afaa34a59285
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
source-wordcount: '284'
ht-degree: 0%
---
# Configurar esquema XDM, conjunto de dados e sequência de dados no AEP

## Criar esquema XDM

* Fazer logon no Adobe Experience Platform
* Gerenciamento de dados -> Esquemas -> Criar esquema

* Crie um esquema baseado em eventos XDM chamado _Supervisores Financeiros_. Se você não estiver familiarizado com a criação de um esquema, siga esta [documentação](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/create-schema-ui)

* Adicione a estrutura a seguir ao esquema. O elemento PreferredFinancialInstrument armazena a preferência do usuário para Ações, Títulos, CD. O **__techmarketingdemos_**é a ID do locatário e será diferente em seu ambiente.
  ![xdm-schema](assets/xdm-schema.png)

* O elemento PreferredFinancialInstrument tem valores de enumeração definidos como mostrado abaixo
  ![valores-enumeração](assets/enum-values.png)

* Verifique se o esquema está ativado para o perfil.

## Criar um conjunto de dados com base no esquema

Um **conjunto de dados na Adobe Experience Platform (AEP)** é um contêiner de armazenamento estruturado usado para assimilar, armazenar e ativar dados com base em um esquema XDM definido.


* Gerenciamento de dados -> Conjuntos de dados -> Criar conjunto de dados
* Crie um conjunto de dados chamado _Conjunto de dados de Supervisores Financeiros_ com base no esquema XDM (Supervisores Financeiros) criado na etapa anterior.

* Verifique se o conjunto de dados está habilitado para o perfil

## Criar um fluxo de dados

Um fluxo de dados no Adobe Experience Platform é como um pipeline seguro (ou rodovia) que conecta seu site ou aplicativo aos serviços da Adobe, permitindo que os dados fluam e o conteúdo personalizado flua de volta.

* Coleta de dados > Fluxos de dados, em seguida, clique em Nova sequência de dados. Nomeie o fluxo de dados _Fluxo de Dados de Consultores Financeiros_

* Forneça os detalhes a seguir, como mostrado na captura de tela abaixo
  ![sequência de dados](assets/datastream.png)
* Clique em Salvar, em Adicionar mapeamento e adicione o serviço Adobe Experience Platform e o conjunto de dados do evento conforme mostrado
  ![datastream-mapping](assets/datastream-service.png)

* Escolha o conjunto de dados de evento apropriado (criado anteriormente).

* Salvar a sequência de dados

