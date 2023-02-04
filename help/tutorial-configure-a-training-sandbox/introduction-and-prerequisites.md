---
title: Configurar uma sandbox de treinamento - introdução
description: Saiba como configurar uma sandbox para fins de treinamento. Siga as etapas necessárias para configurar os esquemas, assimilar dados de amostra e criar eventos.
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
hide: true
exl-id: 8fa673de-9be9-4ab2-94cf-cfa8ac518223
source-git-commit: a0f089635df6af8fce9127083ecf582a56b5d569
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 10%

---

# Configurar uma sandbox de treinamento - Introdução e pré-requisitos

![Tutorial de banner - Configurar uma sandbox de treinamento](./assets/ajo-banner-configure-training-sandbox.png)

Este tutorial foi projetado para administradores e engenheiros de dados que têm a tarefa de fornecer um ambiente de treinamento da Adobe Journey Optimizer. Saiba mais sobre as etapas necessárias para configurar os esquemas, assimilar dados de amostra e criar eventos. Você também criará três perfis de teste que permitem aos alunos verificar seu trabalho.

Os dados de amostra fornecidos são baseados em uma empresa ficcional de vestuário atlético chamada _[!DNL Luma]_. [!DNL Luma] O tem lojas em vários países, uma presença online com um site e aplicativos móveis. [!DNL Luma]A usa o Adobe Journey Optimizer para fornecer experiências conectadas, contextuais e personalizadas aos seus clientes.

No final deste tutorial, você terá uma sandbox compatível com o [!DNL Luma] casos de utilização abrangidos pelos exercícios práticos no [Desafios da Journey Optimizer](/help/challenges/introduction-and-prerequisites.md) seção.

## Pré-requisitos

Antes de começar a configurar a sandbox de treinamento, verifique se você tem:

1. Um desenvolvimento dedicado [sandbox](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/access-control/create-and-manage-sandboxes.html?lang=en).
1. [Predefinições de mensagem de email](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/channel-configuration/set-up-email-channel.html?lang=en) configurado para marketing e mensagens transacionais.
1. **[!UICONTROL Administrador do Jornada]** e **[!UICONTROL Gerenciador de dados]** direitos para a sandbox de treinamento.
1. Seu [ID da organização](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=pt-BR).

1. Os arquivos JSON com os dados de amostra, configurados para a instância do Journey Optimizer:

   1. Baixe o `luma-sample-data.zip` arquivo [here](/help/tutorial-configure-a-training-sandbox/assets/luma-data/luma-sample-data.zip), que contém todos os arquivos JSON necessários para este tutorial.

   1. Na pasta de downloads, mova a `luma-data.zip` para o local desejado em seu computador e descompacte-o.

      Esses arquivos contêm os dados de amostra da sandbox de treinamento.

   2. Abra cada arquivo e localize **`yourOrganizationID`** e substitua-o pelo [ID da organização](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=pt-BR).

   3. Salve os arquivos.

## Vamos começar

Comece com o [Configuração manual de dados](/help/tutorial-configure-a-training-sandbox/manual-data-set-up.md). Nesta etapa, você define a estrutura de dados necessária. Após concluir a configuração dos dados, você pode assimilar dados na sandbox e, em seguida, configurar eventos.
