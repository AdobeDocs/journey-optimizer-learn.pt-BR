---
source-git-commit: fc279f2ff41f624e4a6a0c4c930cedfcc2745dc5
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 3%
---
# Atividades ao vivo

## O que é

As **atividades online** permitem que você forneça atualizações contínuas e em tempo real que mantêm os clientes informados à medida que uma atividade avança, como um pedido que está sendo preparado, uma entrega em trânsito ou uma viagem. Em vez de enviar uma nova notificação para cada atualização, uma única atividade ativa é criada, atualizada e encerrada conforme a atividade evolui, mantendo a Tela de bloqueio ou a sombra da notificação do cliente sincronizada com o que está acontecendo.

O Adobe Journey Optimizer oferece suporte a atividades ativas nas duas principais plataformas móveis:

* **[Atividades do iOS Live](/help/channels/ios-live-activities.md)**: atualizações avançadas em tempo real na Tela de Bloqueio do iPhone e na Dynamic Island.
* **[Android Live Updates](/help/channels/android-live-updates.md)**: atualizações persistentes e em tempo real no sombreamento de notificação do Android.

Para configurar o Mobile SDK e usar as APIs para iniciar, atualizar e encerrar experiências online nas jornadas do cliente, consulte [Configurar atividade online](https://experienceleague.adobe.com/pt-br/docs/journey-optimizer/using/channels/live-activity/configure-live-activity/mobile-live-configuration-sdk){target="_blank"}.

## Casos de uso

Escolha atividades ativas como seu canal preferido quando precisar:

| # | Benefícios | Por que | Casos de uso de exemplo |
|---|---------|-----|-------------------|
| 1 | Principais características do progresso contínuo | As atualizações são exibidas diretamente na tela de bloqueio ou na sombra de notificação/Dynamic Island, sem que o usuário abra o aplicativo | <ul><li>Rastreamento de entrega de alimentos</li><li>Status de chamada de e-mail</li><li>Resultados de esportes ao vivo</li></ul> |
| 2 | Reduzir a fadiga da notificação | Uma única atividade é atualizada no local, em vez de acionar notificações por push repetidas | <ul><li>Preparação da ordem e estágios de entrega</li><li>Flight boarding e atualizações de portão</li></ul> |
| 3 | Contexto crítico e de vida curta | Ideal para atividades com início e término claros | <ul><li>Contagens regressivas da retirada da calçada</li><li>Sessões de treino ou temporizador</li></ul> |
| 4 | Interface nativa e visível | Usa superfícies nativas do sistema operacional (ilha dinâmica, tela de bloqueio, sombra de notificação) para obter uma experiência de alta visibilidade e baixo atrito | <ul><li>Rastreamento de pacotes</li><li>Atualizações de fila ou tempo de espera</li></ul> |

## Quando *não* usar atividades online

* Para estados de longa duração ou abertos sem um fim claro, encerre a atividade assim que o processo subjacente for concluído.
* Para conteúdo promocional ou de marketing - em vez disso, use notificações por push, mensagens no aplicativo ou cartões de conteúdo.
* Quando a cadência de atualização for muito alta - atualizações frequentes podem ser limitadas pelo SO ou fazer com que o usuário se sinta ruidoso.
* Se o seu aplicativo não for compatível com as versões mínimas do sistema operacional necessárias para as atividades do iOS Live ou atualizações do Android Live.
