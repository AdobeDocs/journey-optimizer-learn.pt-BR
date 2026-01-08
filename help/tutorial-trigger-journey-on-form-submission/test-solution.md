---
title: Testar a solução
description: Criar jornada para enviar email no envio do formulário
feature: Journeys
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-12-25T00:00:00Z
jira: KT-20014
source-git-commit: 6e773afb6bf1770467f9c02739e6b3ede29c81f4
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# Testar a solução


Testar a solução
>[!VIDEO](https://video.tv.adobe.com/v/3478551?captions=por_br)

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
* Descompacte o conteúdo de [index.zip] na pasta pública
* atualize o arquivo `.env` com os valores apropriados. Esses valores estão disponíveis no comando cURL baixado ao criar a conexão HTTP Source

## Executar o servidor

Verifique se você está no diretório `trigger-journey`.
Executar o comando `node server.js`
Aponte seu navegador para [página da Web](http://localhost:3000/)
Preencha e envie o formulário. A jornada é acionada e um email é enviado para a ID de email inserida no formulário.


