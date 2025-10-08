---
title: 'Lição 4: criar uma campanha por push'
description: Revise os dados do perfil e saiba como criar e enviar aos públicos-alvo uma notificação por push no Journey Optimizer.
feature: Push
role: User
level: Intermediate
doc-type: Tutorial
duration: 0
recommendations: noDisplay, noCatalog
jira: KT-14980
exl-id: 0f82d6a5-18c0-45f2-968e-a678fc2d5768
source-git-commit: 201470e35095b38617d1a1bb5d7b16c1e60f431e
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 2%

---

# Lição 4: criar uma campanha por push

No exercício anterior, o senhor era um entusiasta do café, cliente da Fréscopa. Você interagiu com a marca por meio do site e do aplicativo Fréscopa e recebeu muitas mensagens transacionais. Essas mensagens são acionadas por meio da interação do usuário com o site ou o aplicativo.

Neste exercício, você colocará a tônica do profissional de marketing e implementará uma campanha de marketing para o Frésopa, que utilizará o canal de push para direcionar os usuários do aplicativo Fréscopa. As notificações por push são usadas para manter os usuários do aplicativo informados, mesmo quando eles não estão usando o aplicativo, mas também para engajá-los novamente com o aplicativo. O objetivo é incentivar o cliente a comprar a mistura de casas, oferecendo um desconto de 10%.

## Objetivos de aprendizagem

* Saber como criar uma campanha por push.
* Entenda como criar uma mensagem de push.

<br>

## Exercício 4.1 - Criar uma campanha por push

Neste exercício, você cria a campanha por push, projeta e personaliza a notificação por push, além de enviar a notificação por push para seu próprio dispositivo.

1. No Journey Optimizer, na navegação à esquerda, na seção **[!UICONTROL GERENCIAMENTO DE JORNADAS]**, selecione **Campanhas**.

