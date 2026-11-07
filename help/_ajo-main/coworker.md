---
hide: true
title: CX Enterprise Coworker no Journey Optimizer
description: Saiba como a IA conversacional do Coworker ajuda a criar jornadas, simular experiências do cliente e gerenciar desafios de fidelidade no Adobe Journey Optimizer.
role: Leader, User, Developer, Admin
level: Beginner
doc-type: Catalog
duration: 0
last-substantial-update: '2026-11-03'
nudge: true
product_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: Coworker
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
role_v2:
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 57f70215cfd0c70b64679061089a853c244be391
workflow-type: tm+mt
source-wordcount: '1197'
ht-degree: 28%
---

# CX Enterprise Coworker no Journey Optimizer

Colaborador é a IA conversacional da Adobe, integrada aos aplicativos da CX Enterprise, como o Adobe Journey Optimizer. Ela aplica as práticas recomendadas do Adobe para ajudar você a trabalhar de forma eficiente e precisa. Descreva sua tarefa em linguagem simples. Você pode solicitar uma jornada de boas-vindas com um email após a inscrição e um acompanhamento três dias depois. Ou pergunte &quot;Crie uma jornada a partir dessa imagem de fluxograma carregada&quot; e o Colaborador planeje o trabalho. Ele executa tarefas em seus aplicativos Adobe conectados e apresenta os resultados para sua revisão.

Para o Journey Optimizer, isso significa menos tempo gasto configurando etapas do jornada, preparando simulações e configurando desafios de fidelidade, além de mais tempo gasto revisando e aprovando o que o Colaborador produz. Você permanece no controle em cada etapa, enquanto o Co-worker lida com o planejamento, a execução e o acompanhamento.

## Introdução ao Colaborador

Novo no Colaborador? Comece aqui para obter uma compreensão abrangente de como ele pode ajudar você a trabalhar com mais eficiência no Journey Optimizer e em outros aplicativos da CX Enterprise.

<!--
CARDS

