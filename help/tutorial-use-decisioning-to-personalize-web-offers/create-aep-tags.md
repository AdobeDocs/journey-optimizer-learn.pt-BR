---
title: Criar tags do Adobe Experience Platform
description: Criação de públicos da AJO com base nas preferências de investimento do usuário (ações, títulos, CDs)
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-17923
exl-id: 6823ce13-bc77-4e2b-89e0-606e403c15f2
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
source-wordcount: '291'
ht-degree: 0%
---
# Criar tags do Adobe Experience Platform

As tags do Experience Platform são configuradas na página da Web para carregar o Adobe Experience Platform Web SDK, permitindo que a chamada da API sendEvent acione experiências personalizadas. Essa configuração garante que as bibliotecas do lado do cliente necessárias sejam inicializadas corretamente, permitindo a interação em tempo real com a Adobe Journey Optimizer para a entrega de ofertas.

1. Faça logon em Coleção de dados.
1. Clique em **[!UICONTROL Marcas]** > **[!UICONTROL Nova Propriedade]**.
1. Crie uma tag Adobe Experience Platform chamada ECID Service.
1. Adicione as seguintes extensões à tag:

   ![extensões-tags](assets/ecid-tag.png)

1. Configure o Adobe Experience Platform Web SDK para usar o ambiente correto e o DataStream dos consultores financeiros criados no tutorial anterior

   ![web-sdk-configuration](assets/web-sdk-configuration.png)

Nenhuma configuração adicional é necessária para a Camada de dados de clientes Adobe e as extensões principais

## Criar o elemento de dados

O elemento de dados da ECID nas tags do Experience Platform é criado apenas para fins de depuração e teste. O elemento de dados permite aos desenvolvedores visualizar a Experience Cloud ID atribuída à sessão do navegador de um usuário, o que pode ajudar a validar a identificação e garantir que as chamadas do `sendEvent` sejam associadas ao perfil correto. Esse elemento não é necessário para que a personalização funcione, mas é útil durante a implementação e o QA

![ecid](assets/ecid-data-element.png)


## Incluir tags do AEP na página do HTML

Crie e publique as Tags do Adobe Experience Platform.

Quando uma propriedade de Tags do AEP é publicada, o Adobe fornece uma tag de script que você deve colocar dentro da HTML `<head>` ou na parte inferior das tags `<body>`.

1. Vá para a propriedade Tags (ECID Service).

1. Clique em Ambientes e, em seguida, clique no ícone de instalação do ambiente desejado (por exemplo, Desenvolvimento, Armazenamento temporário, Produção).

1. Observe o código incorporado.

   Este código precisa ser colocado antes da tag `</body>` de fechamento na página do HTML.
