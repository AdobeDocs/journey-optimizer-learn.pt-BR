---
title: Configurar uma sandbox de treinamento - Introdução
description: Saiba como configurar uma sandbox para fins de treinamento. Siga as etapas necessárias para configurar os esquemas, assimilar dados de amostra e criar eventos.
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
jira: KT-9382
role: Admin
level: Beginner
last-substantial-update: 2023-02-01T00:00:00.000Z
exl-id: 8fa673de-9be9-4ab2-94cf-cfa8ac518223
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
    internal-label: Data management activity
  - id: d556b755-390a-43f0-be32-a08cf6236126
    internal-label: Configuration
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
    internal-label: Sandboxes
  - id: efb19423-4da4-4fd1-88d8-5ee8c71ae766
    internal-label: Application settings
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 100%
---
# Configurar uma sandbox de treinamento - Introdução e pré-requisitos

![Tutorial de banner - Configurar uma sandbox de treinamento](./assets/ajo-banner-configure-training-sandbox.png)

Este tutorial foi desenvolvido para administradores e engenheiros de dados que possuem a tarefa de fornecer um ambiente de treinamento do Adobe [!DNL Journey Optimizer]. Saiba mais sobre as etapas necessárias para configurar os esquemas, assimilar dados de amostra e criar eventos. Você também criará três perfis de teste que permitem verificar o seu trabalho.

Os dados de amostra fornecidos são baseados em uma empresa fictícia de vestuário atlético chamada _[!DNL Luma]_. A [!DNL Luma] tem lojas em vários países, um site para operações online e aplicativos móveis. A [!DNL Luma] usa o Adobe Journey Optimizer para fornecer experiências conectadas, contextuais e personalizadas aos seus clientes.

No final deste tutorial, você terá uma sandbox que atende aos casos de uso da [!DNL Luma] abrangidos pelos exercícios práticos na seção [Desafios do Journey Optimizer](/help/challenges/introduction-and-prerequisites.md).

## Pré-requisitos

Antes de começar a configurar sua sandbox de treinamento, certifique-se de que você tem:

1. Uma [sandbox](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/access-control/create-and-manage-sandboxes.html?lang=pt-br) de desenvolvimento dedicada.

1. [Predefinições de mensagem de email](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/set-up-email-channel.html?lang=pt-BR) configuradas para mensagens transacionais e de marketing.

1. Direitos de **[!UICONTROL administrador de jornada]** e **[!UICONTROL gerente de dados]** para a sandbox de treinamento.

1. Sua [ID de organização](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=pt-BR).

1. Os arquivos JSON com os dados de amostra, configurados para sua instância do Journey Optimizer:

   1. Baixe o arquivo `luma-sample-data.zip` [aqui](/help/tutorial-configure-a-training-sandbox/assets/luma-data/luma-sample-data.zip). Ele contém todos os arquivos JSON necessários para este tutorial.

   1. Na pasta de downloads, mova o arquivo `luma-data.zip` para o local desejado em seu computador e descompacte-o.

      Esses arquivos contêm os dados de amostra para sua sandbox de treinamento.

   1. Abra cada arquivo e encontre a **`yourOrganizationID`** e substitua-a por sua [ID de organização](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=pt-BR).

   1. Salve os arquivos.

## Vamos começar

Comece com a [configuração manual de dados](/help/tutorial-configure-a-training-sandbox/manual-data-set-up.md).

Nesta etapa, você definirá a estrutura de dados necessária. Após concluir a configuração de dados, você pode assimilar dados na sandbox e, em seguida, configurar eventos.
