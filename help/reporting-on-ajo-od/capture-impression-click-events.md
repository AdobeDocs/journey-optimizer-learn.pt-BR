---
title: Capturar eventos de impressões e interações
description: Capture eventos de impressão e interação e prepare os dados para relatórios no Journey Optimizer.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
recommendations: noDisplay, noCatalog
last-substantial-update: 2025-07-18T00:00:00Z
jira: KT-18526
source-git-commit: 69bc8aace3cc502a18e691584824176833413c7e
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Capturar eventos de impressões e interações

Para habilitar relatórios sobre impressões e cliques na oferta do AJO, os seguintes componentes devem ser configurados:
>[!NOTE]
>
> Esses pré-requisitos já foram concluídos na seção de criação de esquema e conjunto de dados do [tutorial anterior](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/create-schema-and-dataset)

## &#x200B;1. Conjunto de dados na Adobe Experience Platform (AEP)

- Um conjunto de dados com base em um esquema **XDM ExperienceEvent**.

O esquema deve incluir o grupo de campos `Web Details` que captura a URL da página, o referenciador, etc.

## &#x200B;2. Configuração da sequência de dados

- Um **Datastream** deve ser criado no Adobe Experience Platform.
- Essa sequência de dados deve ser vinculada ao conjunto de dados configurado acima para garantir que todos os eventos do Web SDK sejam assimilados corretamente no destino correto.

## &#x200B;3. Propriedade de tags do Adobe Experience Platform

- Extensão do AEP Web SDK configurada para usar o fluxo de dados criado na etapa anterior.
- Serviço da Experience Cloud ID configurado
- Um elemento de dados chamado ECID é adicionado à propriedade
- Implementado no site onde as ofertas são renderizadas.


Para permitir a criação de relatórios sobre o desempenho da oferta, a primeira etapa é capturar quando as ofertas são exibidas (impressões) e quando são clicadas (interações). Esses eventos fornecem a base para medir o envolvimento, calcular taxas de click-through e analisar a eficácia da oferta no Adobe Experience Platform.

A função alloy(&quot;sendEvent&quot;) é usada para registrar interações do usuário com ofertas retornadas pelo Adobe Journey Optimizer (AJO).

A carga sendEvent captura as interações de oferta incluindo o tipo de evento (decisioning.propositionDisplay para impressões ou decisioning.propositionInteract para cliques), uma ID de evento exclusiva, um carimbo de data e hora e a identidade de usuário (identityMap). Também inclui a lista de ofertas (apresentações) exibidas ou clicadas, juntamente com os tokens de rastreamento para garantir uma atribuição precisa. Essa estrutura permite a criação de relatórios e a otimização de desempenho de oferta personalizada no Adobe Journey Optimizer.

Dois tipos de eventos de interação são capturados:

## Evento de impressão

Uma impressão ocorre quando uma oferta é renderizada na página e se torna visível para o usuário. O evento é rastreado usando o tipo de evento decisioning.propositionDisplay.


```javascript
 alloy("sendEvent", {
            xdm: {
              _id: generateUUID(),
              timestamp: new Date().toISOString(),
              eventType: "decisioning.propositionDisplay",
              identityMap: {
                    ECID: [{
                      id: _satellite.getVar("ECID"),
                      authenticatedState: "authenticated",
                      primary: true
                    }]
                  },
              _experience: {
                decisioning: {
                  propositionEventType: {
                    display: 1
                  },
                  
                   propositions: window.latestPropositions
                  
                }
              }
            }
          });
        }
```

## Interação de oferta

Uma interação é registrada quando um usuário clica em uma call-to-action (CTA) dentro da oferta renderizada. O evento é rastreado usando o tipo de evento decisioning.propositionInteract.

```javascript
alloy("sendEvent", {
                xdm: {
                  _id: generateUUID(),
                  timestamp: new Date().toISOString(),
                  eventType: "decisioning.propositionInteract",
                  identityMap: {
                    ECID: [{
                      id: _satellite.getVar("ECID"),
                      authenticatedState: "ambiguous",
                      primary: true
                    }]
                  },
                  _experience: {
                    decisioning: {
                      propositionEventType: {
                        interact: 1
                      },
                      propositionAction: {
                        id: offerId,
                        tokens: [trackingToken]
                      },
                       propositions: window.latestPropositions
                    }
                  }
                }
              })
```

A inclusão de apresentações em eventos de clique e impressão é essencial para um relatório preciso das ofertas no Adobe Journey Optimizer. Essas apresentações representam as ofertas exatas que foram apresentadas ao usuário, permitindo que o Adobe atribua interações do usuário (por exemplo, impressões ou cliques) de volta às decisões específicas tomadas pelo sistema.

Cada oferta em uma proposta inclui um token de rastreamento, que é um identificador exclusivo gerado pelo Adobe. Esse token deve ser transmitido exatamente como recebido, sem alteração, no evento de clique ou impressão correspondente. Os tokens de rastreamento correspondentes garantem que o Adobe possa associar precisamente a ação do usuário à decisão de oferta correta, permitindo a geração de relatórios downstream e a otimização baseada em IA.
