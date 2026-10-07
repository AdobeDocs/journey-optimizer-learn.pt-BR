---
title: Criar uma política de decisão
description: Use uma política de decisão para definir a lógica para determinar quais ofertas são entregues a um usuário durante a personalização.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-17728
exl-id: 186e4a7d-6077-401f-9958-2f955214bc35
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: a984631b-2bae-4860-9b15-69c41a799dcb
    internal-label: APIs and SDKs
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
    internal-label: Decisioning API
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%
---
# Criar uma política de decisão

As políticas de decisão são containers para suas ofertas que aproveitam o mecanismo de [!UICONTROL Decisão] para escolher o melhor conteúdo a ser entregue, dependendo do público.

1. No editor de personalização, clique no item **[!UICONTROL Política de decisão]** na navegação à esquerda e clique em **[!UICONTROL Adicionar política de decisão]**.

   ![criar-política-decisão](assets/decision-policy.png)

1. Clique em **[!UICONTROL Adicionar]** para selecionar a estratégia de seleção.

   ![política-decisão](assets/decision-policy2.png)

1. Clique em **[!UICONTROL Selecionar fallback]** para selecionar a oferta de fallback.
1. Clique em **[!UICONTROL Avançar]** para examinar a política de decisão.
1. Clique em **[!UICONTROL Criar]** para concluir o processo de criação da política de decisão.

## Usar a política de decisão no editor de código

1. No editor de personalização, clique em **[!UICONTROL Inserir política]**.

   O código correspondente à política de decisão é adicionado.

   Nesse estágio, você pode incluir quaisquer atributos de decisão necessários diretamente no código. Esses atributos são definidos no schema usado pelo catálogo Ofertas. Os atributos padrão são organizados no namespace `__experience`, enquanto os atributos personalizados específicos da sua organização são armazenados no namespace `_<imsOrg>`.

   ![using_decision_policy](assets/Insert-policy.png)

   Esse código passa por uma lista de ofertas personalizadas escolhidas para o usuário e exibe o texto de cada uma na página da Web. Ele mostra a mensagem (chamada `offerText`) de cada oferta dentro de um parágrafo, para que os usuários possam ver seu conteúdo personalizado com clareza.

   Se nenhuma oferta personalizada estiver disponível, uma oferta substituta será exibida para garantir que o espaço não seja deixado em branco.

1. Clique em **[!UICONTROL Salvar]** e ative a campanha.
