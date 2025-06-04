---
title: Enviar CRMID para o Adobe Experience Platform
description: Criar tags do Adobe Experience Platform para enviar o CRMID recebido do navegador para o Adobe Experience Platform
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18089
exl-id: 894ad6b7-c4b4-465e-8535-3fdcd77e00eb
source-git-commit: 82d82b3aac2bf91e259b01fd8c6b4d6065f9640a
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 9%

---

# Enviar CRMID para o Adobe Experience Platform

O Adobe Launch (Tags) é usado para enviar a CRMID para o Adobe Experience Platform (AEP), pois fornece um mecanismo flexível e orientado por eventos para transmitir dados de identidade diretamente do navegador. Enviar o CRMID após o logon do usuário permite que o AEP vincule o ECID anônimo ao perfil de CRM conhecido, permitindo a identificação precisa da identidade. Esse vínculo forma a base para a criação de perfis unificados de clientes, a qualificação de públicos e o fornecimento de experiências personalizadas em tempo real no Adobe Journey Optimizer (AJO).

Uma propriedade de Tags da AEP chamada FinWise é criada. As seguintes extensões foram adicionadas à propriedade Tags

![extensões-tags](assets/tags-extensions.png)

Configure a extensão do AEP Web SDK usando o DataStream dos Supervisores Financeiros criado na etapa anterior.
O Serviço da Experience Cloud ID é uma extensão opcional adicionada à propriedade da tag para fins de depuração.

## Marcar elementos de dados

Crie os seguintes elementos de dados

| Elemento de dados | Extensão | Tipo de elemento de dados | Configurações personalizadas |
|--------------|-----------------------------------|---------------------------|----------------------------------------|
| crmid | Camada de dados de clientes Adobe | Estado calculado da camada de dados | user.crmid |
| ECID | Serviço da Experience Cloud ID | ECID |                                        |
| identidade | SDK da Web da Adobe Experience Platform | Mapa de identidade | ![imagem](assets/identity-settings.png) |
| XDMVariable | SDK da Web da Adobe Experience Platform | Variable | ![imagem](assets/xdmvariable.png) |

## Criar regra

Crie uma regra chamada userLoggedin com o seguinte evento e ações

Evento
![evento](assets/data-pushed-event.png)

Atualizar ação de variável
![variável-atualização](assets/update-variable.png)
Enviar ação do evento
![enviar-evento](assets/send-event.png)

## Salvar e criar

Salve as alterações, crie e crie a biblioteca.
