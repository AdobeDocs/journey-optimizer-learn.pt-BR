---
title: Personalização de ofertas com dados meteorológicos em tempo real no Adobe Journey Optimizer usando o Web SDK
description: Este tutorial demonstra como fornecer ofertas dinâmicas e com reconhecimento de clima no Adobe Journey Optimizer usando dados contextuais em tempo real e a API do Personalization do Adobe Web SDK. Você aprenderá a transmitir atributos de clima (como temperatura e condições) do seu site para o Adobe Experience Platform, mapeá-los para o esquema do evento e usá-los em regras de decisão e fórmulas de classificação para personalizar ofertas no momento do carregamento da página. Ideal para profissionais de marketing e desenvolvedores que buscam aprimorar experiências digitais com contexto ambiental em tempo real.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00Z
jira: KT-18258
source-git-commit: c04a15418e31dc82597b7759386907013728bb0d
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Descrição do caso de uso

Usar dados relacionados ao clima no Adobe Journey Optimizer (AJO) para atender ofertas permite que as empresas personalizem as experiências do cliente com base em condições ambientais em tempo real. O tempo é um poderoso sinal contextual. As necessidades e o comportamento das pessoas mudam de acordo com o tempo. Usando dados meteorológicos:

Fornecer ofertas relevantes que se alinhem ao humor e ao ambiente do cliente

Em um dia quente, mostre uma oferta de bebidas frias ou unidades AC. Em um dia chuvoso, promova jaquetas ou guarda-chuva

Exemplo de uma oferta baseada no clima


![ofertas meteorológicas](assets/offers-use-case.png)



## Pré-requisitos para este tutorial

* Acesso ao Experience Platform

* Noções básicas sobre tags do Adobe Experience Platform

* Noções básicas sobre conceitos do Experience Platform (Perfis, Públicos-alvo, Conjuntos de dados)

* Familiaridade com o Journey Optimizer

* Conhecimento básico do JavaScript (ler e escrever funções simples)

* Capacidade de usar as DevTools do navegador (guias Console e Rede)
