---
title: Configurar uma sandbox de treinamento - Introdução
description: Saiba como configurar uma sandbox para fins de treinamento. Siga as etapas necessárias para configurar os esquemas, assimilar dados de amostra e criar eventos.
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
jira: KT-9382
role: Admin
level: Beginner
last-substantial-update: 2023-02-01T00:00:00Z
exl-id: 8fa673de-9be9-4ab2-94cf-cfa8ac518223
source-git-commit: 81f5cc22d46f89ee1c7164a92988311ca6036b8b
workflow-type: ht
source-wordcount: '338'
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
