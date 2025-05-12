---
title: Configurar esquema, conjunto de dados e fluxo de dados XDM no AEP
description: Criação de esquema XDM, conjunto de dados e fluxo de dados
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
jira: KT-17923
exl-id: 0efa418a-5b4f-4012-a6fc-afaa34a59285
source-git-commit: 15b2379c251ed0d7583a01fb6af67815322456cf
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Configurar esquema XDM, conjunto de dados e sequência de dados no AEP

## Criar esquema XDM

* Fazer logon no Adobe Experience Platform
* Gerenciamento de dados -> Esquemas -> Criar esquema

* Crie um esquema baseado em eventos XDM chamado _Supervisores Financeiros_. Se você não estiver familiarizado com a criação de um esquema, siga esta [documentação](https://experienceleague.adobe.com/pt-br/docs/experience-platform/xdm/tutorials/create-schema-ui)

* Adicione a estrutura a seguir ao esquema. O elemento PreferredFinancialInstrument armazena a preferência do usuário para Ações, Títulos, CD. O **__techmarketingdemos_**&#x200B;é a ID do locatário e será diferente em seu ambiente.
  ![xdm-schema](assets/xdm-schema.png)

* O elemento PreferredFinancialInstrument tem valores de enumeração definidos como mostrado abaixo
  ![valores-enumeração](assets/enum-values.png)

* Verifique se o esquema está ativado para o perfil.

## Criar um conjunto de dados com base no esquema

Um **conjunto de dados na Adobe Experience Platform (AEP)** é um contêiner de armazenamento estruturado usado para assimilar, armazenar e ativar dados com base em um esquema XDM definido.


* Gerenciamento de dados -> Conjuntos de dados -> Criar conjunto de dados
* Crie um conjunto de dados chamado _Conjunto de dados de Supervisores Financeiros_ com base no esquema XDM (Supervisores Financeiros) criado na etapa anterior.

* Verifique se o conjunto de dados está habilitado para o perfil

## Criar um fluxo de dados

Um fluxo de dados no Adobe Experience Platform é como um pipeline seguro (ou rodovia) que conecta seu site ou aplicativo aos serviços da Adobe, permitindo que os dados fluam e o conteúdo personalizado flua de volta.

* Coleta de dados > Fluxos de dados, em seguida, clique em Nova sequência de dados. Nomeie o fluxo de dados _Fluxo de Dados de Consultores Financeiros_

* Forneça os detalhes a seguir, como mostrado na captura de tela abaixo
  ![sequência de dados](assets/datastream.png)
* Clique em Salvar, em Adicionar mapeamento e adicione o serviço Adobe Experience Platform e o conjunto de dados do evento conforme mostrado
  ![datastream-mapping](assets/datastream-service.png)

* Escolha o conjunto de dados de evento apropriado (criado anteriormente).

* Salvar a sequência de dados

