---
title: Assimilar dados manualmente
description: Crie conjuntos de dados e assimile dados de amostra manualmente.
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
recommendations: noDisplay, noCatalog
exl-id: 5e7bf81d-4d70-48ef-b357-c361b28359db
source-git-commit: 8a2062f0719e799dd2d039488e6bba943fb458c4
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 8%

---

# Assimilar dados manualmente

Esta seção orienta você pelas etapas necessárias para criar conjuntos de dados e assimilar dados de amostra.

>[!TIP]
>
> Assista ao tutorial em vídeo [Criar conjuntos de dados e assimilar dados](/help/set-up-data/create-datasets-and-ingest-data.md) antes de começar.

Você criará cinco [!UICONTROL conjuntos de dados] baseado no Luma [!UICONTROL esquemas] você criou na [seção anterior](/help/tutorial-configure-a-training-sandbox/manual-data-set-up.md). Após criar os conjuntos de dados, é possível assimilar dados dos arquivos JSON que você baixou e modificou. (Consulte [Introdução e pré-requisitos](/help/tutorial-configure-a-training-sandbox/introduction-and-prerequisites.md) para instruções).

## Criar o primeiro conjunto de dados

Criar um conjunto de dados chamado *[!DNL Luma Loyalty Data]* from [!DNL Luma Loyalty schema]

1. Na navegação à esquerda, em [!UICONTROL GERENCIAMENTO DE DADOS], selecione **[!UICONTROL Conjuntos de dados]**.

1. Selecionar **[!UICONTROL Criar conjunto de dados]**.

   ![Criar um conjunto de dados](assets/create-dataset.png)

1. Na próxima página, selecione [!UICONTROL Criar conjunto de dados a partir do esquema].

   ![Criar um conjunto de dados a partir do esquema](assets/create-dataset-from-schema.png)

1. Na próxima página, pesquise a variável *[!DNL Luma Loyalty]* esquema criado anteriormente.

1. Selecione *[!DNL Luma Loyalty]*.

1. Clique em **[!UICONTROL Próximo]**.

   ![Pesquisar e selecionar esquema](assets/create-dataset-select-schema.png)

1. Configure o conjunto de dados:

   * Nome: `Luma Loyalty Data`

1. Clique em **[!UICONTROL Concluir]**.

   ![Configurar conjunto de dados](assets/create-dataset-configure.png)

## Assimilar dados de amostra

Após criar um conjunto de dados, é possível assimilar dados no conjunto de dados.

1. No [!DNL Luma Loyalty Data] role para baixo na parte inferior do painel direito até a página [!UICONTROL ADICIONAR DADOS] e ativar:

   * **[!UICONTROL Diagnóstico de erros]** e

   * **[!UICONTROL Ingestão parcial]**

   ![Assimilar dados](assets/ingest-data.png)

1. Arraste e solte a `luma-loyalty.json` para carregar dados de amostra no conjunto de dados.

1. Atualize a página e verifique o status do lote para confirmar se o arquivo foi assimilado corretamente.

   375 registros devem ter sido assimilados. Pode levar alguns minutos para que os dados sejam assimilados.

>[!TIP]
>
>Se o lote falhar, verifique se você substituiu a ID da organização no `luma-loyalty.json` com seu [ID da organização](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=pt-BR).

## Crie cinco adicionais [!UICONTROL conjuntos de dados]

Em seguida, crie os cinco adicionais a seguir [!UICONTROL conjuntos de dados] e assimilar os dados no `Luma CRM Data`, o `Luma Products Data`e o `Luma Test Profiles` conjuntos de dados.

| Nome do conjunto de dados | Do esquema | Arquivo a ser assimilado | Registros |
| -----| ------ | -------| ------- |
| `Luma CRM Data` | `Luma CRM` | `luma-crm.json` | 500 |
| `Luma Products Data` | `Luma Products` | `luma-products.json` | 92 |
| `Luma Product Interactions Data` | `Luma Product Interactions` | None | 0 |
| `Luma Product Inventory Events` | `Luma Product Inventory Events` | None | 0 |
| `Luma Test Profiles` | `Luma Test Profiles` | `luma-test-profiles.json` | 3 |

## Próximas etapas

Você criou com êxito todos os conjuntos de dados necessários e assimilou os dados de amostra. A etapa final é [configurar eventos](/help/tutorial-configure-a-training-sandbox/configure-events.md).
