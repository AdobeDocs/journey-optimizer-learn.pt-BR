---
title: Crie um email de boas-vindas com o status de fidelidade - Desafio
description: Entenda as noções básicas para a criação de uma jornada na tela de jornada.
kt: 8109
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: 6fd58b8e-7178-495d-a85d-eb67fc4f3acf
source-git-commit: 30d2e0b2cad59385c8b9bc98f7db671027f7906a
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 7%

---

# Crie um email de boas-vindas com o status de fidelidade - Desafio

![Status de fidelidade do AJO e-mail de boas-vindas - Banner de desafios](/help/challenges/assets/email-assets/luma-transactional-onboarding-1.png)

| Desafio | Criar um email de boas-vindas do status de fidelidade |
|---|---|
| Perfil | Gerenciador de jornadas |
| Competências necessárias | <ul><li>[Criar conteúdo de email com o editor de mensagens](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-email-content-with-the-message-editor.html?lang=en)</li> <li>[Usar informações de evento contextual para personalização](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-contextual-event-information-for-personalization.html?lang=en)</li><li>[Usar funções auxiliares para personalização](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-helper-functions-for-personalization.html?lang=en)</li></ul> |
| Ativos para baixar | [Ativos de confirmação de pedido](/help/challenges/assets/email-assets/order-confirmation-assets.zip) |

## A História

O Luma oferece um programa de fidelidade como uma maneira de atrair e manter seus clientes. O programa oferece quatro níveis diferentes: Prata, ouro, platina e diamante.

Cada nível de fidelidade recebe diferentes níveis ou recompensas, descontos e outros incentivos especiais como recompensa para seus negócios repetidos.

Para sublinhar o status especial do diamante. O Luma deseja enviar um email de boas-vindas para os clientes, quando eles atingirem a camada de diamante.

## Seu desafio

Você foi incumbido de configurar uma jornada que envia automaticamente um email de boas-vindas para os clientes quando eles atingem o nível de fidelidade de diamante.

>[!NOTE]
> Se você estiver trabalhando em uma sandbox de treinamento compartilhado, é prática recomendada adicionar seu nome ou iniciais como um prefixo ao nome de qualquer elemento que você criar.

>[!BEGINTABS]

>[!TAB Tarefa]

Envie um e-mail quando um cliente de fidelidade mudar para um nível do Diamond para parabenizá-lo e informá-lo sobre seus novos benefícios. As seleções de menu

1. Crie um segmento no Journey Optimizer chamado **Luma - Status do Diamante**
2. Crie uma jornada acionada quando um cliente passa para o novo nível de fidelidade Diamond (especificamente quando o cliente entra no segmento definido para um novo membro do nível Diamond) para enviar o email &quot;Luma - New Status - Diamond - Transactional&quot;
   1. Criar uma mensagem de email transacional com o título `(your name)_Luma – New Status – Diamond – Transactional email message`.
   2. Enviar email para uma linha de assunto `Welcome to Diamond Status, (recipient's first name)!`.
   3. Use o arquivo HTML fornecido **[DiamondStatusEmail.html](/help/challenges/assets/email-assets/DiamondStatusEmail.html)** para o corpo do email.
3. Depois de concluir, coloque a jornada no modo de teste e acione a jornada para enviar a si mesmo  

   1. Criar uma mensagem de email transacional com o título `(your name)_Luma – New Status – Diamond – Transactional email message`.
   1. Enviar email para uma linha de assunto `Welcome to Diamond Status, (recipient's first name)!`.
   1. Use o arquivo HTML fornecido **[DiamondStatusEmail.html](/help/challenges/assets/email-assets/DiamondStatusEmail.html)** para o corpo do email.

1. Depois de concluir, coloque a jornada no modo de teste e acione a jornada para enviar a si mesmo  

### Criar Luma - Novo status - Diamante - Mensagem de email transacional

Criar uma mensagem de email de boas-vindas

### **Jornada nº 3 - E-mail de boas-vindas para atualização do status do Diamond**


>[!TAB Critérios de sucesso]

Teste a jornada:

1. Certifique-se de que o evento de qualificação de segmento tenha o Namespace = Email
1. Substitua os parâmetros de email padrão e os defina como seu próprio endereço de email
1. Defina a jornada para o modo de teste
1. Acionar um evento
1. Adicione o seguinte endereço de email ao campo Identificador de perfil: Jenna_Palmer9530@emailsim.io

Você deve receber o email personalizado &quot;Luma - New Status - Diamond-Transactional&quot;.

>[!TAB Verificar o seu trabalho]

Esta é a aparência da sua jornada:

![Status do Diamond-upgrade-jornada](/help/challenges/assets/journey-luma-diamond-status-upgrade.png)

>[!ENDTABS]
