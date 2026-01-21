---
title: Implementar o limite de frequência em ofertas do Adobe Journey Optimizer (AJO) fornecidas pelo AJO Decisioning
description: Este tutorial estende uma implementação existente do Adobe Journey Optimizer (AJO) habilitando o limite de frequência em ofertas fornecidas com o AJO Decisioning. Ele descreve como capturar eventos de impressão e interação usados no limite de frequência.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00Z
jira: KT-18526
exl-id: ae74485f-9ea1-428d-9c07-5db0c5cf93fb
source-git-commit: bef6d831c639d40514552dae3ff20132626a4a09
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# Implementar o limite de frequência em ofertas do Adobe Journey Optimizer (AJO) fornecidas pelo AJO Decisioning

Este tutorial demonstra como aplicar o limite de frequência a ofertas no Adobe Journey Optimizer para controlar a frequência com que os usuários veem a mesma oferta ao longo do tempo.

Ao capturar eventos decisioning.propositionDisplay e decisioning.propositionInteract por meio do Adobe Web SDK e mapeá-los para esquemas XDM no Adobe Experience Platform (AEP), o Adobe Journey Optimizer pode rastrear com precisão as impressões e interações da oferta, permitindo o limite de frequência para limitar a frequência com que uma oferta é exibida a um usuário.

## Pré-requisitos para este tutorial

Antes de continuar, verifique se você tem uma campanha válida do Adobe Journey Optimizer usando a Decisão que está oferecendo ofertas ativamente em uma superfície da Web.

Este tutorial presume que o delivery de ofertas já está funcionando e se concentra exclusivamente na configuração e validação do comportamento de limite de frequência.


