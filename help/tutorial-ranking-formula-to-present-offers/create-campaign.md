---
title: Criar uma campanha
description: Saiba como uma campanha do AJO conecta públicos, políticas de decisão e canais para fornecer ofertas personalizadas no momento certo nos pontos de contato do cliente.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-30T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18188
exl-id: deb16dd5-23cd-495a-ac91-d22fd77f49bd
source-git-commit: 7d812f589172c5052a1e9bfcf6a99d0769a6c2c7
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 1%

---

# Criar uma campanha

Para fornecer ofertas personalizadas aos usuários na página da Web, uma campanha foi criada no Adobe Journey Optimizer e configurada com o canal correto, canal da Web. Essa configuração garante que as ofertas sejam entregues por meio de decisões em tempo real aos usuários que interagem com o site.

Nesta campanha, uma política de decisão foi definida para controlar como as ofertas são selecionadas. A política de decisão inclui uma estratégia de seleção, que consiste em:

Uma coleção de itens de oferta (por exemplo, com base em CEP ou renda),

Regras de elegibilidade que determinam quais ofertas se aplicam a um usuário e

Uma fórmula de classificação que atribui pontuações a ofertas qualificadas para priorizar as mais relevantes.

Quando um usuário conectado visita o site, uma solicitação de personalização é enviada ao AJO. Com base na identidade e nos atributos de perfil compilados do usuário (como código postal e renda anual), a política de decisão avalia todas as ofertas disponíveis. Ela aplica a estratégia de seleção e a lógica de classificação para determinar a melhor correspondência.

O resultado é um conjunto personalizado de ofertas, retornado como conteúdo do HTML e exibido ao usuário em um carrossel no site, criando uma experiência personalizada contínua em tempo real.


## Etapas de alto nível para criar uma campanha no AJO

1. **Criar uma Configuração de Canal**\
   Defina onde e como as ofertas são exibidas (por exemplo, uma página da Web com experiência baseada em código).
   - Faça logon no Jornada Otimizer
Navegue até Administração ->Canais ->Criar configuração de canal
   - **Nome**: `finwise-web-personalization`\
     Identifica essa configuração para a entrega personalizada de ofertas da Web do FinWise.

   - **Plataforma**: `Web`\
     Direcionado especificamente para navegadores da Web. Nenhum canal móvel habilitado.

   - **Tipo de experiência**: `Code-based experience`\
     As ofertas não são injetadas diretamente no DOM. Em vez disso, o AJO retorna o HTML bruto, que é analisado usando o JavaScript personalizado.

   - **URL da página**: `http://localhost:3000/formula.html`\
     O canal é configurado para uma página de teste específica usada durante o desenvolvimento.

   - **Local na Página**: `offers-div`\
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
Essa configuração usa a ECID como a identidade principal para reconhecer usuários. Quando a compilação de identidade está em vigor, a ECID é vinculada à ID do CRM para o Personalized Targeting Selecione ou crie uma política de decisão que defina a lógica da oferta.

5. **Política de decisão**


   A ação está vinculada a uma **Política de Decisão** que define como as ofertas são selecionadas e quantas ofertas são retornadas para exibição. Esta política usa uma **Estratégia de Seleção** criada anteriormente no tutorial.

   Para inserir a política de decisão, clique em **_Editar conteúdo_** nas seções Ações e em **_Editar código_** para abrir o editor de personalização.

   Selecione o ícone _&#x200B;**Política de decisão**&#x200B;_ à esquerda e clique no botão **Adicionar política de decisão** para abrir a tela **Criar política de decisão**. Forneça um nome significativo para a política de decisão e selecione o número de itens que a política de decisão deve retornar. O padrão é 1.
Clique em **_avançar_**, adicione a estratégia de seleção criada na etapa anterior à política de decisão e clique em **avançar** para concluir o processo de criação da política de decisão. Selecione a oferta substituta apropriada.

6. **Inserir Política de Decisão**

   ![editor-personalização](assets/personalization-editor.png)

   Insira a política de decisão recém-criada clicando no botão _&#x200B;**Inserir política**&#x200B;_. Isso insere um loop for no editor de personalização no lado direito.
Coloque o cursor entre cada loop na linha dois e insira o offerText navegando até a oferta aprofundando o `tenant name`


   O código Handlebars percorre as ofertas retornadas por uma política de decisão específica da Adobe Journey Optimizer e cria um `<div>` para cada oferta. Cada `<div>` usa um atributo de tags de dados com o nome interno da oferta para ajudar o grupo do carrossel e organizar ofertas por categoria para uma navegação suave. O conteúdo dentro de cada `<div>` exibe o texto de oferta personalizado, permitindo a apresentação dinâmica e segmentada visualmente de várias ofertas.


7. **Publicar a campanha**\
   Ative a campanha para começar a fornecer ofertas personalizadas em tempo real.

![img](assets/personalization-editor.png)
