---
title: Introdução ao Journey Optimizer Loyalty
description: Saiba como integrar ao Adobe Journey Optimizer Loyalty, configurar um desafio, aplicá-lo e exibi-lo, e analisar seu desempenho.
topic: Get Started
role: User
level: Beginner
doc-type: Tutorial
jira: KT-21773
last-substantial-update: 2026-07-28T00:00:00Z
source-git-commit: e168e56efe575659b5f48e97af77b899f8b6c962
workflow-type: tm+mt
source-wordcount: '1288'
ht-degree: 43%

---


# Introdução ao Journey Optimizer Loyalty

Os Desafios de Fidelidade permitem criar programas de fidelidade envolventes e gamificados que impulsionam o comportamento do cliente e aprofundam os relacionamentos com a marca. Crie desafios que recompensem os clientes por ações específicas, desde fazer compras e escrever comentários até se envolver com redes sociais e fazer referência a amigos.

## Introdução à Fidelidade

Esta seção apresenta o Journey Optimizer Loyalty, abordando o que é, onde ele se encaixa no Adobe Journey Optimizer e o ciclo de vida de desafio, da configuração à análise.

<!--
CARDS

* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/loyalty/discover-journey-optimizer-loyalty
  {description = Understand what Journey Optimizer Loyalty is, where it sits under AJO, and the challenge lifecycle.}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Discover Journey Optimizer Loyalty">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/loyalty/discover-journey-optimizer-loyalty" title="Descubra a fidelidade do Journey Optimizer" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496441/?format=jpeg&nocache=1787271612824" alt="Descubra a fidelidade do Journey Optimizer"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/loyalty/discover-journey-optimizer-loyalty" target="_blank" rel="referrer" title="Descubra a fidelidade do Journey Optimizer">Descubra a Fidelidade do Journey Optimizer</a>
                    </p>
                    <p class="is-size-6">Entenda o que é a Fidelidade do Journey Optimizer, onde ela se encaixa no AJO e o ciclo de vida de desafio.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/loyalty/discover-journey-optimizer-loyalty" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Configurar Fidelidade

Esta seção aborda a configuração única necessária antes de começar a criar desafios.


<!--
CARDS

* ./set-up-loyalty/set-up-a-loyalty-reward-provider.md
  {description = Learn how to set up a reward provider, create reward definitions, and configure reward payloads so Adobe Journey Optimizer can issue loyalty rewards through your external rewards system.}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up a loyalty reward provider">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./set-up-loyalty/set-up-a-loyalty-reward-provider.md" title="Configurar um provedor de premiação de fidelidade" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3497346/?format=jpeg&nocache=1787271613194" alt="Configurar um provedor de premiação de fidelidade"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./set-up-loyalty/set-up-a-loyalty-reward-provider.md" target="_blank" rel="referrer" title="Configurar um provedor de premiação de fidelidade">Configurar um provedor de premiação de fidelidade</a>
                    </p>
                    <p class="is-size-6">Saiba como configurar um provedor de premiação, criar definições de premiação e configurar cargas de premiação para que o Adobe Journey Optimizer possa emitir recompensas de fidelidade por meio de seu sistema de recompensas externo.</p>
                </div>
                <a href="./set-up-loyalty/set-up-a-loyalty-reward-provider.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Configurar seu desafio

Esta seção aborda a criação e a configuração de um desafio de fidelidade de ponta a ponta, incluindo tipo, estrutura e programação, tarefas e recompensas.


<!--
CARDS

* ./configure-your-challenge/set-up-a-loyalty-challenge.md
  {description = Learn how to set up a loyalty challenge by selecting the right challenge type, configuring audiences and schedules, defining participation rules, and controlling how progress is tracked and rewarded.}
* ./configure-your-challenge/create-tasks.md
  {description = Learn how to set up tasks: purchase & spend, quantities, eligible items & exclusions, and reuse.}
* ./configure-your-challenge/configure-rewards.md
  {description = Learn how to configure rewards: provider, milestone vs. completion delivery, reward types & coupons.}
