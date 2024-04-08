---
title: 'Lição 2: criar uma campanha móvel no aplicativo'
description: Crie e acione uma campanha móvel no aplicativo.
feature: In App
role: User
level: Intermediate
doc-type: Article
duration: 0
recommendations: noDisplay, noCatalog
jira: KT-14983
thumbnail: KT-14983.jpeg
exl-id: fe18eca7-229c-4867-ab34-1862bad63124
source-git-commit: 4f5c92f79eba3651b3633b7850e993160cb1f72c
workflow-type: tm+mt
source-wordcount: '1434'
ht-degree: 1%

---

# Lição 2: criar uma campanha móvel no aplicativo

Nesta lição, você cria e aciona mensagens móveis no aplicativo.

## Objetivos de aprendizagem

* Entenda como as mensagens no aplicativo são acionadas.
* Saber como criar uma campanha móvel no aplicativo.
* Acione uma mensagem no aplicativo.

## Exercício 2.1 - Fazer logon no Journey Optimizer

1. Abertura [Adobe Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-ajo-lab/journey-optimizer/home){target="_blank"}
2. Faça logon usando os seguintes detalhes:
   <br>
   **Nome de usuário:** L820+**`<your seat number>`**@adobeeventlab.com
   **Senha:**   Adobe2024!
   <br>
Você pode encontrar os detalhes para fazer login no desktop da sua máquina de laboratório. Use a Adobe ID e a senha.
   ![desktop](/help/summit/l820-lab-workbook/assets/desk-top.png)

   ![Tela de login](/help/summit/l820-lab-workbook/assets/2-1-1-ajo-sign-in.png)
   <br>
3. Você pode pular as próximas duas telas:
   <br>
   ![Número de telefone](/help/summit/l820-lab-workbook/assets/2-1-3-ajo-add-phone.png)
   <br>
   ![Pop-up de personalização](/help/summit/l820-lab-workbook/assets/2-1-4-ajo-personalization-pop-up.png)


>[!SUCCESS]
>
>Você deve estar conectado ao Journey Optimizer e na página inicial:
>
>![Página inicial do AJO](/help/summit/l820-lab-workbook/assets/2-1-5-ajo-homepage.png)


## Exercício 2.2 Criar uma campanha móvel no aplicativo

Neste exercício, você cria uma campanha de mensagens no aplicativo, que é acionada ao abrir o aplicativo.

1. No Journey Optimizer, na navegação à esquerda, selecione **[!UICONTROL Campanhas]**.

