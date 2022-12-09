---
title: Criar um anúncio da Coleção de verão - desafio
description: Envie um anúncio da Coleção de verão a um segmento de clientes existentes para promover a nova Coleção de verão do Luma.
kt: 8109
role: User
level: Beginner
last-substantial-update: 2022-11-16T00:00:00Z
hide: true
exl-id: ae457be7-2c67-4950-a072-1d7030b0e17b
source-git-commit: f5b0529ee13067fe945e32494a164959adfd7d6c
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 2%

---

# Criar um anúncio da Coleção de verão - desafio

![Banner de anúncio da coleção de verão do AJO](/help/challenges/assets/email-assets/luma-transactional-onboarding-3.png)

| Desafio | Criar um anúncio de coleção de verão |
|---|---|
| Perfil | Gerenciador de jornadas |
| Competências necessárias | <ul><li>[Criar segmentos](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=en)</li><li> [Importar e criar conteúdo de email HTML](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-emails/import-and-author-html-email-content.html?lang=en)</li><li>[Caso de uso - Ler segmento](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=en)</li> |
| Ativos para baixar | [Arquivos de email da coleção sazonal](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip) |

## A história

A Luma, uma empresa ficcional de vestuário atlético, está promovendo a última coleta de roupas e equipamentos e impulsionando as vendas para clientes existentes. A Luma está lançando a nova Coleção de verão e gostaria de direcionar especificamente segmentos de clientes diferentes.

## Seu desafio

A equipe de marketing do Luma solicita a implementação de uma campanha de marketing da Coleção de verão no Journey Optimizer. Seu desafio é:

* Crie um segmento definindo quais perfis se qualificam para receber a promoção.
* Criar a jornada.

### Etapa 1: Definir o segmento - Clientes ativos

>[!BEGINTABS]

>[!TAB Tarefa]

#### Criar um segmento em [!DNL Journey Optimizer]

* Criar um segmento em [!DNL Journey Optimizer] chamado *Clientes ativos*.
* O segmento deve incluir somente clientes Luma ativos.
* Os clientes ativos são definidos como clientes que têm uma camada no programa de fidelidade do Luma (bronze, prata, ouro ou platina).


>[!TAB Critérios de sucesso]

No construtor de segmentos, é possível ver o número estimado de perfis qualificados. Se estiver trabalhando com os dados da sandbox de treinamento, você terá cerca de 753 perfis qualificados de 1,29 K.

>[!NOTE]
>Pode levar até 24 horas para que a associação de segmentos apareça para perfis existentes, pois os perfis existentes precisam ser preenchidos retroativamente.

**Um perfil qualificado foi adicionado ao segmento:**

Você pode verificar os perfis que foram adicionados ao segmento se qualificam navegando até um dos perfis listados na visualização de detalhes do seu segmento.

Na página do perfil, verifique o [!UICONTROL Atributos] para confirmar que estão qualificadas: A camada deve ser prata, ouro, platina ou diamante.

![Atributos do perfil](assets/C1-S1-profile-attributes.png)

Você também pode verificar a variável [!UICONTROL Associação de segmento] guia : Seu segmento deve estar listado.

![Associação de segmento](assets/C1-S1-profile-segment-membership.png)

>[!TAB Verificar o seu trabalho]

Campos de segmento: [!UICONTROL Atributos] > [!UICONTROL Perfil individual XDM] > [!UICONTROL Fidelidade] > [!UICONTROL Nível]

Esta é a aparência do seu segmento:

![Segmento - Clientes ativos](/help/challenges/assets/C1-S1.png)

O código deve ter esta aparência:

```javascript
stringCompare("equals", loyalty.tier, ["diamond", "gold", "platinum", "silver"], false)
```

>[!ENDTABS]


### Etapa 2: Criação da Jornada - Anúncio da coleção de verão

>[!BEGINTABS]

>[!TAB Tarefa]

#### Envie o anúncio da Coleção de verão

Uma agência forneceu quatro arquivos HTML com o design dos emails:

* `SeasonalCollectionEmail.html`
* Email da coleção do Luma Men
* Email da coleção de mulheres Luma
* Luma - 20 % de email de coleta

1. [Baixe os arquivos de email da coleção sazonal](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip).

2. Crie uma jornada chamada *Luma - Anúncio da Coleção de verão* com base nas seguintes orientações:

   1. Enviar *Luma - Novo anúncio da coleção de verão* e-mail para a *Clientes ativos* segmento, mantendo 10% do público-alvo como um grupo de controle
      * Título da mensagem *Luma - Anúncio da Coleção de verão*
      * Linha de assunto *(nome do recipient), a nova coleção de verão do Luma está aqui!*
      * Use o arquivo HTML fornecido `SeasonalCollectionEmail.html` para o corpo do email.
   2. Aguarde dois dias e envie uma mensagem de email de acompanhamento com conteúdo mais direcionado:
      * Os clientes do sexo masculino devem receber o **Coleção de Luma Men** email.
         * Título da mensagem: *Coleção de Luma Men*
         * Linha de assunto: *(nome do recipient), explore as artes atléticas masculinas!*
         * Corpo do email: `MensCollectionEmail.html` para o corpo do email.
      * As mulheres devem receber o **Coleção de Mulheres Luma** email.
         * Título da mensagem: *Coleção de Mulheres Luma*
         * Linha de assunto: *(nome do recipient), explore a coleção de mulheres da Luma!*
         * Corpo do email: `WomensCollectionEmail.html`
      * Outros clientes devem receber o **Luma - 20 % da recolha** email.
         * Título da mensagem: *Luma - 20 % da recolha*
         * Linha de assunto: *(nome do recipient), aproveite 20% das vendas!*
         * Corpo do email: `20OOffCollectionEmail.html`
   3. Depois de enviar os emails direcionados acima, aguarde dois dias para que o email seja aberto
   4. Se o email direcionado não for aberto em 2 dias, envie a variável **Luma - 20 %do email de coleta** como uma tentativa final de redirecionamento


