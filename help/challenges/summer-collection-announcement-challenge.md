---
title: Criar um anúncio de coleção de verão - Desafio
description: Envie um anúncio de coleta de verão a um segmento dos clientes existentes para promover a nova coleção de verão do Luma.
kt: 8109
role: User
level: Beginner
last-substantial-update: 2022-11-16T00:00:00Z
hide: true
exl-id: ae457be7-2c67-4950-a072-1d7030b0e17b
source-git-commit: 697f4e6b11e7c40be726471ab368781f32dad165
workflow-type: tm+mt
source-wordcount: '1138'
ht-degree: 2%

---

# Criar um anúncio de coleção de verão - Desafio

![Banner de anúncio da coleção de verão do AJO](/help/challenges/assets/email-assets/luma-transactional-onboarding-3.png)

| Desafio | Criar um anúncio de coleção de verão |
|---|---|
| Perfil | Gerenciador de jornadas |
| Competências necessárias | <ul><li>[Criar segmentos](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=en)</li><li> [Importar e criar conteúdo de email HTML](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-emails/import-and-author-html-email-content.html?lang=en)</li><li>[Caso de uso - Ler segmento](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=en)</li> |
| Ativos para baixar | [Arquivos de email da coleção sazonal](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip) |

## A História

A Luma, uma empresa ficcional de vestuário atlético, pretende promover a última coleta de roupas e equipamentos e impulsionar as vendas para clientes existentes. O Luma está lançando a nova coleção de verão e gostaria de direcionar especificamente segmentos de clientes diferentes.

## Seu desafio

A equipe de marketing do Luma solicita que você implemente uma campanha de marketing de coleção de verão no Journey Optimizer. Seu desafio é criar uma jornada no Journey Optimizer. Especificamente, você deve criar o segmento necessário, criar quatro mensagens e criar a jornada.


### Etapa 1: Definir o segmento - Clientes ativos

>[!BEGINTABS]

>[!TAB Tarefa]

Crie um segmento no Journey Optimizer chamado **Clientes ativos**.

* O segmento deve incluir somente clientes Luma ativos.
* Os clientes ativos são definidos como clientes que têm um nível no programa de fidelidade do Luma (prata, ouro, platina ou diamante).


>[!TAB Critérios de sucesso]

No construtor de segmentos, é possível ver o número estimado de perfis qualificados.

>[!NOTE]
>Pode levar até 24 horas para que a associação de segmentos apareça para perfis existentes, pois os perfis existentes precisam ser preenchidos retroativamente.

**Um perfil qualificado foi adicionado ao segmento:**

Você pode verificar os perfis que foram adicionados ao segmento se qualificam navegando até um dos perfis listados na visualização Detalhes do segmento.

Na página do perfil, verifique o [!UICONTROL Atributos] para confirmar que estão qualificadas: A camada deve ser prata, ouro, platina ou diamante.

![Atributos do perfil](assets/C1-S1-profile-attributes.png)

Você também pode verificar a variável [!UICONTROL Associação de segmento] guia : Seu segmento deve estar listado.

![Associação de segmento](assets/C1-S1-profile-segment-membership.png)

>[!TAB Verifique seu trabalho]

Campos de segmento: [!UICONTROL Atributos] > [!UICONTROL Perfil individual XDM] > [!UICONTROL Fidelidade] > [!UICONTROL Nível]

Esta é a aparência do seu segmento:

![Segmento - Clientes ativos](/help/challenges/assets/C1-S1.png)

O código deve ter esta aparência:

```javascript
stringCompare("equals", loyalty.tier, ["diamond", "gold", "platinum", "silver"], false)
```

>[!ENDTABS]


### Etapa 2: Criar a Jornada - Anúncio da coleção de verão

>[!BEGINTABS]

>[!TAB Tarefa]

Envie um anúncio da coleção de verão a um segmento de email dos clientes existentes que promove a nova coleção de verão do Luma.&#39;

Uma agência forneceu quatro arquivos HTML com o design dos emails: [Baixe os arquivos de email da coleção sazonal](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip)

Crie uma jornada chamada `(your name) - Summer collection announcement` com base nas seguintes orientações:

1. Enviar Luma - Novo email de anúncio de coleção sazonal para o segmento Clientes ativos Luma, mantendo 10% do público como um grupo de controle
   * Título da mensagem `(your name)_Luma New Seasonal Collection Announcement`.
   * Linha de assunto `(recipient's first name), the new Luma collection is here!`.
   * Use o arquivo HTML fornecido *SeasonalCollectionEmail.html* para o corpo do email.
2. Aguarde dois dias e envie uma mensagem de email de acompanhamento com conteúdo mais direcionado:
   * Os clientes do sexo masculino devem receber o **Email da coleção do Luma Men**
      * Título da mensagem: **(seu nome)_Coleção masculina Luma**
      * Linha de assunto: **(nome do recipient), explore as artes atléticas masculinas!**
      * Corpo do email: *MensCollectionEmail.html* para o corpo do email.
   * As mulheres devem receber o **Email da coleção de mulheres Luma**
      * Título da mensagem: **(seu nome)_Coleção de mulheres Luma**
      * Linha de assunto: **(nome do recipient), explore a coleção de mulheres da Luma!**
      * Corpo do email: *WomensCollectionEmail.html*
   * Outros clientes devem receber o **Luma - 20 % de email de coleta**
      * Título da mensagem: **(seu nome)_Luma - 20 % da coleção**
      * Linha de assunto:**(nome do recipient), aproveite 20% das vendas!**
      * Corpo do email: *20ffCollectionEmail.html*
