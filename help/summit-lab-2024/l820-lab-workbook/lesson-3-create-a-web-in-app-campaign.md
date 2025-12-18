---
title: Lição 3 - Criar uma campanha da Web no aplicativo
description: Crie e acione uma campanha no aplicativo da Web.
feature: In App
role: User
level: Intermediate
doc-type: Article
duration: 0
recommendations: noDisplay, noCatalog
jira: KT-13983
thumbnail: KT-13983.jpeg
exl-id: 0f84adfb-edb1-47fa-b696-58eec2b33bb1
source-git-commit: 55ba1a46c1473d94847e7fccc69ed2a33badb54c
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 2%

---

# Lição 3 - Criar uma campanha da Web no aplicativo

Agora que você criou experiências móveis para o aplicativo, nesta lição, você cria uma das experiências que viu no site da Fréscopa. Crie uma campanha no aplicativo da Web. Você projeta e personaliza uma mensagem e define um acionador que aciona a mensagem.

## Objetivos de aprendizagem

* Saber como criar uma campanha no aplicativo da Web.
* Acione uma mensagem no aplicativo.

## Exercício 3.1 Criar uma campanha da Web no aplicativo

Neste exercício, você cria a campanha e define em qual página da Web a mensagem no aplicativo aparece.

1. No Journey Optimizer, na navegação à esquerda, em **GERENCIAMENTO DE JORNADA**, selecione **Campanhas**.

1. Clique em **Criar campanha**.

   ![CriarCampanha](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-1-create-campaign.png)

1. Na página **Criar campanha**, na seção **Ação**, marque a caixa de seleção **Mensagem no aplicativo**.

1. Na lista suspensa **Enviar para**, selecione **Web.**

1. Insira a seguinte URL: **https://dsn.adobe.com/web/adobe-summit-2024/exercise** - *Esta é a página da Web em que sua mensagem aparecerá.*

   ![URL no aplicativo](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-1-1-in-app-url.png)

1. Clique em **[!UICONTROL Criar]**.

## Exercício 3.2 Configurar o Campaign

Nesta página, você define as propriedades da campanha e o evento que aciona a mensagem no aplicativo para aparecer na página da Web. Deixe todas as outras configurações no padrão. Para este exercício, não é necessário definir um público-alvo específico.

### 3.2.1 [!UICONTROL Seção Propriedades]

1. Na seção **Propriedades**, dê à sua campanha um **Nome** exclusivo:

   >[!NOTE]
   > Certifique-se de iniciar o nome com o número do seu assento, para que você possa facilmente
   > encontre sua campanha mais tarde.
   > 
   > Por exemplo, se o número da sua cadeira for 99: 
   >
   > ![Nome das Propriedades](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-1-2-properties-name.png)


### 3.2.2 Configurar a regra de acionador personalizada

Nesta seção, você define quais acionadores a mensagem deverá aparecer no site. Você define um acionador exclusivo que permite enviar a mensagem apenas para você mesmo.

1. Role para baixo até a **[!UICONTROL seção Triggers]**, e clique em **[!UICONTROL Editar acionadores]**.

   ![modificar](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-2-1-2-edit-triggers.png)

1. No construtor de regras, clique em **[!UICONTROL Inicialização do Aplicativo]** e, na lista suspensa, selecione *Dados enviados para a Platform*.
   ![menu suspenso de eventos de acionador](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/trigger-drop-down-sent-to-platform.png)

1. Adicione uma condição clicando em **[!UICONTROL + Adicionar condição]**.

   ![botão adicionar condição](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-2-1-3-add-condition.png)

1. No menu suspenso **[!UICONTROL Selecionar uma característica]**, selecione **[!UICONTROL tipo de evento XDM]**.

   ![Tipo de evento XDM](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-1-2-dropdown-xdm-event.png)


1. No campo de texto a seguir, adicione um *`<custom string value>`* do qual você possa se lembrar e pressione **[!UICONTROL Adicionar]** `<custom string value>` para salvar o valor.

   Este valor de sequência de caracteres personalizado é usado posteriormente para acionar sua mensagem.

   >[!TIP]
   > Adicionar o número do assento ao valor de string personalizado tornará isso exclusivo e mais fácil de lembrar.
   > 
   > Por exemplo: `99web`
   > 

   ![adicionar valor de cadeia de caracteres de gatilho personalizado](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-1-2-add-custom-trigger-dropdown.png)

1. Pressione o botão **[!UICONTROL Concluído]** no canto superior direito.

>[!SUCCESS]
>
>Agora você definiu sua mensagem no aplicativo da Web com um evento de acionador personalizado.
>
>![Campanha da Web com gatilho personalizado definido](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-1-2-2-web-campaign-with-custom-trigger.png)


### 3.2.3 Editar o conteúdo da mensagem no aplicativo

Nesta seção, você define o conteúdo, o design e o layout da mensagem.

1. Clique no botão **Editar conteúdo** na seção **Ação** para acessar a construção de criação.

   ![Botão Editar conteúdo](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-1-edit-content-button.png)

1. O processo de criação é o mesmo que você concluiu nos exercícios no aplicativo móvel acima. Edite livremente a mensagem com seu próprio título, corpo e conteúdo de mídia.

   Se você usar o layout modal ou de tela cheia, poderá adicionar um botão. Você pode usar esta URL para abrir a página do produto: **https://dsn.adobe.com/web/adobe-summit-2024/P2WsaDPf_**

1. Quando terminar de editar a mensagem, clique em **[!UICONTROL Revisar para ativar]**.

1. Se tudo estiver bem na tela de revisão, clique em **[!UICONTROL Ativar]** para publicar sua mensagem no aplicativo da Web.

1. Você retornará ao Painel de campanha.

   Aguarde a unidade em que o status da campanha muda para **Live** antes de passar para a versão 4.1.4.

## Exercício 3.3 Acionar a mensagem no aplicativo da Web

1. Vá para o site da Fréscopa e navegue até a página **Exercício** no navegador.

   ![Link de exercícios da Web](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-2-frescopa-web-exercise-link.png)

1. Atualize a página da Web.

1. Digite o valor exclusivo da sequência de caracteres que você definiu na campanha.

   ![página de exercícios](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-2-exercise-page.png)

1. Clique em **[!UICONTROL Enviar]**.

>[!SUCCESS]
>
>Clicar no botão Enviar com seu valor único acionará a mensagem no aplicativo da Web para ser acionada. E você deve ver sua mensagem no aplicativo da Web na tela.
>
>Esse exercício simulou um evento de envio XDM personalizado que você viu por meio da experiência do cliente da Fréscopa.


## Recursos adicionais

**Vídeos explicativos:**

* [Criar uma campanha no aplicativo](/help/channels/create-an-in-app-campaign.md)
* [Criar uma mensagem no aplicativo](/help/channels/author-in-app-messages.md)

**Documentação do produto:**

* [Introdução ao canal no aplicativo](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/get-started-in-app)
* [Criar uma mensagem no aplicativo da Web](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/create-in-app-web)
* [Projete seu conteúdo no aplicativo](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/design-in-app)
* [Verifique e envie sua notificação no aplicativo](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/send-in-app)
