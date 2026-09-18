---
title: Criação de públicos no Adobe Journey Optimizer
description: Saiba como definir e criar públicos-alvo direcionados no AJO para potencializar jornadas personalizadas e decisões em tempo real do cliente
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30
jira: KT-17923
exl-id: d90f1868-0514-49b2-832d-82460883b6e4
source-git-commit: 073d4a99b74a0bc341117e83a66747aed02648bf
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%
---
# Criação de públicos no Adobe Journey Optimizer


Os públicos-alvo no Adobe Experience Platform são grupos de usuários criados com base em suas ações, preferências ou informações de perfil para fornecer experiências personalizadas.

* Fazer logon no Journey Optimizer
* Navegue até Cliente -> Públicos-alvo ->Criar público-alvo
* Criar públicos-alvo usando o método de criação de regra

  ![público-alvo](assets/rule-based-audience.png)

* Crie os 3 públicos a seguir

  * Clientes interessados em Ações

  * Clientes interessados em títulos

  * Clientes interessados no CD


* Verifique se o método de avaliação de cada público-alvo está definido como _**Edge**_ para qualificação em tempo real.
  ![edge-audience](assets/audience-edge.png)

* Use o campo PreferredFinancialInstrument para segmentar os usuários com base em seus interesses de investimento selecionados, como Ações, Títulos ou CDs

![evento](assets/event-attribute.png)

![InstrumentoFinanceiroPreferencial](assets/stock-customers.png)




>[!NOTE]
>
>>Se o campo PreferredFinancialInstrument não estiver visível na guia events, clique no ícone settings e alterne o esquema XDM completo.



![alternar-esquema-xdm-completo](assets/show-custom-fields.png)
