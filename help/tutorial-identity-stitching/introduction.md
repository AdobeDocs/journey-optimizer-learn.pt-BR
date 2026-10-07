---
title: Configuração de identidade no AEP
description: Estabeleça a compilação de identidade entre um usuário conhecido (CRMID) e um visitante anônimo da web (ECID), permitindo perfis unificados para personalização em tempo real e a definição de ofertas no Adobe Journey Optimizer (AJO).
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00.000Z
jira: KT-18089
exl-id: d6a1201a-3779-4718-8ea8-b88f925f53b6
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d2971708-e780-44bb-9e2a-72f139796afd
    internal-label: Customer
subfeature_v2:
  - id: ef9a83ca-eefa-47cf-aa34-f1a34715583a
    internal-label: Profiles
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 11%
---
# Compilação de identidade no AEP

Em experiências modernas do cliente, é essencial unificar as identidades do usuário em dispositivos e canais. Esse caso de uso demonstra como implementar a compilação de identidades no Adobe Experience Platform (AEP) vinculando uma ID do CRM conhecida, capturada durante o logon do usuário, à Experience Cloud ID (ECID) anônima gerada pela Adobe Web SDK. Ao unir essas identidades em tempo real, o AEP pode criar um perfil do cliente mais completo que abrange tanto o comportamento anônimo quanto os dados autenticados. Isso permite uma segmentação, personalização e decisão do público-alvo mais precisas em ferramentas como o Adobe Journey Optimizer (AJO).

## Habilidades necessárias para o tutorial de compilação de identidade

Para aproveitar este tutorial, é recomendável estar familiarizado com o seguinte:

- **Conceitos Principais Do Adobe Experience Platform (AEP)**\
  Noções básicas sobre esquemas, conjuntos de dados, identidades, políticas de mesclagem e perfis em tempo real.

- **Modelagem de Esquema e Identidade**\
  Capacidade de configurar campos de identidade em esquemas baseados em perfis e eventos.

- **Adobe Launch (Marcas) e Web SDK (Alloy.js)**\
  Experiência em configurar elementos de dados e regras para enviar dados ao AEP usando a Web SDK.

- **Noções básicas sobre o JavaScript**\
  Familiarizado trabalhando com funções para capturar entradas de usuário, eventos de acionador e chamadas de API de depuração.

- **Ferramentas de depuração do AEP**\
  Capacidade de usar o AEP Debugger e o Visualizador de gráfico de identidade para validar a compilação de identidade.

- **Assimilação de dados no AEP**\
  Familiaridade com upload de dados de amostra para conjuntos de dados e garantia da qualidade dos dados.