* ./configure-your-challenge/create-a-challenge-and-get-insights-with-cx-enterprise-coworker.md
  {description = Learn how to use CX Enterprise Coworker to create, configure, and launch loyalty challenges using natural language, including audiences, rewards, schedules, and automated journey setup.}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up a loyalty challenge">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./configure-your-challenge/set-up-a-loyalty-challenge.md" title="Configurar um desafio de fidelidade" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496471/?format=jpeg&nocache=1787271613414" alt="Configurar um desafio de fidelidade"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./configure-your-challenge/set-up-a-loyalty-challenge.md" target="_blank" rel="referrer" title="Configurar um desafio de fidelidade">Configurar um desafio de fidelidade</a>
                    </p>
                    <p class="is-size-6">Saiba como configurar um desafio de fidelidade selecionando o tipo correto de desafio, configurando públicos e programações, definindo regras de participação e controlando como o progresso é monitorado e recompensado.</p>
                </div>
                <a href="./configure-your-challenge/set-up-a-loyalty-challenge.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Create tasks for your loyalty challenge">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./configure-your-challenge/create-tasks.md" title="Crie tarefas para seu desafio de fidelidade" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496442/?format=jpeg&nocache=1787271613396" alt="Crie tarefas para seu desafio de fidelidade"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./configure-your-challenge/create-tasks.md" target="_blank" rel="referrer" title="Crie tarefas para seu desafio de fidelidade">Crie tarefas para seu desafio de fidelidade</a>
                    </p>
                    <p class="is-size-6">Saiba como configurar tarefas: compra e gasto, quantidades, itens elegíveis e exclusões e reutilização.</p>
                </div>
                <a href="./configure-your-challenge/create-tasks.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure rewards">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./configure-your-challenge/configure-rewards.md" title="Configurar recompensas" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496481/?format=jpeg&nocache=1787271613404" alt="Configurar recompensas"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./configure-your-challenge/configure-rewards.md" target="_blank" rel="referrer" title="Configurar recompensas">Configurar recompensas</a>
                    </p>
                    <p class="is-size-6">Saiba como configurar recompensas: provedor, marco vs. entrega de conclusão, tipos de recompensa e cupons.</p>
                </div>
                <a href="./configure-your-challenge/configure-rewards.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Create a loyalty challenge and surface insights with CX Enterprise Coworker">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./configure-your-challenge/create-a-challenge-and-get-insights-with-cx-enterprise-coworker.md" title="Crie um desafio de fidelidade e insights com o CX Enterprise Co-worker" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496528/?format=jpeg&nocache=1787271613421" alt="Crie um desafio de fidelidade e insights com o CX Enterprise Co-worker"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./configure-your-challenge/create-a-challenge-and-get-insights-with-cx-enterprise-coworker.md" target="_blank" rel="referrer" title="Crie um desafio de fidelidade e insights com o CX Enterprise Co-worker">Crie um desafio de fidelidade e forneça insights com o CX Enterprise Co-worker</a>
                    </p>
                    <p class="is-size-6">Saiba como usar o CX Enterprise Co-worker para criar, configurar e iniciar desafios de fidelidade usando linguagem natural, incluindo públicos, recompensas, programações e configuração automatizada de jornadas.</p>
                </div>
                <a href="./configure-your-challenge/create-a-challenge-and-get-insights-with-cx-enterprise-coworker.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Aplicar e exibir seu desafio

Esta seção mostra como propor um desafio a seus clientes usando cartões de conteúdo e experiências baseadas em código.

<!--
CARDS

* ./apply-and-display-your-challenge/build-a-challenge-content-card.md
  {description = Learn how to build a challenge content card / code-based experience, covering opt-in and dynamic progress across the opt-in, progress, and completed stages, plus rewards and channel configuration.}
* ./apply-and-display-your-challenge/display-challenge-content-using-code-based-experience-channel.md
  {description = Learn how to use code-based experiences to promote loyalty challenges, display challenge progress, and deliver personalized content within your app using HTML or JSON.}
* ./apply-and-display-your-challenge/set-up-lifecycle-messaging-for-your-challenge.md
  {description = Learn how to configure multi-channel messaging for every stage of a loyalty challenge, from invitations and engagement messages to completion and reward notifications.}
