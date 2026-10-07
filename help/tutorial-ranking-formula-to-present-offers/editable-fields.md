---
title: Utilização de campos de formulário editáveis em experiências baseadas em código do AJO
description: Saiba como criar blocos de conteúdo editáveis usando campos de formulário em linha nos modelos de experiência baseada em código do Adobe Journey Optimizer para impulsionar os profissionais de marketing com conteúdo de campanha dinâmico e reutilizável.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-22T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-18416
exl-id: 0ba695d6-becb-440d-b0d0-de5b51b42562
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
source-wordcount: '221'
ht-degree: 22%
---
# Utilização de campos de formulário editáveis em experiências baseadas em código do AJO

Em muitas jornadas de marketing, particularmente em setores regulamentados, é essencial incluir um aviso de isenção legal que pode variar dependendo da campanha, da geografia ou do produto. Ao usar um [campo editável](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/tutorials/channels/code-based-experience-channel/form-fields-in-code-based-experiences) diretamente no Editor do Personalization do AJO, os profissionais de marketing e as equipes jurídicas podem manter o controle total sobre o texto do aviso de isenção de responsabilidade sem envolver desenvolvedores ou modificar a lógica de decisão.

Isso permite atualizações rápidas e garante a conformidade em todas as campanhas, ao mesmo tempo que aproveita o conteúdo decidido, como ofertas.

## Inserir campo editável no editor de personalização

- Abra a campanha criada na etapa anterior.
- Clique em _**Modificar campanha**_
- Navegue até a guia _**Conteúdo**_
- Clique em _**Editar código**_ e insira um campo editável chamado legalDisclaimer com um valor padrão usando a seguinte sintaxe no editor de personalização

- `{{#inline "legalDisclaimer" name="Legal Disclaimer"}} Legal Disclaimer will go here {{/inline}}`

- Use a variável `{{{legalDisclaimer}}}` no modelo como mostrado abaixo

- ![campos-editáveis](assets/editable-fields.png)

- Os profissionais de marketing podem editar facilmente o campo Legal Disclaimer (Aviso de isenção de responsabilidade) sem precisar abrir o editor de personalização.
- ![comerciante-de-campo-editável](assets/editable-field-marketer-view.png)



## Publicar a campanha

Ative a campanha para começar a fornecer ofertas personalizadas em tempo real.
