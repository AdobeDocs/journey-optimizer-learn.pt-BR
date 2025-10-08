---
source-git-commit: ac61c4d30929b559826b4a770fc10c26aec74830
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---
# Mensagens no aplicativo

## O que são mensagens no aplicativo?

As mensagens no aplicativo são mensagens que aparecem dentro de um aplicativo enquanto o usuário o está usando ativamente. São mensagens do tipo sobreposição que ficam na parte superior do aplicativo. Eles não aparecem na tela de bloqueio ou fora do aplicativo; em vez disso, são exibidos como banners, pop-ups ou pequenos cartões enquanto o usuário está explorando o aplicativo.

As mensagens no aplicativo são acionadas por ações ou condições específicas do usuário, como visualizar determinada página, concluir uma compra ou fazer parte de um segmento de público-alvo direcionado.


Por exemplo:

* Um jogo pode mostrar um pop-up explicando um novo recurso no momento em que o usuário o desbloqueia.
* Um aplicativo de compras pode exibir um banner com um código de cupom enquanto o usuário navega pelos itens.
* Um aplicativo de mídia social pode mostrar uma mensagem sugerindo que o usuário siga novas contas.

## Casos de uso

| **Benefícios** | **Por que** | **Exemplo de casos de uso** |
|----------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Alto engajamento do usuário | Captura usuários enquanto eles estão ativos no aplicativo, garantindo maior visibilidade e ação | <ul><li>Apresentação da integração</li><li>Anúncios de recursos</li><li>Pop-ups de suporte em tempo real</li></ul> |
| Contextualmente relevante | Permite que as mensagens sejam acionadas pelo comportamento do usuário, tornando-as oportunas e personalizadas | <ul><li> Venda adicional após o uso do recurso</li><li> Chamadas de atenção para inatividade</li><li> Mensagens de erro ou de sucesso</li></ul> |
| Entrega em tempo real | Permite comunicação imediata para atualizações críticas ou sensíveis ao tempo | <ul><li> Interrupções do sistema</li><li>Confirmações de transação</li><li>Falhas de pagamento</li></ul> |
| Nenhuma dependência em canais externos | Mantém a experiência do usuário contida em seu produto sem depender do email/SMS | <ul><li> Lembretes de conclusão do tutorial</li><li>Alertas de expiração de avaliação</li></ul> |
| Melhor potencial de conversão | As mensagens colocadas em contexto convertem melhor do que as mensagens fora da plataforma | <ul><li> Solicitações de atualização depois de atingir os limites do plano</li><li>Pesquisas no aplicativo</li></ul> |
| Personalização e segmentação | Pode ser personalizado com base nos dados do usuário ou nos eventos de aplicativo | <ul><li> Mensagens personalizadas para a camada do usuário ou o nível de atividade</li><li> Alertas específicos de função </li></ul> |
| Não-intrusivo (quando bem projetado) | Permite uma comunicação sutil e eficiente sem interromper o fluxo do usuário | <ul><li> Dicas de ferramenta</li><li>Slides-ins com atualizações</li><li>Chamadas de atenção do widget de chat</li></ul> |


## Quando *não* usar a comunicação no aplicativo

* **O usuário não está usando o aplicativo ativamente**\
  As mensagens no aplicativo não serão vistas se o usuário não estiver conectado no momento ou se não estiver interagindo com seu produto. Em vez disso, use o email ou push.
* **Problemas críticos ou sensíveis ao tempo que exigem atenção imediata**\
  Para mensagens urgentes (por exemplo, alertas de segurança, falhas de pagamento), use canais que possam alcançar o usuário fora do aplicativo, como SMS ou email.
* **Comunicações legais ou normativas**\
  As mensagens relacionadas à conformidade (por exemplo, atualizações de termos, alterações de políticas) podem exigir entrega e confirmação de leitura — mais adequado para e-mails.
* **Reativação de conta ou campanhas de retorno**\
  Se o usuário estiver inativo ou com churn, não verá as mensagens no aplicativo. Use campanhas de reengajamento por email ou notificações por push.
* **Atualizações transacionais de alto volume**\
  Notificações como atualizações de envio ou recibos geralmente são melhor enviadas por email para arquivamento e conveniência.
* **O uso excessivo leva à cegueira ou desconforto do banner**\
  Bombardear os usuários com muitas mensagens no aplicativo pode prejudicar o UX e levar à frustração ou mensagens ignoradas.
* **Nenhum cenário de conectividade/offline**\
  O aplicativo depende do usuário estar online e na sessão — não ajudará em ambientes inéditos offline.