* ./apply-and-display-your-challenge/publish-a-challenge-and-generate-a-journey.md
  {description = Learn how to publish a challenge and automatically generate a journey. Discover how challenge communications are translated into journey orchestration, review the generated journey structure, and customize it with additional conditions, decisioning, or optimization logic.}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Build a challenge content card">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./apply-and-display-your-challenge/build-a-challenge-content-card.md" title="Criar um cartão de conteúdo de desafio" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3496529/?format=jpeg&nocache=1787271613834" alt="Criar um cartão de conteúdo de desafio"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./apply-and-display-your-challenge/build-a-challenge-content-card.md" target="_blank" rel="referrer" title="Criar um cartão de conteúdo de desafio">Criar um cartão de conteúdo de desafio</a>
                    </p>
                    <p class="is-size-6">Saiba como criar um cartão de conteúdo de desafio/experiência baseada em código, que abranja a aceitação e o progresso dinâmico nos estágios de aceitação, progresso e conclusão, além de recompensas e configuração de canal.</p>
                </div>
                <a href="./apply-and-display-your-challenge/build-a-challenge-content-card.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Display challenge content using the code-based experience channel">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./apply-and-display-your-challenge/display-challenge-content-using-code-based-experience-channel.md" title="Exibir conteúdo de desafio usando o canal de experiência baseado em código" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3497465/?format=jpeg&nocache=1787271613831" alt="Exibir conteúdo de desafio usando o canal de experiência baseado em código"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./apply-and-display-your-challenge/display-challenge-content-using-code-based-experience-channel.md" target="_blank" rel="referrer" title="Exibir conteúdo de desafio usando o canal de experiência baseado em código">Exibir conteúdo de desafio usando o canal de experiência baseado em código</a>
                    </p>
                    <p class="is-size-6">Saiba como usar experiências baseadas em código para promover desafios de fidelidade, exibir o progresso do desafio e fornecer conteúdo personalizado no aplicativo usando HTML ou JSON.</p>
                </div>
                <a href="./apply-and-display-your-challenge/display-challenge-content-using-code-based-experience-channel.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up lifecycle messaging for your challenge">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./apply-and-display-your-challenge/set-up-lifecycle-messaging-for-your-challenge.md" title="Configurar mensagens de ciclo de vida para seu desafio" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3497455/?format=jpeg&nocache=1787271613823" alt="Configurar mensagens de ciclo de vida para seu desafio"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./apply-and-display-your-challenge/set-up-lifecycle-messaging-for-your-challenge.md" target="_blank" rel="referrer" title="Configurar mensagens de ciclo de vida para seu desafio">Configurar as mensagens do ciclo de vida para seu desafio</a>
                    </p>
                    <p class="is-size-6">Saiba como configurar mensagens multicanal para cada estágio de um desafio de fidelidade, de convites e mensagens de engajamento a notificações de conclusão e recompensa.</p>
                </div>
                <a href="./apply-and-display-your-challenge/set-up-lifecycle-messaging-for-your-challenge.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Publish a challenge and generate a journey">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./apply-and-display-your-challenge/publish-a-challenge-and-generate-a-journey.md" title="Publicar um desafio e gerar uma jornada" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3498577/?format=jpeg&nocache=1787271613828" alt="Publicar um desafio e gerar uma jornada"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./apply-and-display-your-challenge/publish-a-challenge-and-generate-a-journey.md" target="_blank" rel="referrer" title="Publicar um desafio e gerar uma jornada">Publicar um desafio e gerar uma jornada</a>
                    </p>
                    <p class="is-size-6">Saiba como publicar um desafio e gerar uma jornada automaticamente. Descubra como as comunicações de desafio são traduzidas em orquestração de jornadas, revise a estrutura de jornadas gerada e personalize-a com condições adicionais, decisões ou lógica de otimização.</p>
                </div>
                <a href="./apply-and-display-your-challenge/publish-a-challenge-and-generate-a-journey.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Analisar e relatar

Esta seção aborda como medir o desempenho dos desafios de fidelidade quando eles estiverem ativos.

<!--
CARDS

* ./analyze-and-report/measure-performance-with-challenge-reports.md
  {description = Learn how to use challenge reports and performance dashboards to measure participation, completion rates, revenue attribution, and overall loyalty program performance.}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Measure challenge performance with challenge reports">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="./analyze-and-report/measure-performance-with-challenge-reports.md" title="Meça o desempenho de desafios com relatórios de desafios" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3497534/?format=jpeg&nocache=1787271614112" alt="Meça o desempenho de desafios com relatórios de desafios"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="./analyze-and-report/measure-performance-with-challenge-reports.md" target="_blank" rel="referrer" title="Meça o desempenho de desafios com relatórios de desafios">Meça o desempenho de desafio com relatórios de desafio</a>
                    </p>
                    <p class="is-size-6">Saiba como usar relatórios de desafios e painéis de desempenho para medir a participação, as taxas de conclusão, a atribuição de receita e o desempenho geral do programa de fidelidade.</p>
                </div>
                <a href="./analyze-and-report/measure-performance-with-challenge-reports.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Assistir</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
