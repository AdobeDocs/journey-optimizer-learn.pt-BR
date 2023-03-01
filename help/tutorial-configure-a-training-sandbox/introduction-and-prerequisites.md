---
title: Configurar uma sandbox de treinamento - introdução
description: Saiba como configurar uma sandbox para fins de treinamento. Percorra as etapas necessárias para configurar os esquemas, assimilar dados de amostra e criar eventos.
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
hide: true
exl-id: 8fa673de-9be9-4ab2-94cf-cfa8ac518223
source-git-commit: 2a671ad01f1cdb60c731a707b0584bf2f4262d9b
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 10%

---

# Configurar uma sandbox de treinamento - Introdução e pré-requisitos

![Tutorial de banner - Configurar uma sandbox de treinamento](./assets/ajo-banner-configure-training-sandbox.png)

Este tutorial foi projetado para administradores e engenheiros de dados com a tarefa de fornecer um Adobe [!DNL Journey Optimizer] ambiente de treinamento. Saiba mais sobre as etapas necessárias para configurar os esquemas, assimilar dados de amostra e criar eventos. Você também cria três perfis de teste que permitem que os alunos verifiquem seu trabalho.

Os dados de amostra fornecidos são baseados em uma empresa fictícia de vestuário atlético chamada _[!DNL Luma]_. [!DNL Luma] O tem lojas em vários países, presença online com um site e aplicativos móveis. [!DNL Luma]A usa o Adobe Journey Optimizer para fornecer experiências conectadas, contextuais e personalizadas aos seus clientes.

No final deste tutorial, você terá uma sandbox compatível com [!DNL Luma] casos de utilização abrangidos pelos exercícios práticos no [Desafios do Journey Optimizer](/help/challenges/introduction-and-prerequisites.md) seção.

## Pré-requisitos

Antes de começar a configurar sua sandbox de treinamento, verifique se você tem:

1. Um projeto de desenvolvimento [sandbox](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/access-control/create-and-manage-sandboxes.html?lang=en).

1. [Predefinições de mensagem de email](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/set-up-email-channel.html?lang=en) configurado para marketing e mensagens transacionais.

1. **[!UICONTROL Administrador do Jornada]** e **[!UICONTROL Gerenciador de dados]** para a sandbox de treinamento.

1. Seu [ID da organização](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=pt-BR).

1. Os arquivos JSON com os dados de amostra, configurados para sua instância do Journey Optimizer:

   1. Baixe o `luma-sample-data.zip` arquivo [aqui](/help/tutorial-configure-a-training-sandbox/assets/luma-data/luma-sample-data.zip), que contém todos os arquivos JSON necessários para este tutorial.

   1. Na pasta de downloads, mova o `luma-data.zip` para o local desejado em seu computador e descompacte-o.

      Esses arquivos contêm os dados de amostra para sua sandbox de treinamento.

   1. Abra cada arquivo e encontre **`yourOrganizationID`** e substitua-o pelo seu [ID da organização](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=pt-BR).

   1. Salve os arquivos.

## Vamos começar

Comece com o [Configuração manual de dados](/help/tutorial-configure-a-training-sandbox/manual-data-set-up.md).

Nesta etapa, você define a estrutura de dados exigida. Após concluir a configuração de dados, você pode assimilar dados na sandbox e configurar eventos.
