---
title: Criar uma página da Web para testar a solução
description: Página da Web para testar as ofertas personalizadas entregues usando a decisão.
role: User
level: Beginner
doc-type: Tutorial
feature: Decisioning
last-substantial-update: 2025-05-31T00:00:00.000Z
jira: KT-18188
recommendations: noDisplay, noCatalog
exl-id: 6b1eec78-153c-4ea5-acfe-2dcc6f1e6078
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: a984631b-2bae-4860-9b15-69c41a799dcb
    internal-label: APIs and SDKs
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
    internal-label: Decisioning API
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%
---
# Criar uma página da Web para testar a solução

Este aplicativo de amostra simula um fluxo de logon real no qual as credenciais do usuário são validadas no lado do servidor antes que a ID do CRM seja enviada para o Adobe Experience Platform (AEP). Um servidor Node.js local é usado para fornecer com segurança as páginas da Web, lidar com a lógica de autenticação básica e evitar restrições do navegador (como acesso de arquivo local bloqueado ou cabeçalhos CORS ausentes) que podem interferir na funcionalidade do Adobe Launch ou do Web SDK. Essa configuração garante que a experiência esteja mais próxima de um ambiente de produção real.

As ofertas personalizadas são exibidas somente depois que o usuário faz logon, momento em que a compilação de identidade entre a ID de CRM do usuário e a ECID (Experience Cloud ID) é concluída. Essa compilação de identidade garante que o Adobe Journey Optimizer (AJO) possa reconhecer o perfil com precisão e retornar ofertas direcionadas.

Após o logon bem-sucedido, uma solicitação de personalização é enviada ao AJO para recuperar as ofertas disponíveis para o usuário. Essas ofertas são retornadas como fragmentos do HTML, cada um incorporado com um atributo de tags de dados — como data-tags=&quot;ajo offer-Holiday-based-cd zip-92128 revenue-high&quot; — que inclui o nome da oferta e detalhes de segmentação como código postal e nível de renda.

Em seguida, o JavaScript analisa esses blocos de HTML e envolve cada um dentro de um contêiner de item do carrossel. Os itens estão organizados horizontalmente dentro de uma rota de carrossel, permitindo uma navegação deslizante. Os botões Anterior e Próximo (◀ e ▶) permitem que os usuários girem pelas ofertas personalizadas, uma de cada vez.

Essa configuração oferece uma experiência responsiva e personalizada, garantindo que cada usuário veja ofertas relevantes para seu perfil financeiro — somente depois que sua identidade for compilada com segurança em plataformas.

## Testar esta solução

* Crie uma pasta chamada fórmula de classificação dentro do projeto Node.js existente.

* Descompacte os [arquivos fornecidos nesta pasta de fórmulas de classificação.](assets/ranking-formula.zip)

* Execute o aplicativo navegando até a pasta e iniciando o servidor:
  * `cd ranking-formula`

  * `node server.js`


* Abra o navegador e acesse http://localhost:3000/formula.html.

* Fazer logon usando alice/pass123

Como Alice reside no código postal 92128, as ofertas personalizadas para esse local são exibidas.
