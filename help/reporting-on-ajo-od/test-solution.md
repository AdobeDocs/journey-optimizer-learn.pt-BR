---
title: Testar a solução
description: Crie uma página da Web simples para capturar eventos de impressão e clique nas ofertas.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-07-18T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18526
source-git-commit: 69bc8aace3cc502a18e691584824176833413c7e
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# Testar a solução

Para testar a solução de ponta a ponta, os arquivos [weather-offers.html](assets/weather-offers.html) e [capture-impressions-click-events.js](assets/capture-impressions-click-events.js) devem ser hospedados em um servidor Web ou em um serviço de hospedagem público, como o Github Pages. Isso é necessário porque a API de geolocalização do navegador só funciona por HTTPS ou localhost

## Baixar os arquivos fornecidos

[Arquivo HTML](assets/weather-offers.html)

[Arquivo Javascript](assets/capture-impressions-click-events.js)

## Atualizar o url da superfície no arquivo javascript

Abra o `capture-impressions-click-events.js` e atualize o ` "web://yourdomain.com/weather/weather-offers.html#offerContainer"` substituindo `yourdomain.com` pelo domínio real onde o arquivo do HTML está hospedado.


## Atualizar a propriedade Tags do Adobe Experience Platform

Abra o arquivo weather-offers.html no editor de texto e substitua a tag script pela tag script da Propriedade de tag Adobe Experience Platform criada na etapa anterior deste tutorial. Certifique-se de salvar o arquivo

```
<script src="https://assets.adobedtm.com/AEM_TAGS/launch-ENabcd1234.min.js" async></script>
```

## Interagir com as ofertas

- Abra a página da Web em seu navegador favorito.

- Permitir _&#x200B;**rastreamento de localização**&#x200B;_. Isso é necessário para obter os detalhes meteorológicos com base em sua localização.

- Clique no botão nas ofertas para acionar o evento de interação.

## Exibir o relatório

- Fazer logon no Journey Optimizer

- Navegue até Gerenciamento de Jornadas ->Campanhas

- Clique na campanha e selecione o relatório apropriado no menu de relatório.
