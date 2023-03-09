---
title: Folha de características do L731
description: Esta página contem texto e links que estão sendo usados no Summit Lab L731.
feature: In App, SMS, Push, Email
doc-type: article
role: User
level: Beginner
recommendations: noDisplay, noCatalog
hide: true
hidefromtoc: true
exl-id: ffc5e8c8-8729-4e7e-aa51-d74f91b0cf29
source-git-commit: e2312c022f589ebf1218e1767bbc129b57fa1e2a
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 64%

---

# Summit Lab L731 - Folha de características

Esta página contem texto e links que estão sendo usados no Summit Lab L731. Ele permite copiar e colar o conteúdo nas suas mensagens do Journey Optimizer.

## Exercício 1.1 - Baixar e instalar o aplicativo

### iOS

![Código QR para o iOS](/help/assets/lab731-ios-qr-code.png)

### Android - Espaço reservado

![Código QR para Android](/help/assets/lab731-ios-qr-code.png)


## Exercício 1.3: Fazer logon no Adobe Journey Optimizer

[Clique aqui para fazer logon no Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-2023-ajo-lab/journey-optimizer/home)

**Detalhes de logon:**

* **Nome de usuário:** `L731+<your seat number>@summitlab.us` (exemplo: L731+001@summitlab.us)
* **Senha:** Adobe2023!


## Exercício 2.1 - Criar uma campanha no aplicativo



| Campo | Texto | Links |
|----|----|----|
| Nome da campanha | `<your seat number> March Vegas Campaign` |  |
| Correspondência | booknow |  |
| Opção de URL de mídia |  | https://mcfadyen.com/wp-content/uploads/2023/01/Adobe-Summit-2023-Banner.png |
| Título | Está rolando e está ao vivo! |  |
| Corpo | O Adobe Summit voltará a Las Vegas de 21 a 23 de março de 2023. Prepare-se para palestrantes inspiradores, sessões de expansão de habilidades e novas conexões. |  |
| Botão | Reserve o hotel agora e economize 10% | lab://booking?suite=presidential&amp;discount=10 |
| Botão: Evento interativo | CTA no aplicativo |  |
| URL básica |  | iOS: lab:// <br>Android: https://lab |



## Lição 3 - Criar uma jornada omnicanal

| Mensagem | Linha de título/assunto | Texto | Link |
|----|----|----|----|----|
| Push | Bem-vindo a Vegas Stay! | Faça o check-in no aplicativo móvel e evite filas | lab://checkin |  |
| SMS |  | Bem-vindo a sua estadia em Vegas. Faça o check-in no aplicativo móvel e evite filas: lab://checkin |  |
| email | {{profile.person.name.firstName}}Você está em check-in, agora confira nossas ofertas para sua estadia! |  |  |


Esta é a imagem que estamos usando para o SMS e a notificação por push:

![Check-in online](/help/assets/vegas_online_check_in.jpg)
