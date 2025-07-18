---
title: Rastrear e relatar ofertas do Adobe Journey Otimizer (AJO) entregues pelo AJO Offer Decisioning
description: Este tutorial estende uma implementação existente do Adobe Journey Optimizer (AJO) que fornece ofertas personalizadas com base em dados contextuais, como temperatura. Ele descreve como capturar eventos de impressão e interação e preparar os dados para relatórios no Journey Otimizer.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00Z
jira: KT-18526
source-git-commit: fa4795d92cf290b867df23277a297c99d6222224
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# Adicionar tokens de rastreamento aos itens de oferta

Para modificar o código no editor de personalização, siga as etapas:

Navegue até _&#x200B;**Gerenciamento de Jornadas ->Campanhas**&#x200B;_

Abra a campanha apropriada e clique no botão _&#x200B;**Parar campanha**&#x200B;_ para interromper a campanha.

Abra a campanha interrompida e clique no botão _&#x200B;**Modificar campanha**&#x200B;_.

Clique na guia _&#x200B;**Conteúdo**&#x200B;_ e clique no botão _&#x200B;**Editar código**&#x200B;_ para abrir o editor de personalização.

Adicione dois novos atributos de dados ao div, como mostrado na captura de tela
![token de rastreamento](assets/offer-item-with-tracking-code.png)

O trackingToken e o ItemID podem ser adicionados clicando no ícone da política de decisão na navegação à esquerda e detalhando a árvore de decisão para selecionar o itemID e o trackingToken.
![token de rastreamento](assets/insert-tracking-token.png)

Isso garante que cada oferta renderizada inclua um token de rastreamento de dados, essencial para garantir uma impressão precisa e um rastreamento de eventos de cliques.

Salve as alterações e ative a campanha.
