---
title: Criar uma página da Web para testar a solução
description: Página da Web para testar as ofertas personalizadas entregues usando a decisão.
role: User
level: Beginner
doc-type: Tutorial
feature: Decisioning
last-substantial-update: 2025-05-31T00:00:00Z
jira: KT-18188
source-git-commit: 58d2964644bc199b9db212040676d87d54f767b9
workflow-type: tm+mt
source-wordcount: '334'
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