1. Clique em **[!UICONTROL Criar campanha]**.

   ![Criar campanha](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. Na página **[!UICONTROL Criar campanha]**, na seção **[!UICONTROL Ação]**, marque a caixa de seleção **[!UICONTROL Notificação por push]**.

1. Na lista suspensa **[!UICONTROL Superfície de aplicativo]**, selecione *[!DNL Frecopa-Push]*.

1. Clique em **[!UICONTROL Criar]** para criar uma campanha por push.

   ![Superfície do aplicativo](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-1-2-app-surface.png)

>[!SUCCESS]
>
>Agora você deve estar na página de propriedades do Campaign:
>&#x200B;> ![Propriedades da campanha](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-1-2-campaign-properties.png)

## Exercício 4.2 - Configurar a campanha

Nesta página, você configura as propriedades, o público-alvo, as ações e a programação da campanha.

### 4.2.1 [!UICONTROL Seção de propriedades]

Nomeie a campanha. Certifique-se de iniciar o nome com o número da vaga, para que você possa encontrar facilmente a campanha ao pesquisá-la.

Por exemplo, se o número da sua cadeira for 99: `99 - 10% Discount Campaign`.

### 4.2.2 **[!UICONTROL Seção de público-alvo]**

1. Na seção de público, clique em **[!UICONTROL Selecionar público-alvo]**.

   ![seção de público-alvo](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-2-5-audience-section.png)

1. Na tela **[!UICONTROL Selecionar público-alvo]**, pesquise pelo público-alvo:

   **Laboratório - Sede`your seat number`**

1. Selecione o público e clique em **[!UICONTROL Salvar]**.

   ![seleção de público-alvo](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-2-7-select-audience.png)

### 4.2.3 Editar o conteúdo da notificação por push

Neste exercício, você projeta e personaliza a notificação por push.

1. Na seção **[!UICONTROL Ação]**, clique no botão **[!UICONTROL Editar Conteúdo]**.

   ![Botão Editar conteúdo](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-action-edit-content-button.png)

1. Na próxima tela, dependendo do dispositivo móvel que você tiver, selecione a guia [!DNL iOS™] ou [!DNL Android™] para configurar o seu conteúdo.

>[!BEGINTABS]

>[!TAB iOS]

![guia iOS](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-ios-tab.png)

>[!TAB Android]

![guia Android](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-android-tab.png)

>[!ENDTABS]

#### Seção 4.2.3.1 [!UICONTROL Compor Mensagem]

1. **Redija sua mensagem:** fique à vontade para adicionar qualquer texto que desejar. Estes são exemplos que você pode usar:

   * Título: `Get 10% off today!`
   * Corpo de texto: `Today only! Get 10% off on your House Blend coffee purchase!`

     ![Compor mensagem](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-compose-message.png)

#### 4.2.3.2 Altere o comportamento da mensagem ao clicar para **abrir uma página de produto**

1. Na seção **[!UICONTROL Comportamento ao clicar]**, selecione **[!UICONTROL Deeplink]** na lista suspensa **[!UICONTROL Comportamento ao clicar no corpo]**.

1. Copie e cole a seguinte URL no **campo de URL**:

   `dxdemo://exoticVibes`

   ![deep link](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-deeplink.png)

#### 4.2.3.3 Adicionar uma imagem à mensagem

1. Na seção **[!UICONTROL Adicionar mídia]**, clique em **[!UICONTROL Adicionar mídia]**.

   ![adicionar botões de mídia](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-3-3-add-media-buttons.png)

1. Na tela **[!UICONTROL Selecionar Assets]**, na navegação à esquerda, abra a **pasta Fréscopa** e selecione uma imagem dessa pasta.

   Por exemplo: `HouseBlend.png`

1. Clique na imagem e no botão **[!UICONTROL Selecionar]** para adicionar a imagem à sua notificação por push.

   ![selecionar imagem](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-3-3-select-image.png)

   >[!SUCCESS]
   >
   > 1. Na tela de visualização, clique em **[!UICONTROL Expandir Exibição]**.
   > 1. Pré-visualize a mensagem.
   > <br>
   >
   > ![expandir exibição](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-3-expand-view.png)

### Exercício de bônus

Se você concluiu esta parte do exercício e ainda tem algum tempo, tente o exercício de bônus:

+++ Exercício de bônus

#### Personalizar a mensagem que você está enviando adicionando o nome do destinatário

1. Clique em **caixa de diálogo de personalização** ao lado do campo **[!UICONTROL Corpo]**.

   ![botão de personalização](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-personalization-button.png)

1. Na tela da **caixa de diálogo de personalização**, coloque o cursor onde deseja adicionar o nome no texto.

1. Verifique se os **Atributos do perfil** estão selecionados na navegação à esquerda.

   ![Atributo de perfil](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-personalize-body-profile-attributes.png)

1. No **campo de Pesquisa**, pesquise por: `first name`.

1. Clique em **+** ao lado de **Nome (Atributos do perfil>Pessoa>Nome completo)** para adicionar o campo de personalização ao seu texto.

   ![Pesquisar nome](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-personalize-search-first-name.png)

   >[!SUCCESS]
   >
   > Esta deve ser a aparência do seu texto:
   > 
   >![token do Personalization](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-personalization-token.png)

1. Clique em **[!UICONTROL Salvar]** para salvar a personalização.


   >[!SUCCESS]
   >
   > 1. Na tela de visualização, clique em **[!UICONTROL Expandir Exibição]**.
   > 1. Pré-visualize a mensagem.
   > 
   > ![expandir exibição](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-3-expand-view.png)

+++

### 4.2.4. Revisar e ativar

Se estiver satisfeito com o conteúdo da mensagem, você poderá ativá-la:

1. Clique em **[!UICONTROL Revisar para ativar]**.

   ![botão Revisar e ativar](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-4-review-and-activate-button.png)

1. Na tela **[!UICONTROL Revisar para ativar]**, clique em **[!UICONTROL Ativar]**.

   ![revisar para ativar a tela](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-4-review-to-activate.png)

>[!SUCCESS]
> Na **página de visão geral das campanhas**, encontre sua campanha e verifique o status.
>
> ![status da campanha](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-push-completed.png)
> 
> O status muda de processando para ativo, para concluído - isso pode levar alguns minutos.
> &#x200B;> Quando o status for alterado para concluído:
>
> ![resultados de push](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-push-notification-result.png)

## Recursos adicionais

**Vídeos explicativos:**

* [Configurar e enviar uma campanha por push](/help/channels/create-a-push-campaign.md)

**Documentação do produto:**

* [Introdução à notificação por push](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/push/get-started-push)
* [Criar uma notificação por push](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/push/create-push)
* [Criar uma notificação por push](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/push/design-push)
* [Verificar e enviar sua notificação por push](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/push/send-push)
