---
title: Personalizar ofertas com fórmulas de classificação com base no CEP e na renda
description: Use fórmulas de classificação do Adobe Journey Optimizer para fornecer dinamicamente as ofertas financeiras mais relevantes, adaptadas para o CEP e o nível de renda de cada usuário, para maior engajamento e uma personalização mais inteligente.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-27T00:00:00.000Z
jira: KT-18188
exl-id: 11685f7c-8048-4318-9c28-71bd7da8f7ff
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
source-wordcount: '338'
ht-degree: 16%
---
# Personalizar ofertas com fórmulas de classificação com base no CEP e na renda do usuário

Este caso de uso demonstra como fornecer ofertas financeiras personalizadas, aproveitando atributos de usuário como código postal e receita anual no Adobe Journey Optimizer. Ao usar fórmulas de classificação, as ofertas são pontuadas e priorizadas de forma inteligente com base em promoções específicas do local e na qualificação com base na renda. Por exemplo, os CD de alto rendimento podem ser promovidos junto dos utilizadores em códigos postais ricos, enquanto as opções de investimento diversificadas são apresentadas aos investidores emergentes. As fórmulas de classificação garantem que cada usuário receba ofertas relevantes e financeiramente apropriadas. Os critérios de classificação são definidos usando atributos de perfil, sinais contextuais e modelos de IA opcionais para melhorar ainda mais a precisão da decisão. As ofertas são fornecidas em tempo real por meio da Web ou de canais de email, aumentando o engajamento e a conversão. Essa abordagem combina lógica de negócios com personalização orientada por dados para elevar a experiência do usuário e o impacto do marketing.

## Pré-requisitos

Este tutorial se baseia nos principais conceitos do Adobe Journey Optimizer e do Adobe Experience Platform. Antes de continuar, verifique se os seguintes pré-requisitos foram atendidos:

* [O Tutorial de Compilação de Identidades](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorial-on-identity-stitching-in-aep/introduction) foi concluído, com as IDs do CRM associadas com êxito às ECIDs no Adobe Experience Platform.

* Familiarize-se com a criação de Itens de oferta no AJO, incluindo definição de conteúdo, configuração de metadados e regras de qualificação.

* Familiarizar-se com a configuração de canais (como Web ou email) para entrega de ofertas.

* Familiarizar-se com a criação e a ativação de campanhas no AJO.

* Familiarize-se com o uso do Adobe Launch (tags) para implantar a Web SDK e enviar eventos que contêm dados de identidade e perfil.

Este tutorial aborda as próximas etapas do Offer Decisioning:

* Criar um método de classificação usando atributos de perfil, como código postal e renda anual.

* Definir uma estratégia de seleção para agrupar e priorizar ofertas.

* Criar uma política de decisão para fornecer a oferta mais relevante para cada indivíduo.
