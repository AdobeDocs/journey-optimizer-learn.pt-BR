---
title: Criar uma página da Web para testar a solução
description: Página da Web para testar as ofertas personalizadas entregues usando a decisão.
role: User
level: Beginner
doc-type: Tutorial
feature: Decisioning
last-substantial-update: 2025-05-05T00:00:00Z
jira: KT-17728
exl-id: 72a67137-303d-4dfe-9b70-322c81e5fb27
source-git-commit: 2ca9ffee1a2326b8ae55a8e8de496a632fea79c8
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Criar uma página da Web para testar a solução

Essa página da Web foi criada para testar ofertas personalizadas entregues pelo Adobe Journey Optimizer Decisioning. Ele fornece um ambiente controlado em que a chamada sendEvent pode ser acionada e o conteúdo de oferta retornado renderizado, ajudando a validar a configuração de personalização completa e a garantir que a decisão funcione conforme esperado.

O script a seguir é responsável por buscar e exibir uma oferta personalizada em uma página da Web usando o Adobe Journey Optimizer.

1. Decodificar entidades do HTML: há uma função auxiliar que converte com segurança qualquer caractere especial no conteúdo da oferta em um HTML legível.

2. Executar personalização:
Quando chamado, ele envia uma solicitação (sendEvent) para o Adobe Web SDK a fim de obter conteúdo personalizado para uma área específica na página (o elemento #ajo-offer).
Se uma oferta for retornada, ela decodifica a HTML e a insere na página.
Se nada for retornado, ele registrará um aviso.

3. Aguarde a SDK:
Como o SDK (liga) do Adobe é carregado de forma assíncrona, o script aguarda até que seja totalmente carregado antes de fazer a solicitação.
Ele verifica se há liga a cada 200 milissegundos, até 20 vezes, para evitar erros.

4. No carregamento da página: quando a página termina o carregamento, o script inicia o processo chamando waitForAlloy().



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
        renderDecisions: true,
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
