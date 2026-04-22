---
title: Depuração do push da Web no AJO
description: Esta página fornece dicas úteis para depurar o fluxo de notificação por push da Web, incluindo a verificação de solicitações do Web SDK,
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 45f86aeb8fca071436785cc55225d853bb21998f
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Depuração do push da Web no AJO

Esta página fornece dicas úteis para depurar o fluxo de notificação por push da Web, incluindo a verificação de solicitações do Web SDK, a verificação da ECID e do perfil do usuário no AEP e a garantia de que eventos como price.drop sejam enviados e recebidos corretamente.

- **Usar o Adobe Experience Platform Debugger (Chrome Extension)**\
  Instale a [extensão do AEP Debugger para Chrome](https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob) para inspecionar a atividade do Web SDK com mais facilidade:

Essa ferramenta permite:
- Exibir solicitações e respostas do Web SDK\
- Verifique a ECID (Experience Cloud ID)\
- Validar a configuração da sequência de dados e as cargas

- **Verificar se o usuário foi identificado (ECID)**\
  Use o AEP Debugger ou o console do navegador para confirmar se uma ECID foi gerada. Essa ID é usada para rastrear o usuário no AEP e no AJO.

- **Use a guia Rede para verificar solicitações**\
  Abra a **guia Rede** nas ferramentas de desenvolvedor do seu navegador e filtre as solicitações feitas pelo Web SDK (procure `/collect` ou `interact`).
   - Confirme se as solicitações estão sendo enviadas quando a página é carregada e quando as ações são acionadas
   - Verifique se o evento `price.drop` está incluído na carga

- **Pesquisar o perfil de usuário no AEP**\
  Use a ECID para pesquisar o perfil do usuário no Adobe Experience Platform. Isso ajuda a confirmar que o usuário é reconhecido e que seus dados (como assinatura push) estão sendo armazenados corretamente.

- **Verificar se o evento `price.drop` foi recebido**\
  Depois de acionar o evento na página da Web, verifique no AEP se o evento foi assimilado e associado à mesma ECID.
Verifique o json do evento message.feedback para `feedback.status`. O valor de status deve ser `sent`
  ![queda de preço](assets/price-drop-profile-event.png)

- **Confirmar se as notificações por push estão habilitadas**\
  Verifique se:
   - O usuário aceitou o prompt de notificação do navegador
   - Existe um token de push no perfil do usuário

- **Verificar a configuração do jornada**\
  Verifique se a jornada foi publicada e configurada para escutar o evento `price.drop`.