3. Depois de enviar os emails direcionados acima, aguarde dois dias para que o email seja aberto
4. Se o email direcionado não for aberto em 2 dias, envie a variável **Luma - 20 %do email de coleta** como uma tentativa final de redirecionamento


>[!TAB Critérios de sucesso]

#### Visualizar os emails

**Mensagem de email nº 1 - Novo anúncio de coleta sazonal**

Visualize o email usando o Namespace de identidade: *Email* e o valor Identity : *Jenna_Palmer9530@emailsim.io*

* A linha de assunto deve ler-se: Jenna, a nova coleção Luma está aqui!
* O corpo do email deve corresponder ao que você viu na visualização: [Novo anúncio de coleta sazonal](/help/challenges/assets/email-assets/SeasonalCollectionEmail.html)


**Mensagem de email nº 2 - Coleção de homens Luma**

Enviar uma prova para si mesmo

* Insira seu endereço de email
* Selecione o perfil de teste: Chris_Scott1244@emailsim.io

Você deve receber um email. A linha de assunto deve ler-se &quot;Chris, explore as artes atléticas masculinas!&quot; e o corpo do email deve corresponder ao que você viu na visualização: [Coleção de Luma Men](/help/challenges/assets/email-assets/MensCollectionEmail.html)

**Mensagem de email nº 3 - Coleção de mulheres Luma**

Visualize o email usando o Namespace de identidade: *Email* e o valor Identity : *Jenna_Palmer9530@emailsim.io*

* A linha de assunto deve ler-se: *Jenna, explore a coleção de mulheres da Luma!*
* O corpo do email deve corresponder ao que você viu na visualização: [Coleção de Mulheres Luma](/help/challenges/assets/email-assets/WomensCollectionEmail.html)


**Mensagem de email nº 4 - Luma 20 % da coleta**

Visualize o email usando o Namespace de identidade: *Email* e o valor Identity : *Benny_Steer4909@emailsim.io*

* A linha de assunto deve ler-se: *Benny, aproveite 20% das vendas!*
* O corpo do email deve corresponder ao que você viu na visualização: [Luma 20 % da recolha](/help/challenges/assets/email-assets/20OOffCollectionEmail.html)

**Não se esqueça de publicar seus emails!**

#### Teste a jornada

>[!IMPORTANT]
>
>Antes de definir a jornada no modo de teste:
>
>1. Certifique-se de que a Atividade de leitura de segmento tenha o namespace definido como Email
>1. Para cada email, substitua os parâmetros padrão de Email dos emails para que eles sejam enviados para seu endereço de email:
>1. Mostre os valores ocultos clicando no símbolo dos olhos.
>1. Nos parâmetros de Email , clique no símbolo T (ativar substituição de parâmetro)

   >
   >      ![Substituir parâmetros de email](/help/challenges/assets/c3-override-email-paramters.jpg)
> 
>1. Clique no campo Endereço
>1. Na próxima tela, adicione o endereço de email entre parênteses: *yourname@yourdomain* no editor de expressão e clique em ok.

>


Teste a jornada e envie os emails para sua própria conta:

1. Coloque a jornada no modo de teste
2. Selecionar perfil único de cada vez
3. Tempo de espera: Defina o cronômetro como 120 segundos (digite-o no campo ).
4. Acionar entrada do perfil
5. Você pode testar cada ramificação usando um dos seguintes endereços de email como identificadores de perfil:
   * Feminino: Jenna Palmer: Jenna_Palmer9530@emailsim.io
   * Masculino: Chris Scott: Chris_Scott1244@emailsim.io
   * Gênero não especificado: Benny Steer: Benny_Steer4909@emailsim.io

6. Depois de acionar a entrada do perfil, você deve receber o primeiro email, o cabeçalho deve ser personalizado de acordo com o perfil escolhido.
7. A jornada deve continuar no respectivo ramo e você deve receber o email relacionado (por exemplo, se você escolher Jenna, você deve receber o email &quot;Coleção de mulheres Luma&quot;).
8. Abra o segundo email e a jornada deve terminar
9. Você pode repetir a etapa 4. - 7. para que todos os três perfis verifiquem se todas as suas ramificações estão funcionando corretamente.
10. Para testar as ocorrências de tempo limite, defina o tempo de espera como 30 segundos e acione a entrada novamente.
11. Não abra os emails recebidos (não visualize o email (!)) e deixe o tempo de espera cair.

Você deve receber os seguintes emails:

* Luma - Novo anúncio de coleta sazonal
* Dependendo do perfil de teste usado, você deve receber um dos seguintes emails:
   * Jenna: Coleção de Mulheres Luma
   * Chris: Coleção de Luma Men
   * Benny: Luma - 20% Desligado Da Coleta
* Caso não tenha aberto o segundo email: O Luma - 20% de desconto na coleta

>[!TAB Verificar o seu trabalho]

Esta é a aparência da sua jornada:

![Jornada](/help/challenges/assets/c3-j1-journey.png)

**Condição - Grupo de controle:**

![Grupo de controle](/help/challenges/assets/c3-j1-condition-control-group.png)

**Condição - Gênero:**\

![Condição - Gênero](/help/challenges/assets/c3-j1-condition-gender.png)
>[!ENDTABS]
