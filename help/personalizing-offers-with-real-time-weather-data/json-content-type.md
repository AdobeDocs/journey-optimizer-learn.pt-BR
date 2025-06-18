---
title: Entrega do Personalization com conteúdo JSON no Adobe Journey Optimizer
description: Aproveite o tipo de conteúdo JSON no Adobe Journey Optimizer (AJO) para criar experiências de personalização flexíveis e orientadas por dados.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-18T00:00:00Z
jira: KT-18387
recommendations: noDisplay, noCatalog
source-git-commit: 9f5b52063605832a9b00c05fb1a93bf60ec7686f
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Entrega do Personalization com conteúdo JSON no Adobe Journey Optimizer

Esta seção é fornecida como um recurso adicional para usuários avançados que desejam maior controle sobre como as ofertas são renderizadas no front-end.

O uso do tipo de conteúdo JSON em uma experiência baseada em código (CBE) permite retornar dados de oferta estruturados e manipular a renderização dinamicamente usando o JavaScript. O tipo de conteúdo JSON é particularmente útil para cenários que exigem layouts personalizados, lógica condicional ou integração com dados contextuais, como clima, localização ou tipo de dispositivo.

Embora não seja necessária para a entrega básica de ofertas, essa abordagem oferece flexibilidade para que os desenvolvedores criem experiências personalizadas orientadas por dados que vão além dos recursos de renderização padrão do HTML.

## Crie uma experiência baseada em código (CBE) com o tipo de conteúdo JSON.

Comece criando uma nova Experiência baseada em código (CBE) no Adobe Journey Optimizer e defina o Formato de conteúdo como JSON. O tipo de conteúdo instrui o AJO a retornar dados de oferta estruturados (como offerText, imagens ou metadados) como um objeto JSON em vez de HTML renderizado. Defina a plataforma (por exemplo, Web), o URL de destino onde a oferta é exibida e o local na página (como uma ID de container como offerContainer). Essa configuração permite que o aplicativo web receba dados de oferta e os renderize dinamicamente usando o JavaScript.

![json-content-type](assets/cbe-json-content.png)

## Associar o CBE a uma campanha com uma política de decisão

Depois que a Experiência baseada em código (CBE) com tipo de conteúdo JSON é criada, ela é vinculada a uma campanha por meio de uma Política de decisão. A Política de decisão define a lógica para qualificação, classificação e entrega de ofertas com base no perfil ou em dados contextuais.

Ao inserir a Política de decisão no Editor do Personalization (por exemplo, para mensagens no aplicativo ou emails), é importante garantir que a saída mantenha uma estrutura JSON válida.

Ao inserir uma Política de decisão no Editor do Personalization (PE) em uma campanha, o Adobe Journey Optimizer gera automaticamente um loop Handlebars com base na política selecionada. Por exemplo:
![código-padrão](assets/handlebar-code-default.png)
Esse loop repete todos os itens de decisão retornados pela política e injeta o campo offerText de cada oferta. Essa estrutura padrão funciona bem para tipos de conteúdo do HTML, mas ao trabalhar com conteúdo JSON, pode ser necessário reestruturar para produzir uma matriz ou objeto JSON válido, especialmente se o resultado estiver sendo analisado programaticamente.

![código reestruturado](assets/restructured-code.png)

Este modelo Handlebars foi projetado para produzir uma matriz JSON de objetos de oferta, em que cada objeto contém um único campo offerText. Ela faz loop pelos itens de decisão retornados pela Política de decisão especificada e envolve cada offerText em um formato de objeto JSON.

## Analisar resposta da oferta JSON

A resposta do AJO contém itens de decisão personalizados no formato JSON na estrutura `propositions[].items[].data.content[]`. Cada item de conteúdo inclui campos como offerText.

```javascript
(response.propositions || []).forEach(p => {
  (p.items || []).forEach(item => {
    const contents = item.data?.content || [];
    contents.forEach(contentItem => {
      const html = contentItem.offerText || "";
      const wrapper = document.createElement("div");
      wrapper.className = "offer";
      wrapper.innerHTML = html;
      document.getElementById("offerContainer").appendChild(wrapper);
    });
  });
});
```

### Ativos de amostra

Para ajudar você a começar, baixe o arquivo de amostra do HTML e o arquivo do JavaScript que demonstra como consumir ofertas baseadas em JSON e renderizá-las dinamicamente em sua página da Web.

[código JavaScript](assets/weather-related-offers-script-multiple-json.js)
[Arquivo HTML](assets/multiple-json.html)