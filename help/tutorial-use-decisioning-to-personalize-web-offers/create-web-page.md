---
title: Criar uma página da Web para testar a solução
description: Página da Web para testar as ofertas personalizadas entregues usando a decisão.
role: User
level: Beginner
doc-type: Tutorial
feature: Decisioning
last-substantial-update: 2025-05-05T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-17728
exl-id: 72a67137-303d-4dfe-9b70-322c81e5fb27
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
source-wordcount: '223'
ht-degree: 0%
---
# Criar uma página da Web para testar a solução

Essa página da Web foi criada para testar ofertas personalizadas entregues pelo Adobe Journey Optimizer Decisioning. Ele fornece um ambiente controlado em que a chamada sendEvent pode ser acionada e o conteúdo de oferta retornado renderizado, ajudando a validar a configuração de personalização completa e a garantir que a decisão funcione conforme esperado.

O script a seguir é responsável por buscar e exibir uma oferta personalizada em uma página da Web usando o Adobe Journey Optimizer.

1. Decodificar entidades do HTML:

   Há uma função auxiliar que converte com segurança qualquer caractere especial no conteúdo da oferta em um HTML legível.

1. Executar personalização:

   Quando chamado, ele envia uma solicitação (`sendEvent`) ao Web SDK do Adobe para obter conteúdo personalizado para uma área específica na página (o elemento `#ajo-offer`).

   Se uma oferta for retornada, ela decodifica a HTML e a insere na página.

   Se nada for retornado, ele registrará um aviso.

1. Aguarde a SDK:

   Como o SDK (liga) do Adobe é carregado de forma assíncrona, o script aguarda até que seja totalmente carregado antes de fazer a solicitação.

   Ele verifica se há liga a cada 200 milissegundos, até 20 vezes, para evitar erros.

1. No carregamento da página:

   Quando a página terminar de carregar, o script iniciará o processo chamando `waitForAlloy()`.



```javascript
< script >
    function decodeHtmlEntities(html) {
        const txt = document.createElement("textarea");
        txt.innerHTML = html;
        return txt.value;
    }


function runPersonalization() {
    console.log("🚀 Sending personalization request to AJO...");
    alloy("sendEvent", {
        renderDecisions: false,
        personalization: {
            surfaces: ["#ajo-offer"]
        }
    }).then(result => {
        console.log("🔍 Web SDK decision response:", result);

        const decision = result.propositions?.[0];
        const html = decision?.items?.[0]?.data?.content;

        const container = document.getElementById("ajo-offer");
        if (html && container) {
            const decodedHtml = decodeHtmlEntities(html);
            console.log("✅ Offer HTML content (decoded):", decodedHtml);
            container.innerHTML = decodedHtml;
        } else {
            console.warn("⚠️ No personalized offer returned.");
        }


    }).catch(error => {
        console.error("❌ sendEvent failed:", error);
    });
}

function waitForAlloy(callback, retries = 20) {
    if (typeof alloy === "function") {
        callback();
    } else if (retries > 0) {
        console.log("⌛ Waiting for Alloy...");
        setTimeout(() => waitForAlloy(callback, retries - 1), 200);
    } else {
        console.error("❌ alloy is not loaded after waiting.");
    }
}

// Trigger initial personalization on page load
document.addEventListener("DOMContentLoaded", function() {
    waitForAlloy(() => runPersonalization());
}); <
/script>
```

[A página de exemplo do HTML e os ativos relacionados podem ser baixados aqui](assets/web-page-assets.zip)
