---
title: Personalização de ofertas com fórmulas de Classificação com base no CEP e na renda do usuário
description: Use as fórmulas de classificação da Adobe Journey Optimizer para fornecer dinamicamente as ofertas financeiras mais relevantes, adaptadas ao CEP e nível de renda de cada usuário, visando maior engajamento e personalização mais inteligente.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-27T00:00:00Z
jira: KT-18188
source-git-commit: 58d2964644bc199b9db212040676d87d54f767b9
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Personalização de ofertas com fórmulas de Classificação com base no CEP e na renda do usuário

Este caso de uso demonstra como fornecer ofertas financeiras personalizadas, aproveitando atributos de usuário como código postal e receita anual no Adobe Journey Optimizer. Ao usar fórmulas de classificação, as ofertas são pontuadas e priorizadas de forma inteligente com base em promoções específicas do local e na qualificação com base na renda. Por exemplo, os CD de alto rendimento podem ser promovidos junto dos utilizadores em códigos postais ricos, enquanto as opções de investimento diversificadas são apresentadas aos investidores emergentes. As fórmulas de classificação garantem que cada usuário receba ofertas relevantes e financeiramente apropriadas. Os critérios de classificação são definidos usando atributos de perfil, sinais contextuais e modelos de IA opcionais para melhorar ainda mais a precisão da decisão. As ofertas são fornecidas em tempo real por meio da Web ou de canais de email, aumentando o engajamento e a conversão. Essa abordagem combina lógica de negócios com personalização orientada por dados para elevar a experiência do usuário e o impacto do marketing.

## Pré-requisitos

Este tutorial se baseia nos principais conceitos do Adobe Journey Optimizer e do Adobe Experience Platform. Antes de continuar, verifique se os seguintes pré-requisitos foram atendidos:

* [O Tutorial de Compilação de Identidades](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorial-on-identity-stitching-in-aep/introduction) foi concluído, com as IDs do CRM associadas com êxito às ECIDs no Adobe Experience Platform.

* Familiarize-se com a criação de Itens de oferta no AJO, incluindo definição de conteúdo, configuração de metadados e regras de qualificação.

* Familiarizar-se com a configuração de canais (como Web ou email) para entrega de ofertas.

* Familiarizar-se com a criação e a ativação de campanhas no AJO.

* Familiarize-se com o uso do Adobe Launch (tags) para implantar a Web SDK e enviar eventos que contêm dados de identidade e perfil.

Este tutorial aborda as próximas etapas do Offer Decisioning:

* Criar um método de classificação usando atributos de perfil, como código postal e renda anual.

* Definir uma estratégia de seleção para agrupar e priorizar ofertas.

* Criar uma política de decisão para fornecer a oferta mais relevante para cada indivíduo.


