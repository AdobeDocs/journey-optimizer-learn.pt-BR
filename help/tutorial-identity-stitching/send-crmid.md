---
title: Crie o aplicativo de amostra para simular a atividade de logon
description: Criar um aplicativo Node.js de exemplo para simular um fluxo de logon
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-18089
exl-id: e080149c-0ac0-4559-b99d-ebad9f03b98b
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d2971708-e780-44bb-9e2a-72f139796afd
    internal-label: Customer
subfeature_v2:
  - id: ef9a83ca-eefa-47cf-aa34-f1a34715583a
    internal-label: Profiles
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%
---
# Crie o aplicativo de amostra para simular a atividade de logon

Este aplicativo de amostra, criado e implantado em um servidor Node.js, demonstra como enviar uma ID do CRM para o Adobe Experience Platform (AEP) quando um usuário faz logon. O aplicativo simula um fluxo de logon em que as credenciais do usuário são validadas no lado do servidor. Após o logon bem-sucedido, a ID do CRM do usuário é recuperada e enviada para a adobeDataLayer, acionando uma regra correspondente nas Tags do Adobe Experience Platform (antigo Adobe Launch).

A função attachLoginHandler anexa um ouvinte de eventos de envio a um formulário de logon. No envio do formulário, impede a ação padrão, valida as credenciais em relação ao objeto de um usuário predefinido e recupera a ID do CRM, se válida. A função envia um evento userloggedin com a ID do CRM e o estado de autenticação para a adobeDataLayer, e as tags da Adobe Experience Platform a selecionam para enviar os dados para a Adobe Experience Platform (AEP).


```javascript
function attachLoginHandler() {
    const form = document.getElementById("loginForm");
    if (!form) return;

    form.addEventListener("submit", function(e) {
        e.preventDefault();
        const username = document.getElementById("username").value;
        const password = document.getElementById("password").value;

        if (users[username] && users[username].password === password) {
            const crmid = users[username].crmid;
            window.adobeDataLayer = window.adobeDataLayer || [];
            debugger;
            window.adobeDataLayer.push({
                event: "UserLoggedIn",
                user: {
                    crmid: crmid,
                    authenticatedState: "authenticated"
                }
            });
        }
    });
}
```

O script de tags da Adobe Experience Platform está incluído na Seção `<head>` da página do HTML usando uma tag `<script>`, geralmente da seguinte maneira:

`<script src="https://assets.adobedtm.com/b5eu4857867/4e4d84957/launch-b69e276bb9b5-development.min.js" async crossorigin="anonymous"></script>`

O script de tags do AEP foi obtido ao publicar uma propriedade ativada para o Web SDK criada na etapa anterior e copiando o código incorporado da guia Ambientes.
