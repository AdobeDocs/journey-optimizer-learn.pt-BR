---
title: Criar uma campanha
description: Saiba como uma campanha do AJO conecta públicos, políticas de decisão e canais para fornecer ofertas personalizadas no momento certo nos pontos de contato do cliente.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-30T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18258
source-git-commit: 7d812f589172c5052a1e9bfcf6a99d0769a6c2c7
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 1%

---

# Criar uma campanha

Para fornecer ofertas personalizadas aos usuários na página da Web, uma campanha foi criada no Adobe Journey Optimizer e configurada com o canal correto, canal da Web. Essa configuração garante que as ofertas sejam entregues por meio de decisões em tempo real aos usuários que interagem com o site.

Nesta campanha, uma política de decisão foi definida para controlar como as ofertas são selecionadas. A política de decisão inclui uma estratégia de seleção, que consiste em:

Uma coleção de itens de oferta (por exemplo, com base em tags relacionadas ao clima),

Regras de elegibilidade que determinam quais ofertas se aplicam a um usuário e

Uma fórmula de classificação que atribui pontuações a ofertas qualificadas para priorizar as mais relevantes.
Quando um usuário visita o site, o sistema detecta sua localização e busca a temperatura atual usando uma API meteorológica. Esses dados de temperatura são enviados para o Adobe Experience Platform por meio da Web SDK (Alloy). Com base nesses dados contextuais em tempo real, o Adobe Journey Optimizer avalia ofertas predefinidas que são marcadas para condições climáticas específicas, como quente, leve ou frio. A oferta mais relevante usando a estratégia de seleção e a fórmula de classificação é renderizada automaticamente na página da Web usando o mecanismo de decisão do Adobe, garantindo que o usuário receba conteúdo personalizado alinhado ao tempo atual em sua área.


## Etapas de alto nível para criar uma campanha no AJO

1. **Criar uma Configuração de Canal**\
   Defina onde e como as ofertas são exibidas (por exemplo, uma página da Web com experiência baseada em código).
   - Faça logon no Jornada Otimizer

     Navegue até Administração ->Canais ->Criar configuração de canal
   - **Nome**: `offers-by-weather`\
     Identifica essa configuração para a entrega personalizada de ofertas da Web.

   - **Plataforma**: `Web`\
     Direcionado especificamente para navegadores da Web. Nenhum canal móvel habilitado.

   - **Tipo de experiência**: `Code-based experience`\
     As ofertas não são injetadas diretamente no DOM. Em vez disso, o AJO retorna o HTML bruto, que é analisado usando o JavaScript personalizado.

   - **URL da página**: `https://gbedekar489.github.io/weather/weather-offers.html`\
     O canal é configurado para uma página de teste específica usada durante o desenvolvimento.

   - **Local na Página**: `offerContainer`\
     As ofertas retornadas são analisadas dinamicamente e renderizadas nesse contêiner usando lógica de front-end.

   - **Formato do conteúdo**: `HTML`\
     As ofertas são entregues como fragmentos brutos do HTML, permitindo controle total sobre o estilo, a filtragem e a exibição.


2. **Iniciar uma nova campanha**\
   Navegue até a seção Campanhas e crie uma nova campanha de marketing agendada. Nomeie a campanha apropriadamente.

3. **Adicionar ação**\
   Adicione a ação de experiência baseada em código e vincule a ação a uma configuração de canal criada anteriormente.



4. **Público-alvo**\
   Todos os visitantes (padrão).

   Tipo de identidade: ECID (Experience Cloud ID)
Essa configuração usa a ECID como a identidade principal para reconhecer usuários.


5. **Criar Política de Decisão**

   A ação está vinculada a uma **Política de Decisão** que define como as ofertas são selecionadas e quantas ofertas são retornadas para exibição. Esta política usa uma **Estratégia de Seleção** criada anteriormente no tutorial.

   Para inserir a política de decisão, clique em **_Editar conteúdo_** nas seções Ações e em **_Editar código_** para abrir o editor de personalização.

   Selecione o ícone _&#x200B;**Política de decisão**&#x200B;_ à esquerda e clique no botão **Adicionar política de decisão** para abrir a tela **Criar política de decisão**. Forneça um nome significativo para a política de decisão e selecione o número de itens que a política de decisão deve retornar. O padrão é 1.
Clique em **_avançar_**, adicione a estratégia de seleção criada na etapa anterior à política de decisão e clique em **avançar** para concluir o processo de criação da política de decisão. Nenhuma oferta substituta foi associada à política de decisão.



6. **Inserir Política de Decisão**

   ![editor-personalização](assets/personalization-editor.png)

   Insira a política de decisão recém-criada clicando no botão _&#x200B;**Inserir política**&#x200B;_. Isso insere um loop for no editor de personalização no lado direito.
Coloque o cursor entre cada loop na linha dois e insira o offerText navegando até a oferta aprofundando o `tenant name`

   O código Handlebars repete as ofertas retornadas por uma política de decisão específica no Adobe Journey Optimizer.
   ![barra de identificadores](assets/handlebar-code.png)

7. **Publicar a campanha**\
   Ative a campanha para começar a fornecer ofertas personalizadas em tempo real.


