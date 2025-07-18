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
exl-id: 609a5ddf-d6c6-4f19-bd7f-bca8c266b759
source-git-commit: 23832f2e59ca7558fd403f0a9753db3923023e6d
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Testar a solução

Para testar a solução de ponta a ponta, os arquivos [weather-offers.html](assets/weather-offers.html) e [weather-related-offers-script.js](assets/weather-related-offers-script.js) devem ser hospedados em um servidor Web ou em um serviço de hospedagem público, como o Github Pages. Isso é necessário porque:
- A API de geolocalização do navegador funciona somente em HTTPS ou localhost

Para manter as coisas organizadas e garantir que caminhos relativos funcionem corretamente, recomendamos a seguinte estrutura de pastas para hospedar a solução:

![estrutura-pasta](assets/folder-structure.png)

## Baixar os arquivos fornecidos

[Arquivo HTML](assets/weather-offers.html)

[Arquivo Javascript](assets/weather-related-offers-script.js)


## Atualizar o url da superfície no arquivo javascript

Abra o `weather-related-offers-script.js` e atualize o ` "web://yourdomain.com/weather/weather-offers.html#offerContainer"`bt substituindo o `yourdomain.com` pelo domínio real onde o arquivo do HTML está hospedado.

## Atualizar a propriedade Tags do Adobe Experience Platform

Abra o arquivo weather-offers.html no editor de texto e substitua a tag script pela tag script da Propriedade de tag Adobe Experience Platform criada na etapa anterior deste tutorial. Certifique-se de salvar o arquivo

```
<script src="https://assets.adobedtm.com/AEM_TAGS/launch-ENabcd1234.min.js" async></script>
```



## O que a página da Web faz

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