1. Clique em **[!UICONTROL Criar campanha]**.

   ![Criar campanha](/help/summit/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. No **[!UICONTROL Criar campanha]** página, no campo  **[!UICONTROL Ação]** , selecione a **[!UICONTROL Mensagem no aplicativo]** caixa de seleção

1. No **[!UICONTROL Enviar para]** selecione **[!DNL Mobile]**.

1. No **[!UICONTROL Superfície do aplicativo]** selecione **[!DNL Frecopa Mobile App]**.

1. Clique em **[!UICONTROL Criar]**.

   ![Superfície do aplicativo](/help/summit/l820-lab-workbook/assets/3-1-1-1-create.png)

>[!SUCCESS]
>
>Agora você deve estar nas propriedades do Campaign:
>
> ![Propriedades da campanha](/help/summit/l820-lab-workbook/assets/3-1-1-2-campaign-properties.png)

## Exercício 2.3 Configurar sua campanha

### 2.3.1 [!UICONTROL seção Propriedades]

Nomeie a campanha. Certifique-se de iniciar o nome com o número da vaga, para que você possa encontrar facilmente a campanha novamente.

Por exemplo, se o número da sua cadeira for 99:  `99 - Welcome Campaign`.

![seção de propriedades](/help/summit/l820-lab-workbook/assets/3-1-2-1-properties-section.png)

### 2.3.2 Configurar a regra de acionador personalizada

1. Role para baixo até **[!UICONTROL Seção Acionadores]** e, em seguida, clique em **[!UICONTROL Editar acionadores]**.

   ![modificar](/help/summit/l820-lab-workbook/assets/3-2-1-2-edit-triggers.png)

1. No construtor de regras, clique em **[!UICONTROL Inicialização do aplicativo]** e, na lista suspensa, selecione  *Dados enviados para a plataforma*.
   ![Enviado para a plataforma de dados](/help/summit/l820-lab-workbook/assets/trigger-drop-down-sent-to-platform.png)

1. Adicione uma condição clicando em **[!UICONTROL Adicionar condição]**.

   ![botão adicionar condição](/help/summit/l820-lab-workbook/assets/3-2-1-3-add-condition.png)

1. No **[!UICONTROL Selecionar uma característica]** selecione **[!UICONTROL Tipo de evento XDM]**.

   ![Tipo de evento XDM](/help/summit/l820-lab-workbook/assets/4-1-2-dropdown-xdm-event.png)

1. No campo de texto a seguir, adicione uma *`<custom string value>`* que você pode lembrar.

1. Para salvar o valor, clique em **[!UICONTROL Adicionar**] `<custom string value>`.

   Este valor de sequência de caracteres personalizado é usado posteriormente para acionar sua mensagem.

   >[!TIP]
   > Adicionar o número do assento ao valor da string personalizada torna isso exclusivo e mais fácil de lembrar.
   > 
   > Por exemplo: `99exerciseTrigger`

   ![adicionar valor de string de acionador personalizado](/help/summit/l820-lab-workbook/assets/3-1-2-2-add-custom-trigger.png)

1. Clique em **[!UICONTROL Concluído]** no canto superior direito.

>[!SUCCESS]
>
>Agora você definiu a mensagem no aplicativo com um evento de acionador personalizado.
>
>![Campanha com acionador personalizado definido](/help/summit/l820-lab-workbook/assets/3-1-2-2-campaign-with-custom-trigger.png)


### 2.3.3 Editar o conteúdo da mensagem no aplicativo

No **[!UICONTROL Ação]** clique em **[!UICONTROL Editar conteúdo]**.

![Botão Editar conteúdo](/help/summit/l820-lab-workbook/assets/3-1-3-1-edit-content-button.png)

A variável [!UICONTROL Mensagem no aplicativo] editor é exibido, onde você configura o conteúdo da mensagem no aplicativo.

#### 2.3.3.1 Layout

Selecione qual layout deve ser aplicado à mensagem.

Por exemplo, clique **[!UICONTROL Modal]** para tornar sua mensagem no aplicativo um layout modal.

![botão modal](/help/summit/l820-lab-workbook/assets/3-1-3-2-modal-button.png)

#### 2.3.3.2 Criação da mensagem e publicação da campanha

1. Na seção de mídia, cole no seguinte URL:  `https://t3.ftcdn.net/jpg/02/79/42/52/240_F_279425217_Hr9VBkknMr4fTpuZbxZXfcYdC7jSvGl2.jpg`
   <br>
Ao clicar fora do campo de valor, a imagem deve aparecer.

   ![mídia mostrada na pré-visualização](/help/summit/l820-lab-workbook/assets/3-1-3-2-media.png)

2. No seguinte **[!UICONTROL Conteúdo]** adicione em seu próprio texto personalizado que você deseja que seja exibido na mensagem para **[!UICONTROL Cabeçalho]** e **[!UICONTROL Corpo]**.

   ![Cabeçalho e corpo](/help/summit/l820-lab-workbook/assets/3-1-3-2-content.png)

3. Opções adicionais:
   1. **Botões:**

      ![Seção de botões](/help/summit/l820-lab-workbook/assets/3-1-3-2-buttons.png)

      1. Nesta seção do editor, você pode personalizar o texto do botão CTA editando o campo Texto do botão.

      2. A variável **[!UICONTROL Interagir evento]** O campo é usado para definir o valor passado para o SDK quando o CTA é pressionado pelo usuário.

      3. A variável **[!UICONTROL Target]** é usado para definir para onde o CTA levará o usuário. Isso inclui URLs e Deeplinks. Por exemplo, é possível adicionar esse deep link a uma página de produto, como `dxdemo://exoticVibes`.

      4. Você pode adicionar outros botões pressionando **[!UICONTROL + Botão Adicionar]**.

      5. Quando um segundo botão é adicionado à mensagem, agora há a opção de alterar o layout do botão com a caixa suspensa.


   2. **Formatação avançada**

      ![alternância de formatação avançada](/help/summit/l820-lab-workbook/assets/3-1-3-2-advanced-formatting-toggle.png)

      Ativar essa opção fornecerá opções de personalização adicionais no editor.

      1. Tamanho da mídia
      1. Fonte
      1. Tamanho Pt
      1. Cor da fonte
      1. Alinhamento

      ![opções avançadas de formatação](/help/summit/l820-lab-workbook/assets/3-1-3-2-advanced-formatting-options.png)

   3. **Guia Configurações**

      Ao mudar para essa guia e na guia **[!UICONTROL Visualizar]** é possível alterar a configuração **Visualização do aplicativo**.
      <br>\
      ![Guia Configurações](/help/summit/l820-lab-workbook/assets/3-1-3-1-settings-tab.png)
      <br>

      1. A variável **[!UICONTROL Layout]** fornece a opção de usar uma imagem como plano de fundo ou cor sólida.

      2. A variável **[!UICONTROL Mensagem]** A seção fornece interações personalizadas que podem ser habilitadas para sua mensagem:
         1. Gestos personalizados
         2. Tomada de controle da interface
         3. Tomada de controle da interface personalizada
         4. Tamanho personalizado
         5. Posição personalizada
         6. Animação personalizada
         7. Canto arredondado da mensagem
   <br>
4. Quando terminar a criação do conteúdo e estiver satisfeito com a mensagem, clique no link **[!UICONTROL Revisar para ativar] botão**.

   >[!SUCCESS]
   >
   > Você concluiu a criação da mensagem móvel no aplicativo. Agora você deve estar na Campanha **[!UICONTROL Revisar para ativar]** página.
   >
   >![revisar e ativar](/help/summit/l820-lab-workbook/assets/3-1-4-1-review-and-activate.png)
   >
   > Aqui você poderá ver um resumo completo da sua mensagem.
   >
   > *Anote o valor personalizado usado ao acionar a regra. Esse valor será usado para acionar a mensagem no aplicativo. O valor usado pode ser encontrado na área de destaque da página de resumo.*

   >[!NOTE]
   >O acionador atual da mensagem no aplicativo é o padrão **Ocorre um evento de inicialização de aplicativo**, o que significa que a mensagem no aplicativo é acionada quando o aplicativo é iniciado. Você pode ver isso no **[!UICONTROL seção Programação]**.

5. Se tiver terminado de revisar sua Campanha, pressione o botão Ativate para publicar a Campanha.
   <br>
   ![ativar](/help/summit/l820-lab-workbook/assets/3-1-4-2-activate.png)


>[!SUCCESS]
>
> Agora você deve ver o painel Campanhas. Localize sua campanha rolando ou usando o recurso de pesquisa. Quando a campanha muda o status para **[!UICONTROL Ao vivo]** (~1min), sua campanha foi publicada.
>
> ![Campanha publicada](/help/summit/l820-lab-workbook/assets/3-1-3-2-published-campaign.png)
>


## Exercício 2.4 Acionar a mensagem no aplicativo móvel

Para atualizar a carga e baixar a campanha recém-publicada:

1. Em seu dispositivo móvel, feche completamente o aplicativo Fréscopa.
2. Reabra o aplicativo Fréscopa.
3. Agora navegue até a guia Exercício no aplicativo.

   ![Botão Exercício](/help/summit/l820-lab-workbook/assets/3-2-3-app-exercise-button.png)

4. No campo de texto, digite o valor do acionador personalizado definido no Campaign. Em seguida, pressione Enviar.


   ![modificar](/help/summit/l820-lab-workbook/assets/3-2-2-1-app-condition.PNG){width="250" align="center" zoomable="yes"}

>[!SUCCESS]
>
>Ao clicar em enviar, você acionou manualmente um acionador e a notificação no aplicativo criada é exibida:
>
>![Mensagem no aplicativo](/help/summit/l820-lab-workbook/assets/3-1-3-3-in-app-message.png)
>
> *Se tiver problemas para acionar a mensagem, verifique o seguinte:*
> 
> * *No campo Nome do evento no aplicativo móvel, digite o valor da regra de acionador exatamente como você o tinha no Campaign.*
> * *Verifique se as letras maiúsculas estão corretas e se você não tem um espaço à esquerda ou à direita.*
> * *Você pode pesquisar o valor da regra de acionador usado se voltar para a página de revisão da campanha clicando novamente na campanha no Painel da campanha.*

Você acabou de criar e publicar sua primeira mensagem no aplicativo do Journey Optimizer!


## Exercício de bônus: Campanha e Pré-visualização duplicadas no dispositivo

A variável **Duplicar campanha** e **Visualizar no dispositivo** Os recursos do são funcionalidades prontas para uso que permitem duplicar suas Campanhas e testar e revisar suas mensagens no aplicativo diretamente no dispositivo antes de ativá-las. Neste exercício, você aprenderá a usar esse recurso e a visualizar a mensagem criada no exercício 3.1.

1. Abra a campanha que acabou de criar clicando no nome da campanha na página Campaigns dashboard para abri-la. Isso o levará de volta ao **[!UICONTROL Campanha de revisão]** página.
1. Pressione a **[!UICONTROL Botão Duplicar]**. Isso abrirá um novo prompt para nomear a nova campanha que está sendo duplicada. Adicione um novo nome do qual você se lembre facilmente ou use o nome padrão, onde **[!DNL _copy]** é adicionado por padrão.

   ![campanha duplicada](/help/summit/l820-lab-workbook/assets/3-2-duplicate-campaign.png)

1. Depois que você pressionar o botão duplicate, sua campanha duplicada será criada e você será direcionado ao Painel de Campanhas.
1. Depois que a campanha for duplicada, abra a nova campanha.

1. Você pode acessar o recurso Visualizar no dispositivo no **[!UICONTROL Revisão da campanha]** ou na página **[!UICONTROL Autor da campanha]** etapa.

   ![botão visualizar no dispositivo](/help/summit/l820-lab-workbook/assets/3-3-1-1-preview-on-device-button.png)
   <br>

1. Clique em **[!UICONTROL botão iniciar]** na tela conectar ao dispositivo.

   ![botão iniciar](/help/summit/l820-lab-workbook/assets/3-3-1-2-connect-to-device-start.png)
   <br>

1. Insira o url base que foi configurado para iniciar o aplicativo Fréscopa: `dxdemo://`

   ![url de visualização](/help/summit/l820-lab-workbook/assets/3-3-1-3-preview-url.png)

   <br>

1. Siga as instruções na tela:
   1. Digitalize o código QR com seu dispositivo móvel e o aplicativo Fréscopa será aberto com uma tela que permite inserir um pino exibido.
   2. Insira o pino mostrado no AJO na tela Assurance no seu dispositivo e clique no botão Connect (Conectar), que aparece na parte inferior direita depois que você insere o pino.


   ![insira o pin](/help/summit/l820-lab-workbook/assets/3-3-1-5-enter-pin.PNG){width="250" align="center" zoomable="yes"}
   <br>
1. Este pop-up é exibido na tela do computador

   ![pop-up](/help/summit/l820-lab-workbook/assets/3-3-pop-up.png)

1. Clique no botão Concluído. Isso fechará a caixa de diálogo e seu telefone será conectado à Visualização no dispositivo.


>[!SUCCESS]
>
> A mensagem no aplicativo aparece no dispositivo.
>
> *Depois de conectada, a mensagem no aplicativo deverá ser exibida sempre que você clicar no link **[!UICONTROL Visualizar no dispositivo] botão**.

## Recursos adicionais

**Vídeos explicativos:**

* [Criar uma campanha no aplicativo](/help/channels/create-an-in-app-campaign.md)
* [Criar uma mensagem no aplicativo](/help/channels/author-in-app-messages.md)

**Documentação do produto:**

* [Introdução ao canal no aplicativo](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/get-started-in-app)
* [Criar uma mensagem no aplicativo móvel](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/create-in-app)
* [Projete seu conteúdo no aplicativo](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/design-in-app)
* [Verifique e envie sua notificação no aplicativo](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/send-in-app)
