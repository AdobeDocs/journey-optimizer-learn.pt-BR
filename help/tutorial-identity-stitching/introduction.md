---
title: Configuração de identidade no AEP
description: Estabeleça a identificação de identidade entre um usuário conhecido (CRMID) e um visitante anônimo da Web (ECID), permitindo perfis unificados para personalização em tempo real e o Offer Decisioning no Adobe Journey Optimizer (AJO).
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
jira: KT-18089
exl-id: d6a1201a-3779-4718-8ea8-b88f925f53b6
source-git-commit: f3aeb66ca67448e7751ab2cd6d0bb6ce38f73530
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# Compilação de identidade no AEP

Em experiências modernas do cliente, é essencial unificar as identidades do usuário em dispositivos e canais. Esse caso de uso demonstra como implementar a compilação de identidades no Adobe Experience Platform (AEP) vinculando uma ID do CRM conhecida, capturada durante o logon do usuário, à Experience Cloud ID anônima (ECID) gerada pela Adobe Web SDK. Ao unir essas identidades em tempo real, o AEP pode criar um perfil do cliente mais completo que abrange tanto o comportamento anônimo quanto os dados autenticados. Isso permite uma segmentação, personalização e decisão do público-alvo mais precisas em ferramentas como o Adobe Journey Optimizer (AJO).

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


