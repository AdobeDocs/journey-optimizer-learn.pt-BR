---
title: Criar tags do Adobe Experience Platform
description: Criação de públicos da AJO com base nas preferências de investimento do usuário (ações, títulos, CDs)
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18258
exl-id: 04fad076-e897-4831-9147-768721858a80
source-git-commit: 40690024e5348dd3ac05f350e49a67a99d5e455e
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# Criação de tags do Adobe Experience Platform

As Tags do Adobe Experience Platform (antigo Adobe Launch) ajudam a gerenciar e implantar* tecnologias de marketing e análise no seu site sem precisar alterar o código do site.

Este [vídeo descreve o processo de criação de Tags de Experiência do Adobe](https://experienceleague.adobe.com/en/playlists/experience-platform-get-started-with-tags)

- Fazer logon na Coleção de dados
- Clique em _&#x200B;**Marcas -> Nova propriedade**&#x200B;_

- Crie uma Marca do Adobe Experience Platform chamada _&#x200B;**personalization-on-weather**&#x200B;_.

- Adicionar as seguintes extensões à tag
  ![extensões-tags](assets/tags-extensions1.png)
- Adicione um elemento de dados chamado &quot;ECID&quot;, como mostrado abaixo. Esse elemento de dados é usado posteriormente nos relatórios
  ![ecid-data-element](assets/ecid-data-element.png)

- Certifique-se de configurar o Adobe Experience Platform Web SDK para usar o ambiente correto e o **datastream relacionado ao clima** criado na etapa anterior.
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

Ao publicar uma propriedade de Marcas do AEP, a Adobe fornece uma marca de script que você deve colocar dentro da HTML ``` <head>``` ou na parte inferior das marcas ``` <body>```.

- Vá para a propriedade Tags (personalização no clima).

- Clique em Ambientes e clique no ícone de instalação do ambiente desejado (por exemplo, Desenvolvimento, Armazenamento temporário, Produção).

- Anote o código incorporado. Ela é necessária em um estágio posterior deste tutorial.
