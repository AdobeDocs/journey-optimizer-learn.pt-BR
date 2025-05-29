---
title: Criar ofertas com base em localização com direcionamento por código postal
description: Um item de oferta na decisão representa uma única parte do conteúdo personalizado, como uma mensagem, imagem, promoção ou recomendação, que pode ser entregue a um usuário com base em regras e condições definidas.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-30T00:00:00Z
jira: KT-18188
source-git-commit: 58d2964644bc199b9db212040676d87d54f767b9
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# Criar ofertas com base em localização com direcionamento por código postal

Antes de criar as ofertas, o esquema de Item de oferta foi estendido para incluir um novo campo: código postal. Esse campo personalizado permite que cada oferta seja explicitamente marcada com seu código postal de destino, permitindo filtragem e classificação com base na localização durante a tomada de decisão.

Com o schema atualizado, duas ofertas personalizadas foram criadas:

* Oferta 1: &quot;Planos de investimento flexíveis para Mira Mesa (92126)&quot;
Personalizada para jovens profissionais e residentes com foco na tecnologia no 92126, essa oferta promove opções de investimento flexíveis, como ETFs e fundos mútuos voltados para o crescimento a longo prazo. O campo de código postal está definido como 92126.

* Oferta 2: &quot;CDs de alto rendimento para Rancho Bernardo (92128)&quot;
Direcionado a indivíduos financeiramente estáveis e prontos para aposentadoria em 92128, essa oferta apresenta Certificados de Depósito (CDs) de alto rendimento com retornos garantidos. O campo de código postal está definido como 92128.

Essas ofertas agora são enriquecidas com metadados de localização, tornando-as elegíveis para seleção dinâmica e classificação com base nos CEPs do perfil do usuário em etapas posteriores.

A captura de tela a seguir mostra os atributos personalizados adicionados ao esquema de item de oferta.

![metadados-ofertas](assets/offers-meta-data.png)


## Oferta para 92126

O texto da oferta para ofertas no código postal 92126

```html
<div style="max-width: 600px; margin: 2rem auto; padding: 1.5rem; border: 1px solid #ddd; border-radius: 12px; font-family: Arial, sans-serif; background-color: #f9f9f9; box-shadow: 0 4px 12px rgba(0,0,0,0.05);">   <h2 style="color: #1a237e; font-size: 1.5rem; margin-bottom: 0.5rem;">     Boost Your Financial Game with Smart Investment Options   </h2>   <p style="color: #333; font-size: 1rem; line-height: 1.6;">     In Mira Mesa (92126), ambition meets opportunity. Whether you're building wealth or just getting started, our     <strong>diversified investment plans</strong> — including <strong>tech-focused ETFs</strong> and     <strong>flexible mutual funds</strong> — are designed to grow with your goals.   </p>   <p style="color: #333; font-size: 1rem; line-height: 1.6;">     Enjoy expert guidance, low fees, and strategies built for busy professionals who want more from their money — without the hassle.   </p>   <a href="#start-investing" style="display: inline-block; margin-top: 1rem; background-color: #1a73e8; color: white; padding: 0.75rem 1.25rem; border-radius: 8px; text-decoration: none; font-weight: bold;">     Start Investing Smarter   </a> </div>
```


## Oferta para 92128

O texto da oferta para ofertas no código postal 92128

```html
<div style="max-width: 600px; margin: 2rem auto; padding: 1.5rem; border: 1px solid #ddd; border-radius: 12px; font-family: Arial, sans-serif; background-color: #fdfdfd; box-shadow: 0 4px 12px rgba(0,0,0,0.05);">   <h2 style="color: #1a237e; font-size: 1.5rem; margin-bottom: 0.5rem;">     Grow Your Savings with Confidence – Exclusive CD Rates for 92128   </h2>   <p style="color: #333; font-size: 1rem; line-height: 1.6;">     Live in Rancho Bernardo? Take advantage of your financial momentum with our <strong>high-yield Certificates of Deposit</strong>, offering up to <strong>5.25% APY</strong>.     Designed for peace of mind and smart growth, our flexible CD options let you lock in guaranteed returns while enjoying the stability you deserve.   </p>   <p style="color: #333; font-size: 1rem; line-height: 1.6;">     Whether you're planning retirement or simply securing your future, this offer is tailored for residents like you.   </p>   <a href="#explore-cd-options" style="display: inline-block; margin-top: 1rem; background-color: #1a73e8; color: white; padding: 0.75rem 1.25rem; border-radius: 8px; text-decoration: none; font-weight: bold;">     Explore CD Options   </a> </div>
```

## Oferta genérica (oferta substituta)

O texto da oferta Genérico, sem nenhum código postal associado à oferta

```html
<div style="max-width: 600px; margin: 2rem auto; padding: 1.5rem; border: 1px solid #ddd; border-radius: 12px; font-family: Arial, sans-serif; background-color: #ffffff; box-shadow: 0 4px 12px rgba(0,0,0,0.05);">
  <h2 style="color: #1a237e; font-size: 1.5rem; margin-bottom: 0.5rem;">
    Invest Smarter: Build Wealth with Flexible Financial Plans
  </h2>
  <p style="color: #333; font-size: 1rem; line-height: 1.6;">
    Looking to take control of your financial future? Our flexible investment solutions are designed to meet a wide range of goals — from growing savings to planning for retirement.
    Choose from diversified mutual funds, ETFs, and professionally managed portfolios, all with expert guidance and minimal hassle.
  </p>
  <p style="color: #333; font-size: 1rem; line-height: 1.6;">
    Whether just starting out or optimizing an existing strategy, this offer provides the tools to invest with confidence — no matter where you live.
  </p>
  <a href="#explore-investment-plans" style="display: inline-block; margin-top: 1rem; background-color: #1a73e8; color: white; padding: 0.75rem 1.25rem; border-radius: 8px; text-decoration: none; font-weight: bold;">
    Explore Investment Plans
  </a>
</div>
```

Agrupe estas ofertas em uma coleção chamada **_GenericOffers_**

As ofertas estão disponíveis para todos os visitantes, o que significa que não há restrições de qualificação estritas. Em seguida, a fórmula de classificação se torna crítica para determinar qual oferta deve ser mostrada com base no contexto do perfil.
Como as regras de elegibilidade não estão filtrando as ofertas, todos os três são tratados como candidatos.
A estratégia de seleção recupera todos os três.
A fórmula de classificação os classifica com base nos atributos do perfil (como CEP e annualIncome) para escolher o melhor.



