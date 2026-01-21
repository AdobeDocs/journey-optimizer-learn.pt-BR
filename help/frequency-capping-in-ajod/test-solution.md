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
exl-id: 6b6c66d3-218d-4f5b-adb0-a2eca05989ab
source-git-commit: bef6d831c639d40514552dae3ff20132626a4a09
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---

# Testar a solução

## Implantar os ativos de amostra

Se você não tiver o Node.js instalado, baixe e [instale-o daqui](https://nodejs.org/)

Verifique a instalação executando:

`node -v`

`npm -v`

## Configurar a pasta do projeto

Crie um novo diretório para o aplicativo de amostra usando os seguintes comandos:

`mkdir frequency-capping `

`cd frequency-capping `

## Inicializar o projeto

`npm init -y`

## Instalar as estruturas necessárias

`npm install express`

## Copiar arquivos de ativos

* Descompacte e coloque o conteúdo do [server.zip](assets/server.zip) na pasta `frequency-capping`.
* Extraia o conteúdo de [public.zip](assets/public.zip)para a pasta &#39;frequency-capping&#39;

## Atualizar o url da superfície no arquivo javascript

Abra o `frequency-capping.js` localizado em `public\scripts` e atualize a propriedade de superfícies para corresponder à configuração de canal usada na campanha

## Iniciar servidor JS do nó

Navegue até a pasta `c:\frequency-capping`. Execute o comando `node server.js` para iniciar o servidor js do nó na porta 3000


## Atualizar a propriedade Tags do Adobe Experience Platform

Abra o arquivo `frequency-capping.html` localizado na pasta `public` do editor de texto e substitua a marca de script pela marca de script da Propriedade de Marca da Adobe Experience Platform criada na etapa anterior deste tutorial. Certifique-se de salvar o arquivo

```
<script src="https://assets.adobedtm.com/AEM_TAGS/launch-ENabcd1234.min.js" async></script>
```

## Interagir com as ofertas

* Abra a [página da Web](http://localhost:3000) em seu navegador favorito.
* Interagir com a oferta
* Atualizar a página
* Dependendo das regras de limite de frequência, você deve ver uma nova oferta

## Exibir o relatório

* Fazer logon no Journey Optimizer
* Navegue até Gerenciamento de Jornadas ->Campanhas
* Clique na campanha e selecione o relatório apropriado no menu de relatório.
