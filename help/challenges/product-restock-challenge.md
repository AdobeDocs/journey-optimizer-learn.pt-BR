---
title: Desafio de reposição de produto
description: Aplique o que você aprendeu sobre como criar segmentos e testar suas habilidades.
kt: 8417
feature: Segments
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 305aaf4c-7f5d-4f6f-abeb-466208f1fe48
source-git-commit: 5d9b95a5953994708686a2fbd83d0522fbbeaeb5
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 100%

---

# Desafio de reposição de produto

| Desafio | Reposição de produto |
|---|---|
| Perfil | Gerenciador de Jornadas |
| Competências necessárias | <ul><li>[Criar segmentos](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=pt-BR)</li><li> [Importar e criar conteúdo de email HTML](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/import-and-author-html-email-content.html?lang=pt-BR)</li><li>[Caso de uso - Ler segmento](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=br-PT)</li> |
| Ativos para baixar | [Arquivo de email de reabastecimento do produto](/help/challenges/assets/email-assets/ProductRestockEmail.html.zip) |

## A história

Ao navegar pelo site do Luma, os clientes podem adicionar os produtos nos quais estão interessados à uma lista de desejos, o que permite que o Luma envie aos clientes mensagens de marketing direcionadas e informações sobre os produtos.

## Seu desafio

A Luma solicita que você implemente uma jornada no Journey Optimizer que notifique os clientes que têm um item em sua lista de desejos que estava anteriormente indisponível, quando esse item estiver de volta ao estoque. A equipe criativa fornece o [Arquivo de email de reabastecimento do produto](/help/challenges/assets/email-assets/ProductRestockEmail.html.zip).

>[!BEGINTABS]

>[!TAB Tarefa]

## 1. Definir o segmento – Itens da lista de desejos esgotados

Para direcionar clientes interessados em potencial quando os produtos forem reabastecidos, crie um segmento que consista de clientes:

* Que adicionaram pelo menos um item à lista de desejos (use o tipo de evento: [!UICONTROL Commerce Salvar para mais tarde])
* Que estava esgotado nos últimos três meses (use quantidade em estoque = 0)
* e que não compraram o item desde então.

>[!TIP]
>Exclua todos os tipos de evento de compras em que o SKU corresponde ao SKU do *evento Salvar para mais tarde*. Você pode encontrar o campo na seção *Procurar variáveis*.

Nomeie este segmento: `Out-of-stock-Wishlist`


### 2. Criar a jornada – Notificação de reabastecimento do produto

Quando um item anteriormente indisponível voltar ao estoque, notifique os clientes que o adicionaram com uma chamada para comprar agora, já que o item está de volta ao estoque.

1. Chame a jornada: `Product Restock`
2. A jornada deve ser acionada quando um produto retornar ao estoque
3. Envie o *Email de reabastecimento do produto* para
4. usuários que adicionaram esse item à lista de desejos enquanto ele estava indisponível

>[!TAB Critérios de sucesso]

Teste a jornada:

1. Certifique-se de que o evento de segmento de leitura tenha o namespace = `Luma CRM ID`
1. Substitua os parâmetros de email padrão e os defina para seu próprio endereço de email (consulte email nº 1 para obter instruções)
1. Defina a jornada para o modo de teste
1. Acionar um evento - insira os seguintes dados:

   * Descrição: esqueça as máquinas sofisticadas e as associações caras - O Kit de Bandas Elásticas Harmony Lumaflex é tudo que você precisa para um exercício fantástico. O kit tem tudo que você precisa para uma gama de exercícios de fortalecimento e tonificação.
   * Nome: Kit de bandas elásticas Harmony Lumaflex
   * Preço: 22
   * ID do produto: 24-UG03
   * URL da imagem do produto: https://publish1034.adobedemo.com/content/dam/luma/en/products/gear/fitness-equipment/ug03-bk-0.jpSKU: 24-UG03
   * Tipo de evento de estoque: reabastecimento. 
   * Identificador de perfil: Jenna_Palmer9530@emailsim.io

Você deve receber o email &quot;Reposição de produto por email da Luma&quot; com os detalhes do produto e a personalização de Jenna.

>[!TAB Verifique o seu trabalho]

Esta é a aparência do seu segmento:

![Segmento - Itens indisponíveis da lista de desejos](/help/challenges/assets/C1-S2.png)


Esta deve ser a aparência da sua jornada:

![Jornada de reposição de produto](/help/challenges/assets/c3-j3-journey.png)

Condição: Na lista de desejos

![Condição - na lista de desejos](/help/challenges/assets/c3-j3-condition.png)

Código da condição:

```in(@{LumaProductRestock._wwfovlab065.sku},#{ExperiencePlatform.ExperienceEvents.experienceevent.all(currentDataPackField.eventType=="commerce.saveForLaters").productListItems.all().SKU})```


>[!TIP]
> * Selecione o SKU em Salvar para mais tarde, na seção *Procurar variáveis*
> * Use a opção de comparação ao soltar o SKU em Salvar para mais tarde, no campo evento


Verifique o código no canto inferior direito da tela Editar segmento, em Eventos. O código deve ter esta aparência:

Código:
```(Include have at least 1 Save For Laters event where ((Stock Quantity equals 0)) THENExclude all  Purchases events where ((SKU equals Save For Laters1 SKU)) ) and occurs in last 3 month(s)```

>[!ENDTABS]

### Criar email - Luma-Reposição de Produto

Notifique os clientes que adicionaram um item indisponível com uma chamada para comprar agora que o item está novamente em estoque.



>[!TIP]
>
> Use o evento comercial existente. Adicione uma condição que verifique se o SKU de reabastecimento está incluído em (algum) tipo de evento salvar para mais tarde.




