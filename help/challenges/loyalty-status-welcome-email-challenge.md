---
title: Crie um email de boas-vindas com o status de fidelidade - Desafio
description: Entenda as noções básicas para a criação de uma jornada na tela de jornada.
kt: 8109
feature: Journeys
role: User
level: Beginner
hide: true
source-git-commit: 957515149af1281d29a45b24ca499ef097656eb8
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 8%

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

### Crie um segmento de Status de Diamante Luma.

Crie um segmento no Journey Optimizer chamado **seu nome - Luma - Diamond Status**.

### Criar Luma - Novo status - Diamante - Mensagem de email transacional

Criar uma mensagem de email de boas-vindas

1. Criar uma mensagem de email transacional com o título `(your name)_Luma – New Status – Diamond – Transactional email message`.
2. Enviar email para uma linha de assunto `Welcome to Diamond Status, (recipient's first name)!`.
3. Use o arquivo HTML fornecido **[DiamondStatusEmail.html](/help/challenges/assets/email-assets/DiamondStatusEmail.html)** para o corpo do email.


### **Jornada nº 3 - E-mail de boas-vindas para atualização do status do Diamond**

Envie um email quando um cliente de fidelidade mudar para um novo nível para parabenizá-lo e informá-lo sobre seus novos benefícios.

1. Crie uma jornada acionada quando um cliente passa para o novo nível de fidelidade Diamond (especificamente quando o cliente entra no segmento definido para um novo membro do nível Diamond) para enviar o email &quot;Luma - New Status - Diamond - Transactional&quot;
2. Depois de concluir, coloque a jornada no modo de teste e acione a jornada para enviar a si mesmo  

CRITÉRIOS DE SUCESSO

Você deve receber o email personalizado &quot;Luma - New Status - Diamond-Transactional&quot;.
