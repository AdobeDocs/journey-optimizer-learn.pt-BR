---
title: Criar política de decisão
description: Uma política de decisão define a lógica usada para determinar quais ofertas são entregues a um usuário durante a personalização.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00Z
jira: KT-17728
exl-id: 186e4a7d-6077-401f-9958-2f955214bc35
source-git-commit: 6bf0c2487afff4811aa94e9591ae29c38af15d34
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Criar política de decisão

As políticas de decisão são containers para suas ofertas que aproveitam o mecanismo de decisão para escolher o melhor conteúdo a ser entregue, dependendo do público.

No editor de personalização, clique no item de política Decison na navegação à esquerda e clique em Add decision policy

![criar-política-decisão](assets/decision-policy.png)

Clique em Adicionar para selecionar a estratégia de seleção
Clique em Selecionar fallback para selecionar a oferta de fallback.
Clique em próximo para revisar a política de decisão e clique em criar para concluir o processo de criação da política de decisão.


![política-decisão](assets/decision-policy2.png)


## Usar a política de decisão no editor de código

No editor de personalização, clique em Insert policy. O código correspondente à política de decisão é adicionado.

Nesse estágio, você pode incluir quaisquer atributos de decisão necessários diretamente no código. Esses atributos são definidos no schema usado pelo catálogo Ofertas. Os atributos padrão são organizados no namespace __experience, enquanto os atributos personalizados específicos da sua organização são armazenados no namespace `_<imsOrg>`.

![using_decision_policy](assets/Insert-policy.png)

Esse código passa por uma lista de ofertas personalizadas escolhidas para o usuário e exibe o texto de cada uma na página da Web. Ele mostra a mensagem (chamada offerText) de cada oferta dentro de um parágrafo, para que os usuários possam ver seu conteúdo personalizado com clareza.
Se nenhuma oferta personalizada estiver disponível, uma oferta substituta será exibida para garantir que o espaço não seja deixado em branco.

Clique em Salvar e depois Ativar a campanha.
