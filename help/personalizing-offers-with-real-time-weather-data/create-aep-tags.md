---
title: Criar tags do Adobe Experience Platform
description: Criação de públicos da AJO com base nas preferências de investimento do usuário (ações, títulos, CDs)
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-18258
exl-id: 04fad076-e897-4831-9147-768721858a80
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
source-wordcount: '286'
ht-degree: 0%
---
# Criação de tags do Adobe Experience Platform

As Tags do Adobe Experience Platform (antigo Adobe Launch) ajudam a gerenciar e implantar* tecnologias de marketing e análise no seu site sem precisar alterar o código do site.

Este [vídeo descreve o processo de criação de Tags de Experiência do Adobe](https://experienceleague.adobe.com/pt-br/playlists/experience-platform-get-started-with-tags)

* Fazer logon na Coleção de dados
* Clique em _&#x200B;**Marcas -> Nova propriedade**
* Crie uma Marca do Adobe Experience Platform chamada _&#x200B;**personalization-on-weather**&#x200B;_.
* Adicionar as seguintes extensões à tag

![extensões-tags](assets/tags-extensions1.png)

* Adicione um elemento de dados chamado &quot;ECID&quot;, como mostrado abaixo. Esse elemento de dados é usado posteriormente nos relatórios

![ecid-data-element](assets/ecid-data-element.png)

* Certifique-se de configurar o Adobe Experience Platform Web SDK para usar o ambiente correto e o **datastream relacionado ao clima** criado na etapa anterior.

![web-sdk-configuration](assets/tags-extensions.png)



## Criar e implantar as tags do AEP


Crie uma nova biblioteca e adicione todos os recursos modificados a ela, conforme ilustrado nas capturas de tela abaixo.

**Adicionar biblioteca**

![nova-biblioteca](assets/tag-add-library.png)

**Criar uma biblioteca**

Na tela Criar biblioteca, especifique o nome da biblioteca e o ambiente.

Adicionar todos os recursos alterados a esta biblioteca
![biblioteca de marcas](assets/tag-build-library.png)

Clique no botão Salvar e criar no desenvolvimento para criar a biblioteca

## Incluir tags do AEP na página do HTML

Ao publicar uma propriedade de Marcas do AEP, a Adobe fornece uma marca de script que você deve colocar dentro da HTML ` <head>` ou na parte inferior das marcas ` <body>`.

1. Vá para a propriedade Tags (personalização no clima).
2. Clique em Ambientes e clique no ícone de instalação do ambiente desejado (por exemplo, Desenvolvimento, Armazenamento temporário, Produção).
3. Anote o código incorporado. Ela é necessária em um estágio posterior deste tutorial.