* https://experienceleague.adobe.com/pt-br/docs/coworker/content/home
  {title = CX Enterprise Coworker guide}
  {description = A full introduction to Coworker, its capabilities, and supported applications.}
  {image = https://experienceleague.adobe.com/pt-br/media_17fc8a012fc3b7ce5ef185f0ea427262b55a3b65f.jpg?width=400&format=pjpg&optimize=medium}
  {cta = Get Started}

* https://experienceleague.adobe.com/pt-br/playlists/coworker-get-started-with-chat
  {title = What can Coworker Chat do?}
  {description = Learn how Coworker Chat uses a conversational interface to plan, execute, and complete customer experience work across Adobe and connected systems in minutes.}
  {image = https://experienceleague.adobe.com/pt-br/media_17fc8a012fc3b7ce5ef185f0ea427262b55a3b65f.jpg?width=400&format=pjpg&optimize=medium}
  {cta = Watch}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="CX Enterprise Coworker guide">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/pt-br/docs/coworker/content/home" title="Guia do CX Enterprise Coworker" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://experienceleague.adobe.com/pt-br/media_17fc8a012fc3b7ce5ef185f0ea427262b55a3b65f.jpg?width=400&format=pjpg&optimize=medium" alt="Guia do CX Enterprise Coworker"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/pt-br/docs/coworker/content/home" target="_blank" rel="referrer" title="Guia do CX Enterprise Coworker">Guia do CX Enterprise Coworker</a>
                    </p>
                    <p class="is-size-6">Uma introdução completa ao Coworker, seus recursos e aplicativos compatíveis.</p>
                </div>
                <a href="https://experienceleague.adobe.com/pt-br/docs/coworker/content/home" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Introdução</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="What can Coworker Chat do?">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/pt-br/playlists/coworker-get-started-with-chat" title="O que o chat do Coworker pode fazer?" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://experienceleague.adobe.com/pt-br/media_17fc8a012fc3b7ce5ef185f0ea427262b55a3b65f.jpg?width=400&format=pjpg&optimize=medium" alt="O que o chat do Coworker pode fazer?"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/pt-br/playlists/coworker-get-started-with-chat" target="_blank" rel="referrer" title="O que o chat do Coworker pode fazer?">O que o Chat do Colaborador pode fazer?</a>
                    </p>
                    <p class="is-size-6">Saiba como o chat do Coworker usa uma interface de conversa para planejar, executar e concluir o trabalho de experiência do cliente em minutos na Adobe e nos sistemas conectados.</p>
                </div>
                <a href="https://experienceleague.adobe.com/pt-br/playlists/coworker-get-started-with-chat" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Journey Optimizer no Colaborador

Saiba como o Colaborador transforma a maneira como você trabalha no Journey Optimizer, elaborando jornadas de prompts ou imagens, gerando conteúdo de mensagem e orientando você pelas verificações de simulação e configuração, tudo isso por meio de uma experiência de chat fácil de usar.

<!--
CARDS

* https://experienceleague.adobe.com/pt-br/docs/coworker/content/chat/use-cases/journeys/create-journey-from-natural-language
  {title = Generate journeys from natural language}
  {description = Turn a plain-language prompt into a draft Journey Optimizer journey with Coworker.}
  {image = https://images-tv.adobe.com/mpcv3/13099/3496867/2dacfe4d-cdd2-4a33-8449-1fad8a3a310d/e8788cf105924012acd2a90d56bb1845_1793746003-1920x1080.jpg}
  {cta = Watch}

* https://experienceleague.adobe.com/pt-br/docs/coworker/content/chat/use-cases/journeys/create-journey-from-image
  {title = Create a journey from an image}
  {description = Turn a flowchart image into a draft Journey Optimizer journey that you can review and edit.}
  {image = https://images-tv.adobe.com/mpcv3/13968/3504865/d8195c30-94b5-4070-859b-b9dda5515d1d/9026fe8b165e4092b602fa898bba4d6f_1792796167-1920x1080.jpg}
  {cta = Watch}

* https://experienceleague.adobe.com/pt-br/docs/coworker/content/chat/use-cases/journeys/simulate-journey-using-coworker
  {title = Simulate a journey using Coworker}
  {description = Test journey paths with generated profiles and events. Review proof messages and path coverage before publishing.}
  {image = https://images-tv.adobe.com/mpcv3/14050/3507004/d8195c30-94b5-4070-859b-b9dda5515d1d/c41211c8bf714a43bc5bd2284b6b5a28_1793746064-1920x1080.jpg}
  {cta = Watch}

* https://experienceleague.adobe.com/pt-br/docs/coworker/content/chat/use-cases/journeys/create-simulate-and-analyze-a-cross-channel-journey-with-cx-enterprise-coworker
  {title = Create, simulate, and analyze cross-channel journeys}
  {description = Build a journey with email and SMS content. Simulate its paths and identify configuration issues with Coworker.}
  {image = https://images-tv.adobe.com/mpcv3/13953/3504706/d8195c30-94b5-4070-859b-b9dda5515d1d/84c8ffc936c64926b227bea57502d15f_1792184436-1920x1080.jpg}
  {cta = Watch}

* https://experienceleague.adobe.com/en/docs/coworker/using/chat/use-cases/journeys/journey-version-comparison
  {title = Compare journey versions using Coworker}
  {description = Compare journey versions with visual comparisons and detailed summaries. Identify changes to activities, branches, and properties, and track when updates were made.}
  {image = https://images-tv.adobe.com/mpcv3/14061/3507163/d8195c30-94b5-4070-859b-b9dda5515d1d/7c8f011e10e54868b17e9fafbc38e28c_1793823976-1920x1080.jpg}
  {cta = Watch}

* https://experienceleague.adobe.com/en/docs/coworker/content/chat/use-cases/journeys/create-loyalty-challenge
  {title = Create a loyalty challenge and surface insights}
  {description = Create loyalty challenges with Coworker. Configure audiences, rewards, and schedules, then review challenge insights.}
  {image = https://images-tv.adobe.com/mpcv3/13055/3496528/d8195c30-94b5-4070-859b-b9dda5515d1d/72c3012d74bf482fbd10758d4fc08a05_1785395630-1920x1080.jpg}
  {cta = Watch}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Generate journeys from natural language">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/pt-br/docs/coworker/content/chat/use-cases/journeys/create-journey-from-natural-language" title="Gerar jornadas a partir do idioma natural" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://images-tv.adobe.com/mpcv3/13099/3496867/2dacfe4d-cdd2-4a33-8449-1fad8a3a310d/e8788cf105924012acd2a90d56bb1845_1793746003-1920x1080.jpg" alt="Gerar jornadas a partir do idioma natural"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/pt-br/docs/coworker/content/chat/use-cases/journeys/create-journey-from-natural-language" target="_blank" rel="referrer" title="Gerar jornadas a partir do idioma natural">Gerar jornadas a partir da linguagem natural</a>
                    </p>
                    <p class="is-size-6">Transforme um prompt em linguagem simples em um rascunho da jornada do Journey Optimizer com o Co-worker.</p>
                </div>
                <a href="https://experienceleague.adobe.com/pt-br/docs/coworker/content/chat/use-cases/journeys/create-journey-from-natural-language" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Create a journey from an image">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/pt-br/docs/coworker/content/chat/use-cases/journeys/create-journey-from-image" title="Criar uma jornada a partir de uma imagem" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://images-tv.adobe.com/mpcv3/13968/3504865/d8195c30-94b5-4070-859b-b9dda5515d1d/9026fe8b165e4092b602fa898bba4d6f_1792796167-1920x1080.jpg" alt="Criar uma jornada a partir de uma imagem"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/pt-br/docs/coworker/content/chat/use-cases/journeys/create-journey-from-image" target="_blank" rel="referrer" title="Criar uma jornada a partir de uma imagem">Criar uma jornada a partir de uma imagem</a>
                    </p>
                    <p class="is-size-6">Transforme uma imagem de fluxograma em uma jornada de rascunho do Journey Optimizer que você pode revisar e editar.</p>
                </div>
                <a href="https://experienceleague.adobe.com/pt-br/docs/coworker/content/chat/use-cases/journeys/create-journey-from-image" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Simulate a journey using Coworker">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/pt-br/docs/coworker/content/chat/use-cases/journeys/simulate-journey-using-coworker" title="Simular uma jornada usando o Colaborador" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://images-tv.adobe.com/mpcv3/14050/3507004/d8195c30-94b5-4070-859b-b9dda5515d1d/c41211c8bf714a43bc5bd2284b6b5a28_1793746064-1920x1080.jpg" alt="Simular uma jornada usando o Colaborador"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/pt-br/docs/coworker/content/chat/use-cases/journeys/simulate-journey-using-coworker" target="_blank" rel="referrer" title="Simular uma jornada usando o Colaborador">Simular uma jornada usando o Colaborador</a>
                    </p>
                    <p class="is-size-6">Testar caminhos de jornadas com perfis e eventos gerados. Revise as mensagens de prova e a cobertura de caminho antes de publicar.</p>
                </div>
                <a href="https://experienceleague.adobe.com/pt-br/docs/coworker/content/chat/use-cases/journeys/simulate-journey-using-coworker" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Create, simulate, and analyze cross-channel journeys">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/pt-br/docs/coworker/content/chat/use-cases/journeys/create-simulate-and-analyze-a-cross-channel-journey-with-cx-enterprise-coworker" title="Criar, simular e analisar jornadas entre canais" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://images-tv.adobe.com/mpcv3/13953/3504706/d8195c30-94b5-4070-859b-b9dda5515d1d/84c8ffc936c64926b227bea57502d15f_1792184436-1920x1080.jpg" alt="Criar, simular e analisar jornadas entre canais"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/pt-br/docs/coworker/content/chat/use-cases/journeys/create-simulate-and-analyze-a-cross-channel-journey-with-cx-enterprise-coworker" target="_blank" rel="referrer" title="Criar, simular e analisar jornadas entre canais">Criar, simular e analisar jornadas entre canais</a>
                    </p>
                    <p class="is-size-6">Crie uma jornada com conteúdo de email e SMS. Simule seus caminhos e identifique problemas de configuração com o Co-worker.</p>
                </div>
                <a href="https://experienceleague.adobe.com/pt-br/docs/coworker/content/chat/use-cases/journeys/create-simulate-and-analyze-a-cross-channel-journey-with-cx-enterprise-coworker" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Compare journey versions using Coworker">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/coworker/using/chat/use-cases/journeys/journey-version-comparison" title="Comparar versões do jornada usando o Colaborador" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://images-tv.adobe.com/mpcv3/14061/3507163/d8195c30-94b5-4070-859b-b9dda5515d1d/7c8f011e10e54868b17e9fafbc38e28c_1793823976-1920x1080.jpg" alt="Comparar versões do jornada usando o Colaborador"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/coworker/using/chat/use-cases/journeys/journey-version-comparison" target="_blank" rel="referrer" title="Comparar versões do jornada usando o Colaborador">Comparar versões do jornada usando o Colaborador</a>
                    </p>
                    <p class="is-size-6">Compare as versões do jornada com comparações visuais e resumos detalhados. Identifique alterações em atividades, ramificações e propriedades e acompanhe quando as atualizações foram feitas.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/coworker/using/chat/use-cases/journeys/journey-version-comparison" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Create a loyalty challenge and surface insights">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/coworker/content/chat/use-cases/journeys/create-loyalty-challenge" title="Criar um desafio de fidelidade e insights de superfície" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://images-tv.adobe.com/mpcv3/13055/3496528/d8195c30-94b5-4070-859b-b9dda5515d1d/72c3012d74bf482fbd10758d4fc08a05_1785395630-1920x1080.jpg" alt="Criar um desafio de fidelidade e insights de superfície"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/coworker/content/chat/use-cases/journeys/create-loyalty-challenge" target="_blank" rel="referrer" title="Criar um desafio de fidelidade e insights de superfície">Criar um desafio de fidelidade e insights de superfície</a>
                    </p>
                    <p class="is-size-6">Crie desafios de fidelidade com o Colaborador. Configure públicos, recompensas e cronogramas e, em seguida, analise insights de desafio.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/coworker/content/chat/use-cases/journeys/create-loyalty-challenge" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

>[!AVAILABILITY]
>
>O gerenciamento de desafio de fidelidade exige o direito do Adobe Journey Optimizer Loyalty. Entre em contato com a equipe de conta da Adobe se precisar de acesso.
