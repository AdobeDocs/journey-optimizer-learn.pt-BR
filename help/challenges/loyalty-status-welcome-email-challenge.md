---
title: Crie um email de boas-vindas com o status de fidelidade - Desafio
description: Crie uma jornada que envia automaticamente um email de boas-vindas para os clientes quando eles atingem o nível de fidelidade.
jira: KT-8109
feature: Journeys
role: User
level: Beginner
last-substantial-update: 2023-02-01T00:00:00Z
exl-id: 6fd58b8e-7178-495d-a85d-eb67fc4f3acf
source-git-commit: 7861e0ca17a616273f5ea1b4d850310f1f4ec8b8
workflow-type: ht
source-wordcount: '421'
ht-degree: 100%

---

# Criar um email de boas-vindas com o status de fidelidade - Desafio

| Desafio | Crie um email de boas-vindas com o status de fidelidade |
|---|---|
| Perfil | Gerenciador de Jornadas |
| Competências necessárias | <ul><li>[Criar segmentos](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=pt-BR)</li> <li>[Qualificação do segmento](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment-qualification.html?lang=pt-BR)</li><li>[Importar conteúdo HTML](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/import-and-author-html-email-content.html?lang=pt-BR)</li></ul> |
| Ativos para baixar | [StatusUpgradeEmail.zip](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip) |

{style="table-layout:auto"}

## A história

A Luma oferece um programa de fidelidade como uma maneira de atrair e manter seus clientes. O programa oferece quatro níveis diferentes: bronze, prata, ouro e platina. Cada nível de fidelidade recebe diferentes recompensas, descontos e outros incentivos especiais como recompensa por seus negócios frequentes.

Para enfatizar o status especial “platina”, a Luma deseja enviar um email de boas-vindas para os clientes quando eles atingirem o nível platina.

## Seu desafio

Você foi solicitado a configurar uma jornada que envia automaticamente um email de boas-vindas para os clientes quando eles atingirem o nível de fidelidade platina.

>[!BEGINTABS]

>[!TAB Tarefa]

Quando um cliente do programa de fidelidade se qualifica para o nível platina, ele deve receber um email para parabenizá-lo e informá-lo sobre seus novos benefícios. A equipe criativa forneceu um arquivo HTML **[Luma - atualização de status - email de boas-vindas](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip)** com o corpo do email.

1. Crie um [!UICONTROL segmento] no Journey Optimizer chamado `Luma - platinum status`.

1. Criar uma jornada chamada `Luma - New Status - platinum`.

   1. Um cliente entra na jornada quando se qualifica para o nível de fidelidade platina.

   1. O cliente deve receber uma mensagem de email rotulada `Luma - Platinum Status - Welcome`, com a linha de assunto `Welcome to Platinum Status, {firstName}!` e com o corpo de email fornecido pela equipe criativa. Esse é um email [!UICONTROL transacional].

   1. Ao fazer upload do arquivo HTML, você percebe que o email se refere ao status “diamante”, em vez de “platina”. Em vez de solicitar um novo arquivo da equipe criativa, atualize o email no [!UICONTROL Designer de email].

>[!TAB Critérios de sucesso]

Teste a jornada:

1. Certifique-se de que a [!UICONTROL atividade Ler segmento] tem o [!UICONTROL namespace] definido como **[!DNL Luma CRM id(lumaCrmId)]**.

1. Substitua os [!UICONTROL parâmetros de email] padrão e defina-os como seu próprio endereço de email:
   * Nos **[!UICONTROL parâmetros de email]**, clique no ícone de T (habilitar a substituição de parâmetro)

   * Clique no campo **[!UICONTROL Endereço]**.

   * Na próxima tela, adicione seu endereço de email entre parênteses (`"yourname@yourdomain"`) no editor de expressão e clique em **[!UICONTROL OK]**.

1. Defina a jornada para o modo de teste.

1. Selecione **[!UICONTROL Acionar um evento]**.

1. Adicione a seguinte `CRM ID` para `Stanleigh Stooke` no campo **[!UICONTROL Identificador de perfil]**: `4f34057d9d9e792c28ba18ecae378e98`

**Resultado:** você deve receber o email personalizado *Luma - status platina - boas-vindas*.

É assim que o email deve parecer:

![Luma - atualização de status - email de boas-vindas](/help/challenges/assets/status-upgrade-welcome-email.png)

>[!TAB Verifique o seu trabalho]

O segmento deve ter essa aparência:

![Luma - status platinum - segmento](/help/challenges/assets/segment-luma-platinum-status.png)

Esta deve ser a aparência da sua jornada:

![platinum-status-upgrade-jornada](/help/challenges/assets/journey-luma-status-upgrade.png)

>[!ENDTABS]
