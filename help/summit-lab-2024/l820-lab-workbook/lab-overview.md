---
title: Pasta de trabalho do laboratório - L820 - Crie momentos móveis personalizados com o Adobe Journey Optimizer
description: Explore vários cenários móveis e saiba como implementar experiências personalizadas para web e dispositivos móveis com o Journey Optimizer.
feature: Overview
role: User
level: Intermediate
doc-type: Tutorial
duration: 0
jira: KT-14977
thumbnail: KT-14977.jpeg
last-substantial-update: 2024-03-26T00:00:00.000Z
exl-id: e6d029f9-c936-427b-9d6e-4e296fd3c3ce
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
    internal-label: Overview
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%
---
# PASTA DE TRABALHO DO LABORATÓRIO

![Adobe Summit - texto alternativo](/help/summit-lab-2024/l820-lab-workbook/assets/adobe-summit.png "Adobe Summit")

## L820 - Crie momentos móveis personalizados com o Adobe Journey Optimizer

Neste laboratório prático, você explora vários cenários móveis e aprende a implementar experiências personalizadas para web e dispositivos móveis com o Journey Optimizer.


>[!IMPORTANT]
>
>Evite publicar fotos ou capturas de tela da sessão nas redes sociais.
><br>
>**Confidencialidade do Adobe**
>As informações e divulgações de produtos compartilhadas hoje durante este laboratório são Informações confidenciais da Adobe.
>Os participantes não podem reproduzir, utilizar, divulgar ou divulgar Informações confidenciais a qualquer pessoa ou entidade.
>As divulgações de produtos são somente para fins informativos, não são uma garantia de qualquer recurso ou funcionalidade futura e estão sujeitas a alterações a qualquer momento. Sendo assim, esses recursos ou funcionalidades do produto não fazem parte de nenhum modo de seu contrato com a Adobe ou são de outra forma comprometidos com você.
><br>
>**Aviso**
>A Adobe está fornecendo acesso antecipado aos recursos do, que aproveitam a tecnologia de IA geradora. Observe que esses recursos ainda estão em desenvolvimento e podem produzir respostas inesperadas ou imprecisas. Seus comentários são bem-vindos à medida que lançamos esse recurso no mercado.


### Principais lições

* Entenda a variedade de experiências móveis compatíveis.
* Configure uma campanha por push.
* Saiba como configurar campanhas móveis no aplicativo.
* Configurar mensagens no aplicativo da Web.
* Teste seus próprios cenários personalizados.

### Pré-requisitos

* Conheça o número do seu assento: Você pode encontrar o número do seu assento no tampo da mesa da máquina do laboratório:

![Número da vaga](/help/summit-lab-2024/l820-lab-workbook/assets/locate-seat-number.png)
Você precisa de acesso a:

* [Adobe Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-ajo-lab/journey-optimizer/home){target="_blank"} - os detalhes de logon são fornecidos durante os exercícios.
* [Fréscopa](https://dsn.adobe.com/p/adobe-summit-2024?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFub255bW91cyIsImVtYWlsIjoiYW5vbnltb3VzQGFkb2JlLmNvbSIsImlzc3VlciI6InNoYXJlZC1saW5rIiwiYXJnb24iOnsiYWNjZXNzIjoicmVhZC1wcm9qZWN0IiwicHJvamVjdElkIjoiYWRvYmUtc3VtbWl0LTIwMjQifSwiaWF0IjoxNzEwNTI0MTIwLCJleHAiOjE3MTIzMzg1MjB9.q2uGVst6HjJw8SCWl-3pViNzepkdGnNCvGqZnbbkTsY){target="_blank"}


### Entender o caso de uso

A Fréscopa, uma empresa dinâmica e inovadora, é especializada em revolucionar a experiência do café por meio de sua mistura única de serviços de assinatura de café e uma variedade diversa de produtos relacionados ao café disponíveis em seu site e aplicativo móvel. Com o compromisso de oferecer qualidade e sabor excepcionais, a Fréscopa atende aos entusiastas do café que buscam conveniência e opções premium.

O coração do negócio da Fréscopa reside nos seus serviços de subscrição de café, proporcionando aos clientes uma seleção com curadoria de grãos de alta qualidade entregues à sua porta. Esta abordagem personalizada garante que os amantes de café possam desfrutar de uma experiência fresca e deliciosa, adaptada às suas preferências.

Complementando seus serviços de assinatura, o site e aplicativo móvel da Fréscopa oferecem uma ampla gama de produtos relacionados ao café, permitindo que os clientes explorem e aprimorem seus rituais de café. De equipamentos de fabricação de cerveja a acessórios artesanais, a Fréscopa oferece um balcão único para os aficionados por café que buscam qualidade e comodidade.

O compromisso da Fréscopa com a excelência vai além de seus produtos, já que a empresa se dedica a criar uma jornada perfeita e agradável para o cliente. A combinação de tecnologias inovadoras e uma abordagem centrada no cliente coloca a Fréscopa na vanguarda da indústria cafeeira em evolução. Em essência, Fréscopa encarna a fusão de paixão e tecnologia, redefinindo a forma como os indivíduos experimentam e desfrutam de seu café. Com foco em qualidade, conveniência e ofertas personalizadas, a Fréscopa convida os entusiastas do café a embarcar em uma jornada de sabor, entregue na porta da casa.

