---
title: Testar a solução
description: Crie uma página da Web simples para testar a personalização de oferta contextual usando dados de temperatura em tempo real.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18258
source-git-commit: a9fc14da78e1c67b01aef5dcdd417ce02d36d50a
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 1%

---

# Testar a solução

Uma página da Web é criada para testar a personalização de oferta contextual usando dados de temperatura em tempo real. Quando um usuário visita a página, o navegador solicita acesso de localização geográfica. Após a aprovação, a página busca os detalhes do tempo atual, como temperatura, condição e cidade, por meio da API OpenWeatherMap. Esses dados contextuais são exibidos para o usuário e enviados para o Adobe Experience Platform usando o Adobe Web SDK (Alloy).

A chamada sendEvent é configurada com renderDecisions: false, o que significa que as ofertas retornadas pela Adobe Journey Optimizer são tratadas manualmente. O script processa a resposta de decisão, decodifica o conteúdo e insere dinamicamente a oferta mais relevante em um container designado (#offerContainer).

## O que a JavaScript faz

O JavaScript busca dinamicamente informações meteorológicas com base na localização do usuário e usa o Adobe Experience Platform (AEP) para fornecer ofertas personalizadas. Veja um detalhamento das etapas:

1. **Espera até que o Alloy carregue**

   O script garante que o Adobe Web SDK (Alloy) esteja totalmente carregado antes de fazer qualquer solicitação de personalização.

2. **Obtém a Localização do Usuário**

   Ele usa a API de geolocalização do navegador para recuperar a latitude e a longitude atuais do usuário.

3. **Obtém Dados Meteorológicos**

   Ele chama a API OpenWeatherMap para obter detalhes do tempo atual:

   Temperatura (em °F)

   Condição do tempo (por exemplo, &quot;Chuva&quot;, &quot;Limpar&quot;)

   Nome da cidade

   Umidade

4. **Exibir Informações Meteorológicas na Página da Web**

   Atualiza o DOM com uma mensagem como:

   &quot;A temperatura atual em San Diego é de 72°F com céu limpo.&quot;

5. **Envia o Contexto de Clima para o AEP**

   Usa alloy(&quot;sendEvent&quot;) para enviar dados meteorológicos contextuais para o AEP

   ```javascript
   xdm: {
   eventType: "decisioning.request",
   _techmarketingdemos: {
   temperature: temp,
   weatherConditions: condition,
   cityName: city
     }
   }
   ```

6. **Recupera e renderiza ofertas**

   Recebe ofertas retornadas pela AJO.

   Decodifica o conteúdo do HTML.

   Injeta dinamicamente as ofertas na variável <div id="offerContainer"> direcionado.

7. **Assets de exemplo**

   A página da Web usada para testar a solução está disponível para download

[Página da Web](assets/weather-offers.html)

[Código JavaScript](assets/weather-related-offers-script.js)

