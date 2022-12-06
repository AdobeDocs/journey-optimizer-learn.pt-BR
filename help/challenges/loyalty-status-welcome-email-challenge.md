---
title: Crie um email de boas-vindas com o status de fidelidade - Desafio
description: Entenda as noções básicas para a criação de uma jornada na tela de jornada.
kt: 8109
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: 6fd58b8e-7178-495d-a85d-eb67fc4f3acf
source-git-commit: e148101f8404c8e2019ee17823bcf1d7a9668bc5
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 4%

---

# Crie um email de boas-vindas com o status de fidelidade - Desafio

![Status de fidelidade do AJO e-mail de boas-vindas - Banner de desafios](/help/challenges/assets/email-assets/luma-transactional-onboarding-1.png)

| Desafio | Criar um email de boas-vindas do status de fidelidade |
|---|---|
| Perfil | Gerenciador de jornadas |
| Competências necessárias | <ul><li>[Criar segmentos](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html)</li> <li>[Qualificação do segmento](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment-qualification.html)</li><li>[Importar conteúdo de HTML](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-emails/import-and-author-html-email-content.html)</li></ul> |
| Ativos para baixar | [platinumStatusEmail.zip](/help/challenges/assets/email-assets/platinumStatusEmail.zip) |

## A História

O Luma oferece um programa de fidelidade como uma maneira de atrair e manter seus clientes. O programa oferece quatro níveis diferentes: Bronze, prata, ouro e platina. Cada nível de fidelidade recebe diferentes níveis ou recompensas, descontos e outros incentivos especiais como recompensa para seus negócios repetidos.

Sublinhar o status de platina especial. O Luma deseja enviar um email de boas-vindas para os clientes, quando eles atingirem a camada de platina.

## Seu desafio

Você foi solicitado a configurar uma jornada que envia automaticamente um email de boas-vindas para os clientes quando eles atingem o nível de fidelidade do platinum.

>[!BEGINTABS]

>[!TAB Tarefa]

Quando um cliente de fidelidade se qualifica para o nível platinum, ele deve receber um e-mail para parabenizá-lo e informá-lo sobre seus novos benefícios. A equipe criativa forneceu um arquivo HTML **[Luma - atualização de status - e-mail de boas-vindas](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip)** com o corpo do email.

1. Crie um segmento no Journey Optimizer chamado `Luma – status upgrade`.
2. Crie uma jornada chamada &#39;Luma - New Status - platinum&#39;.
   1. Um cliente se move para a jornada, quando se qualifica para o nível de fidelidade platinum.
   2. O cliente deve receber uma mensagem de email rotulada `Luma – Platinum Status - Welcome`, com a linha de assunto `Welcome to Platinum Status, (recipient's first name)!` com o corpo fornecido pela equipe criativa.
   3. Ao fazer upload do arquivo HTML, você percebe que o email se refere ao status de &quot;diamante&quot;, em vez de &quot;platina&quot;. Em vez de solicitar um novo arquivo da equipe criativa, atualize o email no designer de email.

>[DICA!]
> Certifique-se de que o Luma - Status Platinum - Email de boas-vindas é transacional.


>[!TAB Critérios de sucesso]

Teste a jornada:

1. Certifique-se de que a Atividade de leitura de segmento tenha o namespace definido como **ID do CRM Luma (lumaCrmId)**
2. Substitua os parâmetros de email padrão e os defina como seu próprio endereço de email

+++ Clique aqui para obter mais informações sobre como substituir
   * Mostre os valores ocultos clicando no símbolo dos olhos.
   * Nos parâmetros de Email , clique no símbolo T (ativar substituição de parâmetro)

   ![Substituir parâmetros de email](/help/challenges/assets/c3-override-email-paramters.jpg)

   * Clique no campo Endereço
   * Na próxima tela, adicione o endereço de email entre parênteses: `"yourname@yourdomain"` no editor de expressão e clique em ok.
+++


3. Defina a jornada para o modo de teste
4. Acionar um evento
5. Adicione a seguinte ID do CRM para Stanleigh Stooke no campo Identificador de perfil: `4f34057d9d9e792c28ba18ecae378e98`

Você deve receber o *Luma - Status platinum - Bem-vindo* email.

>[!TAB Verificar o seu trabalho]

Esta é a aparência da sua jornada:

![platinum-status-upgrade-jornada](/help/challenges/assets/journey-luma-status-upgrade.png)


Esta é a aparência do email:

![Luma - atualização de status - e-mail de boas-vindas](/help/challenges/assets/status-upgrade-welcome-email.png)

>[!ENDTABS]
