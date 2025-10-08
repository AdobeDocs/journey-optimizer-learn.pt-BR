---
source-git-commit: ac61c4d30929b559826b4a770fc10c26aec74830
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 2%

---

# Visão geral das notificações por push

## O que são notificações por push?

**As notificações por push** são mensagens curtas que aparecem em um telefone, tablet ou computador, mesmo quando o usuário não está usando o aplicativo que as enviou. São uma maneira de os aplicativos &quot;tocarem no seu ombro&quot; e chamarem a sua atenção.

Por exemplo:

* Um aplicativo de compras pode alertá-lo sobre uma grande venda.
* Um aplicativo de entrega pode informar que seu pedido está a caminho.
* Um aplicativo da companhia aérea pode informar que seu voo está pronto para check-in.

**Importante:** o usuário precisa dar permissão (aceitação) ao aplicativo para que ele possa enviar notificações por push. Isso geralmente acontece quando o aplicativo é aberto pela primeira vez após o download ou posteriormente se o aplicativo perguntar novamente durante o uso. Sem a permissão do usuário, o aplicativo não pode enviar notificações por push para seu dispositivo.

## Casos de uso

Escolha notificações por push como seu canal de mensagens preferido quando precisar:

| # | Benefícios | Por que | Exemplo de casos de uso |
|---|---------|-----|-------------------|
| 1 | Atualizações sensíveis ao tempo | As mensagens de push podem aparecer na tela de bloqueio ou como banners, sem exigir que o usuário abra o aplicativo. | <ul><li> Alertas urgentes (interrupções de serviço, avisos de segurança)</li><li>Ofertas sensíveis ao tempo (vendas rápidas)</li><li> Atualizações em tempo real (pontuações de esportes, entrega de pedidos)</ul> |
| 2 | Reenvolvimento | O push pode trazer usuários inativos de volta para o aplicativo, fornecendo prompts personalizados e relevantes. | <ul><li> Lembretes de carrinho abandonado ou de navegação — por exemplo, &quot;Você deixou itens em seu carrinho — confira agora por 10% de desconto&quot;.</li></ul> |
| 3 | Reduza a dependência de canais mais caros | Push geralmente é gratuito para envio depois de criar a infraestrutura, ao contrário de SMS ou email, em que há custos por mensagem. | <ul><li> Use push em vez de SMS pago para atualizações frequentes.</li></ul> |
| 4 | Forneça conteúdo avançado e interativo | As APIs de push modernas permitem imagens, vídeos, ações rápidas (por exemplo, &quot;Aceitar&quot; / &quot;Recusar&quot;) ou deep links para telas de aplicativos específicas. | <ul><li>Campanhas de marketing com apelo visual</li><li>Ações rápidas do usuário sem abrir totalmente o aplicativo.</li></ul> |
| 5 | Aproveitar os recursos nativos do dispositivo | As notificações por push se integram aos recursos de SO da iOS/Android, como vibração, sons, selos e acionadores de geofencing. | <ul><li> Ofertas baseadas em localização quando perto de uma loja</li><li> Lembretes acionados em horários específicos.</li></ul> |
| 6 | Quando a aceitação for provável | O push só funciona para usuários que aceitaram explicitamente o. Se o aplicativo oferecer alto valor ou a marca já tiver confiança, as taxas de aceitação podem ser altas. | <ul><li> Aplicativos com bases de usuários fiéis</li><li> Fluxos de integração que explicam o valor das notificações.</li></ul> |

## Quando *não* usar push como canal principal

* Baixas taxas de aceitação ou resistência do usuário às notificações.
* Necessidade de conteúdo de formulário longo (o email pode ser melhor).
* Informações confidenciais ou altamente privadas (push pode ser visto em telas de bloqueio).
* A maioria dos usuários está no desktop e não no aplicativo móvel.
