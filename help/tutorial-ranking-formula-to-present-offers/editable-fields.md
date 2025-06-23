---
title: Utilização de campos de formulário editáveis em experiências baseadas em código do AJO
description: Saiba como criar blocos de conteúdo editáveis usando campos de formulário em linha nos modelos de experiência baseada em código do Adobe Journey Optimizer para potencializar os profissionais de marketing com conteúdo de campanha dinâmico e reutilizável.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-22T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18416
source-git-commit: b9feb65fb7af8fb495f81841ab9235e4ae80ecd7
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---

# Utilização de campos de formulário editáveis em experiências baseadas em código do AJO

Em muitas jornadas de marketing, particularmente em setores regulamentados, é essencial incluir um aviso de isenção legal que pode variar dependendo da campanha, da geografia ou do produto. Ao usar um [campo editável](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/channels/code-based-experience-channel/form-fields-in-code-based-experiences) diretamente no Editor do Personalization do AJO, os profissionais de marketing e as equipes jurídicas podem manter o controle total sobre o texto do aviso de isenção de responsabilidade sem envolver desenvolvedores ou modificar a lógica de decisão.

Isso permite atualizações rápidas e garante a conformidade em todas as campanhas, ao mesmo tempo que aproveita o conteúdo decidido, como ofertas.

## Inserir campo editável no editor de personalização

- Abra a campanha criada na etapa anterior.
- Clique em _**Modificar campanha**_
- Navegue até a guia _**Conteúdo**_
- Clique em _**Editar código**_ e insira um campo editável chamado legalDisclaimer com um valor padrão usando a seguinte sintaxe no editor de personalização

- 
  <pre> {{#inline "legalDisclaimer" name="Legal Disclaimer"}} Aviso de isenção de responsabilidade legal aqui {{/inline}}  </pre>

- Usar o <code>{{{legalDisclaimer}}}</code> no modelo, conforme mostrado abaixo

- ![campos-editáveis](assets/editable-fields.png)

- Os profissionais de marketing podem editar facilmente o campo Legal Disclaimer (Aviso de isenção de responsabilidade) sem precisar abrir o editor de personalização.
- ![comerciante-de-campo-editável](assets/editable-field-marketer-view.png)



## Publicar a campanha

Ative a campanha para começar a fornecer ofertas personalizadas em tempo real.

