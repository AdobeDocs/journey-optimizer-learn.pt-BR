---
title: Configurar esquema XDM, conjunto de dados, sequência de dados e públicos no AEP
description: Criação de esquema XDM, conjunto de dados, sequência de dados e públicos-alvo
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
jira: KT-17923
source-git-commit: f970a1780b1bdf717675cd79c98a38ac422a679f
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---


# Configurar esquema XDM, conjunto de dados, sequência de dados e públicos no AEP

* Fazer logon no Adobe Experience Platform

* Crie um esquema baseado em eventos XDM chamado Supervisores financeiros no Journey Optimizer. Se você não estiver familiarizado com a criação de um esquema, siga esta [documentação](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/create-schema-ui)

* Adicione a estrutura a seguir ao esquema. O elemento PreferredFinancialInstrument armazena a preferência do usuário para Ações, Títulos, CD
  ![xdm-schema](assets/xdm-schema.png)

* O elemento PreferredFinancialInstrument tem valores de enumeração definidos como mostrado abaixo
  ![valores-enumeração](assets/enum-values.png)

* Verifique se o esquema está ativado para o perfil.

## Criar um conjunto de dados com base no esquema

Um **conjunto de dados na Adobe Experience Platform (AEP)** é um contêiner de armazenamento estruturado usado para assimilar, armazenar e ativar dados com base em um esquema XDM definido.

* Crie um conjunto de dados chamado _Conjunto de dados de Supervisores Financeiros_ com base no esquema XDM (Supervisores Financeiros) criado na etapa anterior.

* Verifique se o conjunto de dados está habilitado para o perfil

## Criar um fluxo de dados

Um fluxo de dados no Adobe Experience Platform é como um pipeline seguro (ou rodovia) que conecta seu site ou aplicativo aos serviços da Adobe, permitindo que os dados fluam e o conteúdo personalizado flua de volta.

* Vá para AEP > Fluxos de dados e clique em Novo fluxo de dados. Nomeie o fluxo de dados _Fluxo de Dados de Consultores Financeiros_

* Forneça os detalhes a seguir, como mostrado na captura de tela abaixo
  ![sequência de dados](assets/datastream.png)
* Clique em Salvar, em Adicionar mapeamento e adicione o serviço Adobe Experience Platform e o conjunto de dados do evento conforme mostrado
  ![datastream-mapping](assets/datastream-service.png)

* Escolha o conjunto de dados de evento apropriado (criado anteriormente).

* Salvar a sequência de dados

## Criar públicos-alvo

Os públicos-alvo no Adobe Experience Platform são grupos de usuários criados com base em suas ações, preferências ou informações de perfil para fornecer experiências personalizadas.

* Navegue até Cliente -> Públicos-alvo
* Criar públicos-alvo usando o método de criação de regra

* Crie os três públicos-alvo a seguir no AJO usando o elemento PreferredFinancialInstrument do esquema do evento.

   * Clientes interessados em Ações

   * Clientes interessados em títulos

   * Clientes interessados no CD

Verifique se o método de avaliação de cada público-alvo está definido como Edge para qualificação em tempo real.

As capturas de tela a seguir devem ajudar você a criar os Públicos-alvo.

![público-alvo](assets/rule-based-audience.png)

![evento](assets/event-attribute.png)


![InstrumentoFinanceiroPreferencial](assets/stock-customers.png)

![edge-audience](assets/audience-edge.png)