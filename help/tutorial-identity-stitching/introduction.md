---
title: Compilação de identidade no AEP
description: Estabeleça a identificação de identidade entre um usuário conhecido (CRMID) e um visitante anônimo da Web (ECID), permitindo perfis unificados para personalização em tempo real e o Offer Decisioning no Adobe Journey Optimizer (AJO).
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
jira: KT-18089
source-git-commit: 502cdc41b666959141ff4dfc63608cc463009811
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# Descrição do caso de uso

Em experiências modernas do cliente, é essencial unificar as identidades do usuário em dispositivos e canais. Esse caso de uso demonstra como implementar a compilação de identidades no Adobe Experience Platform (AEP) vinculando uma ID do CRM conhecida, capturada durante o logon do usuário, à Experience Cloud ID anônima (ECID) gerada pela Adobe Web SDK. Ao unir essas identidades em tempo real, o AEP pode criar um perfil do cliente mais completo que abrange tanto o comportamento anônimo quanto os dados autenticados. Isso permite uma segmentação, personalização e decisão do público-alvo mais precisas em ferramentas como o Adobe Journey Optimizer (AJO).

