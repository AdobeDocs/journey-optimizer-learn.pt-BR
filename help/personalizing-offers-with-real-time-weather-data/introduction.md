---
title: Personalização de ofertas com dados meteorológicos em tempo real no Adobe Journey Optimizer usando o SDK da web
description: Este tutorial demonstra como entregar ofertas dinâmicas e baseadas no clima no Adobe Journey Optimizer usando dados contextuais em tempo real e a API de personalização do SDK da web da Adobe. Você aprenderá a transmitir atributos de clima (como temperatura e condições) do seu site para a Adobe Experience Platform, mapeá-los para o esquema do evento e usá-los em regras de decisão e fórmulas de classificação para personalizar ofertas no momento do carregamento da página. Ideal para profissionais de marketing e desenvolvedores que buscam aprimorar experiências digitais com contexto ambiental em tempo real.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00.000Z
jira: KT-18258
exl-id: f40dd541-470c-4f42-8181-eb1c277ebaa3
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
source-wordcount: '230'
ht-degree: 42%
---
# Descrição do caso de uso

Usar dados relacionados ao clima no Adobe Journey Optimizer (AJO) para atender ofertas permite que as empresas personalizem as experiências do cliente com base em condições ambientais em tempo real. O tempo é um poderoso sinal contextual. As necessidades e o comportamento das pessoas mudam de acordo com o tempo. Usando dados meteorológicos:

Fornecer ofertas relevantes que se alinhem ao humor e ao ambiente do cliente

Em um dia quente, mostre uma oferta de bebidas frias ou unidades AC. Em um dia chuvoso, promova jaquetas ou guarda-chuva

Exemplo de uma oferta baseada no clima


![ofertas meteorológicas](assets/offers-use-case.png)



## Pré-requisitos para este tutorial

* Acesso ao Experience Platform.

* Conhecimento básico das Tags do Adobe Experience Platform.

* Conhecimento básico dos conceitos do Experience Platform (perfis, públicos-alvo, conjuntos de dados).

* Familiaridade com o Journey Optimizer.

* Conhecimento básico do JavaScript (ler e escrever funções simples).

* Capacidade de usar as DevTools do navegador (guias Console e Rede).
