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
source-git-commit: 201470e35095b38617d1a1bb5d7b16c1e60f431e
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 24%

---

# Summit Lab L535: Folha de características

Esta página contém textos e links que estão sendo usados no L535 Summit Lab. Ele permite copiar e colar o conteúdo nas suas mensagens do Journey Optimizer.

## Links

* [Site SecurFinancial](https://dsn.adobe.com/web/hausmann-FTTN?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFub255bW91cyIsImVtYWlsIjoiYW5vbnltb3VzQGFkb2JlLmNvbSIsIm5hbWUiOiJBbm9ueW1vdXMiLCJpc1N1cGVyVXNlciI6ZmFsc2UsImlzc3VlciI6ImhhdXNtYW5uIiwicHJvamVjdHMiOnsiaGF1c21hbm4tRlRUTiI6InZpZXcifSwiaWF0IjoxNzQwNzU2NTYxLCJleHAiOjE3NDMzNDg1NjF9.ryOTsqDH9B33436RlIo4AHFxx8aGjNEMqv9FAxLZb9U){target="_blank"}
* [Adobe Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:ajo-summit-lab/journey-optimizer/journeys){target="_blank"}
* [Pasta de TrabalhoL535](/help/summit-labs/summit-lab-assets/assets/summit_lab_manual_l535-final-v4.pdf){target="_blank"}
* [Baixar o aplicativo](https://demo-system-next.s3.amazonaws.com/dxdemo/summit/index.html){target="_blank"}

## Copiar e colar para exercícios

### Exercício 2.1 - Logon no Journey Optimizer

Faça logon usando os seguintes detalhes:

Endereço de email:    L535+*seu assento número*@adobeeventlab.com

Senha:       Adobe4Summit!


### Exercício 2.3 - Compor a mensagem de email

#### Solicitação

```
Generate a welcome email for new SecurFinancial customers who just opened a new checking account. 
Add a call to action to install the SecurFinancial mobile app.
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
Welcome to SecurFinancial
```

#### Texto do corpo

```
Did you know you can find an ATM near in the SecurFinancial app? Try it now!
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
https://demo-system-next.s3.amazonaws.com/assets/securfinancial/home-loan.jpg
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

![Logotipo do SecureFinancial](/help/summit-labs/summit-lab-assets/assets/SecureFinancial-logo.png)


![Celular](/help/summit-labs/summit-lab-assets/assets/online-banking-app-01.png)
