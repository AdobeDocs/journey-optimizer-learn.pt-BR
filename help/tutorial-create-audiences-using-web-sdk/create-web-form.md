---
title: Criar um formulário web
description: Crie um formulário na página do HTML que permita aos usuários selecionar sua preferência de investimento
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-17923
exl-id: 20de8dec-aac8-43ed-8305-e723f82a5dd9
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d2971708-e780-44bb-9e2a-72f139796afd
    internal-label: Customer
subfeature_v2:
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%
---
# Criar um formulário web

O formulário do HTML a seguir foi criado para capturar a preferência dos usuários
![formulário-html](assets/web-form.png)

Quando um usuário clica no botão na página da Web, sua preferência financeira selecionada (como Ações, Títulos ou CDs) é capturada e enviada para a Camada de dados da Adobe. Esse evento (assetClassSelection) armazena a escolha do usuário em tempo real. O Adobe Launch ouve esse evento, recupera a opção de investimento selecionada (PreferredFinancialInstrument) e pode acionar ações como enviar os dados para o Adobe Experience Platform (AEP) ou atualizar as regras de personalização

A seguinte JavaScript foi escrita para lidar com o envio do formulário

```javascript
function handleSubmission() {
  window.adobeDataLayer = window.adobeDataLayer || [];

  const selectedAssetClass = document.querySelector('input[name="assetclass"]:checked');
  const errorMessage = document.getElementById("error-message");
  const messageBox = document.getElementById("message");

  if (!selectedAssetClass) {
    errorMessage.textContent = "Please select a financial instrument.";
    messageBox.textContent = "";
    return;
  }

  errorMessage.textContent = "";

  const subscriptionEvent = {
    event: "assetClassSelection",
    xdm: {
      eventType: "assetClassSelection",
      eventID: "investment_preference_event",
      timestamp: new Date().toISOString(),
      FinancialInterest: {
        PreferredFinancialInstrument: selectedAssetClass.value
      }
    }
  };

  console.log("📩 Sending asset class data to AEP:", subscriptionEvent);
  window.adobeDataLayer.push(subscriptionEvent);

  // ✅ Show thank-you message
  messageBox.textContent = `Thank you for selecting "${selectedAssetClass.value}". We'll use this to personalize your experience.`;
}
```

[A amostra do formulário do HTML é fornecida como parte deste tutorial](assets/webform.zip)