>[!TAB Critérios de sucesso]

#### Visualizar os emails

**Mensagem de email nº 1 - Luma - Anúncio da coleção de verão**

Visualizar o email:

1. Adicione um perfil de teste: Louise Petti:
   1. Namespace de identidade: *ID do CRM Luma*
   2. Valor de identidade: *d1f132f9f9502bba047a6ec86c4b61f9*

Resultado:
* A linha de assunto deve ler-se: Louise, a nova coleção Luma está aqui!
* O corpo do email deve corresponder ao que você viu na visualização: [Novo anúncio de coleta sazonal](/help/challenges/assets/email-assets/SeasonalCollectionEmail.html)


**Mensagem de email nº 2 - Coleção de homens Luma**

Envie uma prova para você mesmo:

1. Adicione um perfil de teste: Stanleigh Stooke:
   1. Namespace de identidade: *ID do CRM Luma*
   1. Valor de identidade: `4f34057d9d9e792c28ba18ecae378e98`
1. Selecione o perfil de teste: Stanleigh Stooke.
1. Envie uma prova para si mesmo.

Resultado:\
Você deve receber um email. A linha de assunto deve ler-se *Stanleigh, explore as artes atléticas masculinas!* e o corpo do email deve corresponder ao que você viu na visualização: [Coleção de Luma Men](/help/challenges/assets/email-assets/MensCollectionEmail.html)

>[!NOTE]
>Pode levar alguns minutos para você receber a prova.

**Mensagem de email nº 3 - Coleção de mulheres Luma**

Visualizar o email com o perfil de teste *Louise Petti.*

* A linha de assunto deve ler-se: *Louise, explore a coleção de mulheres da Luma!*
* O corpo do email deve corresponder ao que você viu na visualização: [Coleção de Mulheres Luma](/help/challenges/assets/email-assets/WomensCollectionEmail.html)


**Mensagem de email nº 4 - Luma 20 % de desconto na coleção**

Visualizar o email com o perfil de teste *Louise Petti.*

* A linha de assunto deve ler-se: *Louise, aproveite 20% das vendas!*
* O corpo do email deve corresponder ao que você viu na visualização: [Luma 20 % da recolha](/help/challenges/assets/email-assets/20OOffCollectionEmail.html)


#### Teste a jornada

>[!IMPORTANT]
>
>Antes de definir a jornada no modo de teste:
>
>1. Certifique-se de que a variável [!UICONTROL Ler atividade do segmento] tem o namespace definido como **ID do CRM Luma (lumaCrmId)**
>1. Para cada email, substitua os parâmetros de email padrão para os emails de modo que eles sejam enviados para seu endereço de email:
   >    * Mostre os valores ocultos clicando no símbolo dos olhos.
   >    * Nos parâmetros de email, clique no símbolo T (ativar substituição de parâmetro).

      >
      >      ![Substituir parâmetros de email](/help/challenges/assets/c3-override-email-paramters.jpg)
   > 
   >    * Clique no botão [!UICONTROL Endereço] campo
   >    * Na próxima tela, adicione o endereço de email entre parênteses: `"yourname@yourdomain"` no editor de expressão e clique em ok.

>


Teste a jornada e envie os emails para sua própria conta:

1. Coloque a jornada no modo de teste.
1. Selecionar **[!UICONTROL Perfil único por vez]**.
1. Tempo de espera: Defina o cronômetro como 120 segundos (digite-o no campo ).
1. Acionar entrada do perfil
1. Você pode testar cada ramificação usando uma das seguintes opções *Ids do CRM Luma* como identificadores de perfil:
   * Feminino: Leora Dietsche, Valor de identidade:`a8f14eab3b483c2b96171b575ecd90b1`
   * Masculino: Stanleigh Stooke, Valor de identidade: `4f34057d9d9e792c28ba18ecae378e98`
   * Gênero não especificado: Louise Petti, Valor de identidade: `d1f132f9f9502bba047a6ec86c4b61f9`

1. Depois de acionar a entrada do perfil, você deve receber o primeiro email. O cabeçalho deve ser personalizado de acordo com o perfil escolhido.
1. A jornada deve continuar na respectiva ramificação e você deve receber o email relacionado (por exemplo, se você escolher *Jenna*, você deve receber a variável *Coleção de Mulheres Luma* email).
1. Abra o segundo email e a jornada deve terminar.
1. Você pode repetir a etapa 4. - 7. para que todos os três perfis verifiquem se suas ramificações estão funcionando corretamente.
1. Para testar as ocorrências de tempo limite, defina o tempo de espera como 30 segundos e acione a entrada novamente.
1. Não abra os emails recebidos (não visualize o email (!)) e deixe o tempo de espera cair.

Você deve receber os seguintes emails:

* Luma - Novo anúncio de coleta sazonal
* Dependendo do perfil de teste usado, você deve receber um dos seguintes emails:
   * Leora: Coleção de Mulheres Luma
   * Ressalto: Coleção de Luma Men
   * Louise: Luma - 20% Desligado Da Coleta
* Caso não tenha aberto o segundo email: O Luma - 20% de desconto na coleta

>[!TAB Verificar o seu trabalho]

Esta é a aparência da sua jornada:

![Jornada](/help/challenges/assets/c3-j1-journey.png)

**Condição - Grupo de controle:**

![Grupo de controle](/help/challenges/assets/c3-j1-condition-control-group.png)

**Condição - Gênero:**\

![Condição - Gênero](/help/challenges/assets/c3-j1-condition-gender.png)
>[!ENDTABS]
