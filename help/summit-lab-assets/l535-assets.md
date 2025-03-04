---
title: Folha de características do L535
description: Esta página contém textos e links que estão sendo usados no L535 Summit Lab.
feature: In App, SMS, Push, Email
doc-type: article
role: User
level: Beginner
recommendations: noDisplay, noCatalog
hide: true
hidefromtoc: true
exl-id: 1c3f4341-1293-463d-bee0-57440fcff23a
source-git-commit: 51ab40981a42b0df56d3994f1155eb4ae7575b17
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 21%

---

# Summit Lab L535: Folha de características

Esta página contém textos e links que estão sendo usados no L535 Summit Lab. Ele permite copiar e colar o conteúdo nas suas mensagens do Journey Optimizer.

## Links

* [Adobe Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:ajo-summit-lab/journey-optimizer/journeys)
* [Site SecurFinancial](https://dsn.adobe.com/web/hausmann-FTTN?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFub255bW91cyIsImVtYWlsIjoiYW5vbnltb3VzQGFkb2JlLmNvbSIsIm5hbWUiOiJBbm9ueW1vdXMiLCJpc1N1cGVyVXNlciI6ZmFsc2UsImlzc3VlciI6ImhhdXNtYW5uIiwicHJvamVjdHMiOnsiaGF1c21hbm4tRlRUTiI6InZpZXcifSwiaWF0IjoxNzQwNzU2NTYxLCJleHAiOjE3NDMzNDg1NjF9.ryOTsqDH9B33436RlIo4AHFxx8aGjNEMqv9FAxLZb9U)
* [Baixar o aplicativo](https://demo-system-next.s3.amazonaws.com/dxdemo/summit/index.html)

## Exercícios

### Exercício 2.3

**Etapa 12** Aviso de mensagem de email:

Gerar um email de boas-vindas para o novo SecurFinancial
clientes que acabaram de abrir uma nova conta poupança. Adicionar um
plano de ação para instalar o aplicativo móvel SecurFinancial.

### Exercício 3.1

**Etapa 7**

```javascript
{%#if select _Push_details1 from profile.pushNotificationDetails where
_Push_details1.token.isNotNull()%}
Welcome to your new SecurFinancial checking account! Discover the
SecurFinancial mobile app, designed for effortless banking. Manage accounts,
transfer funds, and monitor transactions securely, anytime, anywhere. Open the
app
{%else%}
Welcome to your new SecurFinancial checking account! Discover the
SecurFinancial mobile app, designed for effortless banking. Manage accounts,
transfer funds, and monitor transactions securely, anytime, anywhere. Click here
to install the app: https://demo-systemnext.
s3.amazonaws.com/dxdemo/summit/index.html
{%/if%} 
```


![Logotipo do SecureFinancial](/help/summit-lab-assets/assets/SecureFinancial-logo.png)

![Celular](/help/summit-lab-assets/assets/online-banking-app-01.png)


