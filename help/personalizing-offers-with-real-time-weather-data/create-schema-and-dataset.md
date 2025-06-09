---
title: Configurar esquema XDM, conjunto de dados e fluxo de dados no AEP
description: Criação de esquema XDM, conjunto de dados e fluxo de dados
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18258
source-git-commit: dac6b373226bd0be2533cf859e4f250018cf568b
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Configurar esquema XDM, conjunto de dados e fluxo de dados no AEP

## Criar esquema XDM

Para usar o Adobe Experience Platform Web SDK (Alloy.js) em uma página da Web, as tags do AEP devem ser associadas a um fluxo de dados mapeado para um esquema de evento XDM. O Web SDK (alloy.sendEvent) envia dados para o AEP como Eventos de Experiência, que devem estar em conformidade com um esquema XDM com base na classe XDM ExperienceEvent.

Para criar um esquema XDM

* Fazer logon no Adobe Experience Platform
* Gerenciamento de dados -> Esquemas -> Criar esquema

* Crie um esquema baseado em eventos XDM chamado **_Weather-Schema_**. Se você não estiver familiarizado com a criação de um esquema, siga esta [documentação](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/create-schema-ui)


* Verifique se o esquema tem os seguintes campos com o tipo de dados apropriado.

![weather-schema](assets/weather-schema.png)

## Criar um conjunto de dados com base no esquema

Um **conjunto de dados na Adobe Experience Platform (AEP)** é um contêiner de armazenamento estruturado usado para assimilar, armazenar e ativar dados com base em um esquema XDM definido.


* Gerenciamento de dados -> Conjuntos de dados -> Criar conjunto de dados
* Crie um conjunto de dados chamado **_Weather-schema-dataset_** com base no esquema XDM(_&#x200B;**Weather-Schema**&#x200B;_) criado na etapa anterior.


## Criar um fluxo de dados

Um fluxo de dados no Adobe Experience Platform é como um pipeline seguro (ou rodovia) que conecta seu site ou aplicativo aos serviços da Adobe, permitindo que os dados fluam e o conteúdo personalizado flua de volta.

* Navegue até Coleção de dados > Fluxos de dados e clique em Novo fluxo de dados. Nomeie a sequência de dados **sequência de dados relacionada ao tempo**


* Forneça os detalhes a seguir, como mostrado na captura de tela abaixo
  ![sequência de dados](assets/datastream.png)
* Clique em Salvar, em Adicionar mapeamento e adicione o serviço Adobe Experience Platform e o Conjunto de dados do evento com as caixas de seleção apropriadas marcadas
  ![datastream-mapping](assets/datastream-service.png)

* Salve o fluxo de dados.
