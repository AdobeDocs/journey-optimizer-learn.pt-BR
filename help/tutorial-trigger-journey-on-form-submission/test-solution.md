---
title: Testar a solução
description: Criar jornada para enviar email no envio do formulário
feature: Journeys
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-12-25T00:00:00.000Z
jira: KT-20014
exl-id: 9b4a3e0c-d153-4a6b-a7de-b926bd669f6a
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
    internal-label: Journeys
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%
---
# Testar a solução


Testar a solução
>[!VIDEO](https://video.tv.adobe.com/v/3478546)

## Implantar os ativos de amostra

Se você não tiver o Node.js instalado, baixe e [instale-o daqui](https://nodejs.org/)

Verifique a instalação executando:

`node -v`

`npm -v`

## Configurar a pasta do projeto

Crie um novo diretório para o aplicativo de amostra usando os seguintes comandos:

`mkdir trigger-journey `

`cd trigger-journey`

## Inicializar o projeto

`npm init -y`

## Instalar as estruturas necessárias

`npm install express dotenv axios cors`

## Copiar arquivos de ativos

* Descompacte e coloque o conteúdo de [project-root.zip](assets/project-root.zip) na pasta `trigger-journey`.

* Crie uma pasta chamada `public` na pasta `trigger-journey`
* atualize o arquivo `.env` com os valores apropriados. Esses valores estão disponíveis no comando cURL baixado ao criar a conexão HTTP Source.
* Descompacte o conteúdo de [index.zip](assets/index.zip) na pasta `public`

## Executar o servidor

Verifique se você está no diretório `trigger-journey`.
Executar o comando `node server.js`
Aponte seu navegador para a [página da Web](http://localhost:3000/)
Preencha e envie o formulário. A jornada é acionada e um email é enviado para a ID de email inserida no formulário.
