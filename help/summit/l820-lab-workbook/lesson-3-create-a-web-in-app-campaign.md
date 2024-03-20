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
source-git-commit: c509c768d07984d07ed2ec65634e000c54bb6ff1
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---



# Lição 3 - Criar uma campanha da Web no aplicativo

Agora que você criou experiências móveis para o aplicativo, nesta lição, você cria uma das experiências que viu no site da Fréscopa. Crie uma campanha no aplicativo da Web. Você projeta e personaliza uma mensagem e define um acionador que aciona a mensagem.

## Objetivos de aprendizagem

* Saber como criar uma campanha no aplicativo da Web.
* Acione uma mensagem no aplicativo.

## Exercício 3.1 Criar uma campanha da Web no aplicativo

Neste exercício, você cria a campanha e define em qual página da Web a mensagem no aplicativo aparece.

1. No Journey Optimizer, na navegação à esquerda, em **GERENCIAMENTO DE JORNADAS** selecionar **Campanhas**.

1. Clique em **Criar campanha**.

   ![CreateCampaign](/help/summit/l820-lab-workbook/assets/4-1-create-campaign.png)

1. No **Criar campanha** página, no campo **Ação** , selecione a **Mensagem no aplicativo** caixa de seleção

1. No **Enviar para** selecione **Web.**

1. Insira o seguinte URL: **https://dsn.adobe.com/web/adobe-summit-2024/exercise** - *Esta é a página da Web na qual sua mensagem será exibida.*

   ![URL no aplicativo](/help/summit/l820-lab-workbook/assets/4-1-1-in-app-url.png)

1. Clique em **[!UICONTROL Criar]**.

## Exercício 3.2 Configurar o Campaign

Nesta página, você define as propriedades da campanha e o evento que aciona a mensagem no aplicativo para aparecer na página da Web. Deixe todas as outras configurações no padrão. Para este exercício, não é necessário definir um público-alvo específico.

### 3.2.1 [!UICONTROL seção Propriedades]

1. No **Propriedades** dê à sua campanha um perfil exclusivo **Nome**:

   >[!NOTE]
   > Certifique-se de iniciar o nome com o número do seu assento, para que você possa facilmente
   > encontre sua campanha mais tarde.
   > 
   > Por exemplo, se o número da sua cadeira for 99: 
   >
   > ![Nome das propriedades](/help/summit/l820-lab-workbook/assets/4-1-2-properties-name.png)


### 3.2.2 Configurar a regra de acionador personalizada

Nesta seção, você define quais acionadores a mensagem deverá aparecer no site. Você define um acionador exclusivo que permite enviar a mensagem apenas para você mesmo.

1. Role para baixo até **[!UICONTROL Seção Acionadores]** e, em seguida, clique em **[!UICONTROL Editar acionadores]**.

   ![modificar](/help/summit/l820-lab-workbook/assets/3-2-1-2-edit-triggers.png)

1. No construtor de regras, clique em **[!UICONTROL Inicialização do aplicativo]** e, na lista suspensa, selecione  *Dados enviados para a plataforma*.
   ![menu suspenso acionar evento](/help/summit/l820-lab-workbook/assets/trigger-drop-down-sent-to-platform.png)

1. Adicione uma condição clicando em **[!UICONTROL + Adicionar condição]**.

   ![botão adicionar condição](/help/summit/l820-lab-workbook/assets/3-2-1-3-add-condition.png)

1. No **[!UICONTROL Selecionar uma característica]** selecione **[!UICONTROL Tipo de evento XDM]**.

   ![Tipo de evento XDM](/help/summit/l820-lab-workbook/assets/4-1-2-dropdown-xdm-event.png)


1. No campo de texto a seguir, adicione uma *`<custom string value>`* que você consegue lembrar e pressione **[!UICONTROL Adicionar]** `<custom string value>` para salvar o valor.

   Este valor de sequência de caracteres personalizado é usado posteriormente para acionar sua mensagem.

   >[!TIP]
   > Adicionar o número do assento ao valor de string personalizado tornará isso exclusivo e mais fácil de lembrar.
   > 
   > Por exemplo: `99web`
   > 

   ![adicionar valor de string de acionador personalizado](/help/summit/l820-lab-workbook/assets/4-1-2-add-custom-trigger-dropdown.png)

1. Pressione a **[!UICONTROL Concluído]** no canto superior direito.

>[!SUCCESS]
>
>Agora você definiu sua mensagem no aplicativo da Web com um evento de acionador personalizado.
>
>![Campanha da Web com acionador personalizado definido](/help/summit/l820-lab-workbook/assets/4-1-2-2-web-campaign-with-custom-trigger.png)


### 3.2.3 Editar o conteúdo da mensagem no aplicativo

Nesta seção, você define o conteúdo, o design e o layout da mensagem.

1. Clique em **Editar conteúdo** botão na caixa **Ação** seção para acessar a construção de criação.

   ![Botão Editar conteúdo](/help/summit/l820-lab-workbook/assets/3-1-3-1-edit-content-button.png)

1. O processo de criação é o mesmo que você concluiu nos exercícios no aplicativo móvel acima. Edite livremente a mensagem com seu próprio título, corpo e conteúdo de mídia.

   Se você usar o layout modal ou de tela cheia, poderá adicionar um botão. Você pode usar esse URL para abrir a página do produto: **https://dsn.adobe.com/web/adobe-summit-2024/P2WsaDPf_**

1. Quando terminar de editar a mensagem, clique em **[!UICONTROL Revisar para ativar]**.

1. Se tudo estiver bem na tela de revisão, clique em **[!UICONTROL Ativar]** para publicar sua mensagem no aplicativo da Web.

1. Você retornará ao Painel de campanha.

   Unidade de espera para a qual o status da campanha muda **Ao vivo** antes de passar para o 4.1.4.

## Exercício 3.3 Acionar a mensagem no aplicativo da Web

1. Acesse o site da Fréscopa e acesse o **Exercício** página no seu navegador.

   ![Link de exercícios da Web](/help/summit/l820-lab-workbook/assets/4-2-frescopa-web-exercise-link.png)

1. Atualize a página da Web.

1. Digite o valor exclusivo da sequência de caracteres que você definiu na campanha.

   ![página de exercícios](/help/summit/l820-lab-workbook/assets/4-2-exercise-page.png)

1. Clique em **[!UICONTROL Enviar]**.

>[!SUCCESS]
>
>Clicar no botão Enviar com seu valor único acionará a mensagem no aplicativo da Web para ser acionada. E você deve ver sua mensagem no aplicativo da Web na tela.
>
>Esse exercício simulou um evento de envio XDM personalizado que você viu por meio da experiência do cliente da Fréscopa.
