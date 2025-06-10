---
title: Crie ofertas para testar a decisão dinâmica e a classificação.
description: Um item de oferta na decisão representa uma única parte do conteúdo personalizado, como uma mensagem, imagem, promoção ou recomendação, que pode ser entregue a um usuário com base em regras e condições definidas.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18258
source-git-commit: c04a15418e31dc82597b7759386907013728bb0d
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# Criar ofertas para testar a decisão dinâmica e a classificação

Essas ofertas são projetadas para testar a decisão dinâmica e a classificação com base em entradas contextuais em tempo real (como temperatura), transmitidas pelo Adobe Web SDK (alloy(&quot;sendEvent&quot;)).

Antes de criar as ofertas, o esquema de Item de oferta foi estendido para incluir um novo campo: offerText

![offer-schema](assets/offer-schema.png).

Crie as 3 ofertas a seguir


## Oferta de clima quente (Tag:quente)

O texto da oferta para ofertas de clima quente

```html
<div data-tags="weather hot skincare sunscreen" style="border: 1px solid #e0e0e0; padding: 1.5rem; border-radius: 10px; background-color: #fff3e0;">   <h2 style="color: #e65100;">Protect Your Skin This Summer</h2>   <p>High temperatures mean high UV risk. Get <strong>20% off</strong> our dermatologist-recommended sunscreens and skin protection kits.</p>   <p>Offer valid this week only for areas with temperatures over 90°F.</p>   <a href="#" style="display:inline-block; margin-top:1rem; padding:0.75rem 1.5rem; background:#e65100; color:white; border-radius:5px; text-decoration:none;">Shop Sunscreen</a> </div>
```


## Oferta De Tempo Leve (Tag:Spring)

O texto da oferta para clima leve

```html
<div data-tags="ajo offer-mild-weather">   <h2 style="color: #2e7d32;">🌤️ Enjoy the Outdoors — Gear Up Now!</h2>   <p style="font-size: 1.1rem;">Perfect weather to be outside! Check out our selection of <strong>picnic sets, walking shoes, and fitness accessories</strong> for your next outdoor adventure.</p>   <p style="font-size: 1.1rem;">Get <strong>free shipping</strong> on all outdoor gear this week.</p>   <a href="#" style="display:inline-block;padding:0.75rem 1.5rem;background:#2e7d32;color:white;border-radius:6px;text-decoration:none;margin-top:1rem;">Explore Outdoor Picks</a> </div>
```

## Oferta de clima frio (Tag:cold)

O texto da oferta para clima frio

```html
<div class="offer-content" style="text-align: center; padding: 1rem;">   <img src="https://raw.githubusercontent.com/gbedekar489/gbedekar489.github.io/main/weather/pexels-romanp-16170.jpg"         alt="Winter clothing"         style="width: 100%; max-width: 400px; border-radius: 12px; margin-bottom: 1rem;">   <h2>Cold Weather, Hot Deals 🧤</h2>   <p>Stay warm in style with our exclusive <strong>25% off</strong> winter outerwear. From puffer jackets to wool scarves, find the perfect layers to beat the chill.</p>   <p><strong>Use code:</strong> <code>WINTER25</code> at checkout</p>   <p><em>Limited time offer. While supplies last.</em></p> </div>
```

### Criar coleção

Navegue até **_Decisão -> Catálogos ->Coleção->Criar coleção_**
Nomeie a coleção **Weather-Related-Offers**

Agrupe essas ofertas nesta coleção usando o construtor de regras.

