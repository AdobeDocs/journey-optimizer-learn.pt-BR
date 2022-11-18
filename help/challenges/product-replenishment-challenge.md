---
title: Desafio de reposição de produto
description: Aplique o que você aprendeu sobre como criar segmentos e testar suas habilidades.
kt: 8417
feature: Segments
role: User
level: Beginner
hide: true
source-git-commit: 957515149af1281d29a45b24ca499ef097656eb8
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 2%

---


# Desafio de reposição de produto

| Desafio | Reposição de Produto |
|---|---|
| Perfil | Gerenciador de jornadas |
| Competências necessárias | <ul><li>[Criar segmentos](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-segments.html?lang=en)</li><li> [Importar e criar conteúdo de email HTML](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/import-and-author-html-email-content.html?lang=en)</li><li>[Caso de uso - Ler segmento](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=en)</li> |
| Ativos para baixar | [Arquivos de email da coleção sazonal](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip) |

## A história

Ao navegar pelo site Luma, os clientes podem adicionar produtos que estão interessados em uma lista de desejos. O que permite que o Luma envie aos clientes mensagens de marketing direcionadas e informações sobre os produtos.

## Seu desafio

O Luma solicita que você implemente uma jornada no Journey Optimizer que notifique os clientes, que têm um item em sua lista de desejos que estava anteriormente indisponível, quando esse item estiver de volta no estoque.

## Definir o segmento - Itens da lista de permissões esgotados

Para direcionar clientes interessados em potencial quando os produtos forem rearmazenados, crie um segmento que consista em clientes

* Que adicionaram pelo menos um item à lista de desejos (Use o tipo de evento: [!UICONTROL Comércio Salvar para mais tarde])
* Qual **esgotado** nos últimos 3 meses (use stock quantity = 0)
* E não compraram o item desde então.

Nomeie este segmento: *seu nome - Fora do estoque*

+++**VERIFIQUE O SEU TRABALHO**

Esta é a aparência do seu segmento:

![Segmento - Itens da lista de desejos indisponíveis](/help/challenges/assets/C1-S2.png)

Clientes que adicionaram um item à lista de desejos indisponível nos últimos 3 meses:

* Evento: Salvar para mais tarde
   * Incluir pelo menos 1
   * Onde a quantidade de estoque for 0

e desde então não compraram o item:

* Exclua todos os tipos de evento de Compras, onde o SKU corresponde ao SKU do **Salvar para evento mais tarde**.

>[!TIP]
> * Selecione o SKU em Salvar para mais tarde no *Procurar variáveis* seção
> * Use a opção de comparação ao soltar o SKU em Salvar para mais tarde no campo de evento


Verifique o código no canto inferior direito da tela Editar segmento, em Eventos. O código deve ter esta aparência:

Código:
```(Include have at least 1 Save For Laters event where ((Stock Quantity equals 0)) THENExclude all  Purchases events where ((SKU equals Save For Laters1 SKU)) ) and occurs in last 3 month(s)```

+++

### Criar Email - Reposição de Produto Luma

Notifique os clientes que adicionaram um item esgotado com uma chamada para iniciar compras agora que o item está novamente em estoque.

### Criar a notificação jornada - rebloqueio de produto

Quando um item anteriormente indisponível voltar ao estoque, notifique os clientes que adicionaram um item indisponível com uma chamada para iniciar compras agora que o item está de volta ao estoque.

1. Crie uma jornada chamada &quot;seu nome_Luma - Pecado do produto
1. A jornada deve ser acionada quando um produto retornar ao estoque
1. Envie o *Reposição de Luma-Product* enviar email para
1. Usuários que adicionaram este item à lista de desejos enquanto estava indisponível

>[!TIP]
>
> Use o evento comercial existente. É necessário adicionar uma condição que verifique se o SKU de rebloqueio está incluído no tipo de evento (qualquer), exceto para mais tarde.

+++**CRITÉRIOS DE SUCESSO**

Teste a jornada:

1. Certifique-se de que o evento de qualificação de segmento tenha o Namespace = Email
1. Substitua os parâmetros de email padrão e os defina para seu próprio endereço de email (consulte email nº 1 para obter instruções)
1. Defina a jornada para o modo de teste
1. Acionar um evento - insira os seguintes dados:

   * Descrição: Esqueça as máquinas sofisticadas e as associações caras - o Harmony Lumaflex Resistth Band Kit é tudo que você precisa para um exercício fantástico. O kit tem tudo o que você precisa para uma gama de exercícios de fortalecimento e tonificação.
   * Nome: Kit de banda de força do Harmony Lumaflex
   * Preço: 22º
   * Identificação do produto: 24-UG03
   * URL da Imagem do Produto: https://publish1034.adobedemo.com/content/dam/luma/en/products/gear/fitness-equipment/ug03-bk-0.jpSKU: 24-UG03
   * Tipo de evento de estoque: refúgio
   * Identificador de perfil: Jenna_Palmer9530@emailsim.io

Você deve receber o email &quot;Reposição de produto por email do Luma&quot; com os detalhes do produto e a personalização de Jenna.

+++

+++**VERIFIQUE O SEU TRABALHO**

Esta é a aparência da sua jornada:

![Jornada de reposição de produto](/help/challenges/assets/c3-j3-journey.png)

Condição: Na lista de desejos

![Condição - na lista de desejos](/help/challenges/assets/c3-j3-condition.png)

Código da condição:

```in(@{LumaProductRestock._wwfovlab065.sku},#{ExperiencePlatform.ExperienceEvents.experienceevent.all(currentDataPackField.eventType=="commerce.saveForLaters").productListItems.all().SKU})```

+++
