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
source-git-commit: af70e8e589e3a4b48885d3ad1241ab8c140fa75a
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 29%

---

# Summit Lab L535: Folha de características

Esta página contém textos e links que estão sendo usados no L535 Summit Lab. Ele permite copiar e colar o conteúdo nas suas mensagens do Journey Optimizer.

## Links

* [Adobe Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:ajo-summit-lab/journey-optimizer/journeys)
* [Site SecurFinancial](https://dsn.adobe.com/web/hausmann-FTTN?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFub255bW91cyIsImVtYWlsIjoiYW5vbnltb3VzQGFkb2JlLmNvbSIsIm5hbWUiOiJBbm9ueW1vdXMiLCJpc1N1cGVyVXNlciI6ZmFsc2UsImlzc3VlciI6ImhhdXNtYW5uIiwicHJvamVjdHMiOnsiaGF1c21hbm4tRlRUTiI6InZpZXcifSwiaWF0IjoxNzQwNzU2NTYxLCJleHAiOjE3NDMzNDg1NjF9.ryOTsqDH9B33436RlIo4AHFxx8aGjNEMqv9FAxLZb9U)
* [Baixar o aplicativo](https://demo-system-next.s3.amazonaws.com/dxdemo/summit/index.html)

## Copiar e colar para exercícios

### Exercício 2.3 - Compor a mensagem de email

#### Prompt

```
Generate a welcome email for new SecurFinancial customers who just opened a new savings account. Add a call to action to install the SecurFinancial mobile app.
```

### Exercício 3.1 - Aplicar conteúdo dinâmico à mensagem SMS

#### Código

```
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

### Exercício 4.2 - Configuração dos tratamentos

#### Título

```
Welcome to SecurFinancial"
```

#### Texto do corpo

```
Did you know you can find an ATM near in the SecurFinancial app? Try it now!"
```

#### URL

```
dxdemo://atm
```

### Exercício 6 - Cartões de conteúdo

#### Título

```
Welcome to SecurFinancial!
```

#### Corpo

```
Thank you for downloading the app. You can find ATMs, track your spending and more. All within the app.
```

#### URL da mídia

```
https://demo-systemnext.s3.amazonaws.com/assets/securfinancial/homeloan.jpg
```

#### Título do botão

```
Find ATMs
```

#### URL de destino

```
dxdemo://atm
```

## Imagens

![Logotipo do SecureFinancial](/help/summit-lab-assets/assets/SecureFinancial-logo.png)


![Celular](/help/summit-lab-assets/assets/online-banking-app-01.png)


