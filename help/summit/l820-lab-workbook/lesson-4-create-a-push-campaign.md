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
source-git-commit: c590b47ad3dfc54badbac0d8fcaff6b9dd053cc1
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

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

1. No Journey Optimizer, na navegação à esquerda, no campo de **[!UICONTROL GERENCIAMENTO DE JORNADAS]** , selecione **Campanhas**.

1. Clique em **[!UICONTROL Criar campanha]**.

   ![Criar campanha](/help/summit/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. No **[!UICONTROL Criar campanha]** página, no campo  **[!UICONTROL Ação]** , selecione a **[!UICONTROL Notificação por push]** caixa de seleção

1. No **[!UICONTROL Superfície do aplicativo]** selecione *[!DNL Frecopa-Push]*.

1. Clique em **[!UICONTROL Criar]** para criar uma campanha por push.

   ![Superfície do aplicativo](/help/summit/l820-lab-workbook/assets/2-3-1-2-app-surface.png)

>[!SUCCESS]
>
>Agora você deve estar na página de propriedades do Campaign:
> ![Propriedades da campanha](/help/summit/l820-lab-workbook/assets/2-3-1-2-campaign-properties.png)

## Exercício 4.2 - Configurar a campanha

Nesta página, você configura as propriedades, o público-alvo, as ações e a programação da campanha.

### 4.2.1 [!UICONTROL seção Propriedades]

Nomeie a campanha. Certifique-se de iniciar o nome com o número da vaga, para que você possa encontrar facilmente a campanha ao pesquisá-la.

Por exemplo, se o número da sua cadeira for 99: `99 - 10% Discount Campaign`.

### 4.2.2 **[!UICONTROL Seção Público]**

1. Na seção de público, clique em **[!UICONTROL Selecionar público]**.

   ![seção público](/help/summit/l820-lab-workbook/assets/2-3-2-5-audience-section.png)

1. No **[!UICONTROL Selecionar público]** pesquise pelo público:

   **Laboratório - Assento`your seat number`**

1. Selecione o público e clique em **[!UICONTROL Salvar]**.

   ![seleção de público](/help/summit/l820-lab-workbook/assets/2-3-2-7-select-audience.png)

### 4.2.3 Editar o conteúdo da notificação por push

Neste exercício, você projeta e personaliza a notificação por push.

1. No **[!UICONTROL Ação]** clique na guia **[!UICONTROL Editar conteúdo] botão**.

   ![Botão Editar conteúdo](/help/summit/l820-lab-workbook/assets/2-3-action-edit-content-button.png)

1. Na próxima tela, dependendo do dispositivo móvel que você tiver, selecione [!DNL iOS™] ou [!DNL Android™] para configurar o conteúdo.

>[!BEGINTABS]

>[!TAB iOS]

![Guia iOS](/help/summit/l820-lab-workbook/assets/2-3-ios-tab.png)

>[!TAB Android]

![Guia Android](/help/summit/l820-lab-workbook/assets/2-3-android-tab.png)

>[!ENDTABS]

#### 4.2.3.1. [!UICONTROL Compor mensagem] seção

1. **Redija sua mensagem:** Fique à vontade para adicionar qualquer texto que desejar. Estes são exemplos que você pode usar:

   * Título: `Get 10% off today!`
   * Corpo de texto: `Today only! Get 10% off on your House Blend coffee purchase!`

     ![Compor mensagem](/help/summit/l820-lab-workbook/assets/2-3-compose-message.png)

#### 4.2.3.2 Altere o comportamento da mensagem ao clicar para **abrir uma página de produto**

1. No **[!UICONTROL Comportamento ao clicar]** , selecione **[!UICONTROL Deeplink]** do **[!UICONTROL Comportamento de clique no corpo]** lista suspensa.

1. Copie e cole o seguinte URL na **Campo de URL**:

   `dxdemo://exoticVibes`

   ![deep link](/help/summit/l820-lab-workbook/assets/2-3-deeplink.png)

#### 4.2.3.3 Adicionar uma imagem à mensagem

1. No **[!UICONTROL Adicionar mídia]** clique em **[!UICONTROL Adicionar mídia]**.

   ![adicionar botões de mídia](/help/summit/l820-lab-workbook/assets/2-3-3-3-add-media-buttons.png)

1. No **[!UICONTROL Selecionar ativos]** , na navegação à esquerda, abra a variável **Pasta Fréscopa** e selecione uma imagem dessa pasta.

   Por exemplo: `HouseBlend.png`

1. Clique na imagem e clique no ícone **[!UICONTROL Selecionar] botão** para adicionar a imagem à sua notificação por push.

   ![selecionar imagem](/help/summit/l820-lab-workbook/assets/2-3-3-3-select-image.png)

   >[!SUCCESS]
   >
   > 1. Na tela de pré-visualização, clique em **[!UICONTROL Expandir visualização]**.
   > 1. Pré-visualize a mensagem.
   > <br>
   >
   > ![expandir visualização](/help/summit/l820-lab-workbook/assets/2-3-3-expand-view.png)

### Exercício de bônus

Se você concluiu esta parte do exercício e ainda tem algum tempo, tente o exercício de bônus:

+++ Exercício de bônus

#### Personalizar a mensagem que você está enviando adicionando o nome do destinatário

1. Clique em **caixa de diálogo de personalização** ao lado da **[!UICONTROL Corpo]** campo.

   ![botão de personalização](/help/summit/l820-lab-workbook/assets/2-3-personalization-button.png)

1. No **caixa de diálogo de personalização** , coloque o cursor onde deseja adicionar o nome no texto.

1. Certifique-se de que o **Atributos do perfil** são selecionados na navegação à esquerda.

   ![Atributo de perfil](/help/summit/l820-lab-workbook/assets/2-3-personalize-body-profile-attributes.png)

1. No **Campo de pesquisa**, pesquisar por: `first name`.

1. Clique em **+** ao lado da **Nome (Atributos do perfil>Pessoa>Nome completo)** para adicionar o campo de personalização ao texto.

   ![Pesquisar nome](/help/summit/l820-lab-workbook/assets/2-3-personalize-search-first-name.png)

   >[!SUCCESS]
   >
   > Esta deve ser a aparência do seu texto:
   > 
   >![Token de personalização](/help/summit/l820-lab-workbook/assets/2-3-personalization-token.png)

1. Clique em **[!UICONTROL Salvar]** para salvar a personalização.


   >[!SUCCESS]
   >
   > 1. Na tela de pré-visualização, clique em **[!UICONTROL Expandir visualização]**.
   > 1. Pré-visualize a mensagem.
   > 
   > ![expandir visualização](/help/summit/l820-lab-workbook/assets/2-3-3-expand-view.png)

+++

### 4.2.4. Revisar e ativar

Se estiver satisfeito com o conteúdo da mensagem, você poderá ativá-la:

1. Clique em **[!UICONTROL Revisar para ativar]**.

   ![botão revisar e ativar](/help/summit/l820-lab-workbook/assets/2-3-4-review-and-activate-button.png)

1. No **[!UICONTROL Revisar para ativar]** clique em **[!UICONTROL Ativar]**.

   ![revisar para ativar a tela](/help/summit/l820-lab-workbook/assets/2-3-4-review-to-activate.png)

>[!SUCCESS]
> No **Página de visão geral das campanhas**, encontre sua campanha e verifique o status.
>
> ![status da campanha](/help/summit/l820-lab-workbook/assets/2-3-push-completed.png)
> 
> O status muda de processando para ativo, para concluído - isso pode levar alguns minutos.
> Quando o status for alterado para concluído:
>
> ![resultados de push](/help/summit/l820-lab-workbook/assets/2-3-push-notification-result.png)


**Obrigado!**

Obrigado por sua participação. Forneça-nos feedback sobre como o fizemos e se o laboratório atendeu às suas expectativas, respondendo à pesquisa da sessão do Lab 820 no aplicativo Summit.

