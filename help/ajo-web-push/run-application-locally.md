---
title: Executar o aplicativo localmente
description: Configurar o aplicativo de amostra localmente para explorar o fluxo de notificação por push da Web usando o AJO.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 45f86aeb8fca071436785cc55225d853bb21998f
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Executar o aplicativo localmente

Esta página orienta você na configuração local do aplicativo de amostra para que você possa testar e explorar o fluxo de notificação por push da Web usando o Adobe Journey Optimizer. Você irá clonar o repositório, configurar as variáveis de ambiente e executar o aplicativo em seu sistema local.


Siga estas etapas para executar o aplicativo de amostra no sistema local.

## &#x200B;1. Instalar Node.js

Verifique se você tem o **Node.js (versão 16 ou superior)** instalado em seu sistema.

Você pode [baixá-lo aqui:](https://nodejs.org/)

Verificar a instalação

```node -v```

```npm -v```


## &#x200B;2. Clonar o repositório

```git clone https://github.com/gbedekar489/ajo-web-push.git```

```cd ajo-web-push```

## &#x200B;3. Instalar dependências

```npm install```

## &#x200B;4. Configurar variáveis de ambiente

Crie um arquivo .env no diretório raiz e adicione o seguinte:

```
DATASTREAM_ID=your_datastream_id
ORG_ID=your_org_id
VAPID_PUBLIC_KEY=your_vapid_public_key
APP_ID=your_app_id
DATASET_ID=your_profile_dataset_id
PORT=3000
```

Quando executados localmente, esses valores são lidos do arquivo .env. Na produção (por exemplo, Renderização), eles são configurados como variáveis de ambiente.