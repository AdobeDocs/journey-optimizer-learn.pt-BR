---
title: Configurar a estrutura de dados manualmente
description: Crie os namespaces de identidade necessários e defina a estrutura de dados da amostra Luma.
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
recommendations: noDisplay, noCatalog
source-git-commit: d82a80675230db561bc2fcb6613159bd5a898f32
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 8%

---


# Configurar dados manualmente

Nesta seção, você cria os namespaces de identidade necessários e define o [!DNL Luma] exemplo de estrutura de dados ao criar o [[!UICONTROL esquemas]](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=pt-BR).

>[!TIP]
>Assista ao tutorial em vídeo [Mapear identidades](/help/set-up-data/map-identities.md) antes de começar.

## Etapa 1: Criar namespaces de identidade

Nesta etapa, você cria namespaces de identidade para a variável [!DNL Luma] campos de identidade personalizados nomeados `loyaltyId`, `crmId`e `lumaProduct`. Os namespaces de identidade desempenham um papel essencial na criação de perfis de clientes em tempo real, já que dois valores correspondentes no mesmo namespace permitem que duas fontes de dados formem um gráfico de identidade.

Comece criando um namespace para a variável [!DNL Luma] esquema de fidelidade:

1. Na interface do usuário da Platform, acesse **[!UICONTROL Identidades]** no painel de navegação esquerdo.

1. Selecionar **[!UICONTROL Criar namespace de identidade]**.

1. Forneça os seguintes detalhes:

   | Nome de exibição | Símbolo de identidade | Tipo |
   |---|---|---|
   | `Luma Loyalty ID` | `lumaLoyalty` | [!UICONTROL ID entre dispositivos] |

1. Selecione **[!UICONTROL Criar]**.

   ![Criar namespaces](assets/createNamespace.png)

1. Crie mais dois namespaces seguindo as mesmas etapas:

   | Nome de exibição | Símbolo de identidade | Tipo |
   |---|---|---|
   | `Luma CRM ID` | `lumaCRM` | [!UICONTROL ID entre dispositivos] |
   | `Luma Product` | `lumaProduct` | [!UICONTROL Identificador de não pessoas] |

## Etapa 2: Criar esquemas

Nesta etapa, é possível definir a estrutura dos dados de amostra criando seis [[!UICONTROL esquemas]](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html):

* [[!DNL Luma Loyalty]](#create-luma-loyalty-schema)

* [[!DNL Luma Products]](#create-luma-products-schema)

* [[!DNL Luma Product Inventory Events]](#create-luma-product-inventory-event-schema)

* [[!DNL Luma CRM]](#create-luma-crm-and-luma-product-interactions-schemas)

* [[!DNL Luma Product Interactions]](#create-luma-crm-and-luma-product-interactions-schemas)

* [[!DNL Luma Test Profiles]](#create-luma-crm-and-luma-product-interactions-schemas)

>[!TIP]
>
>Assista ao tutorial em vídeo: [Criar um esquema](/help/set-up-data/create-schema.md) antes de começar.

### Criar [!DNL Luma Loyalty] [!UICONTROL Esquema] {#create-luma-loyalty-schema}

#### Criar o esquema

Comece criando o [!DNL Luma Loyalty] schema:

1. Ir para **[!UICONTROL GERENCIAMENTO DE DADOS]** > **[!UICONTROL Esquemas]** no painel de navegação esquerdo.

1. Selecionar **[!UICONTROL Criar esquema]** no canto superior direito.

1. No menu suspenso , selecione **[!UICONTROL Perfil individual XDM]**, já que você está modelando atributos de um cliente individual (pontos, status e assim por diante).

   ![Criar esquema](assets/loyaltyCreateSchema.png)

#### Adicionar grupos de campos existentes

Em seguida, é solicitado que você adicione grupos de campos ao esquema. Você deve adicionar todos os campos aos esquemas usando grupos. Você está adicionando grupos de campos existentes e deve criar um grupo de campos.

>[!NOTE]
>
>Se a variável [!UICONTROL Grupos de campos] o modal não abre automaticamente no [!UICONTROL Esquemas] página, selecione **[!UICONTROL Adicionar]** (como mostrado na imagem a seguir).

![Adicionar grupo de campos](assets/add_field_group.png)

1. No **[!UICONTROL Adicionar grupos de campos]** ative os seguintes grupos de campos:

   * **[!UICONTROL Detalhes demográficos]** para dados básicos do cliente, como nome e data de nascimento.

   * **[!UICONTROL Detalhes de contato pessoal]** para obter detalhes básicos sobre o contato, como endereço de email e número de telefone.

   * **[!UICONTROL Detalhes da Fidelidade]** para detalhes de fidelidade, como pontos, data de adesão ou status. O grupo de campos de fidelidade está muito abaixo da lista, portanto, é mais fácil pesquisá-lo.

1. Selecionar **[!UICONTROL Adicionar grupo de campos]** para adicionar todos os três grupos de campos ao schema.

   ![Selecionar grupos de campos padrão](assets/addstandardFieldGroups.png)

1. Selecione o nó superior do schema.

1. Enter `Luma Loyalty` como [!UICONTROL Nome de exibição].

#### Crie um [!UICONTROL grupo de campos]

Para ajudar a garantir a consistência nos esquemas, o Adobe recomenda gerenciar todos os identificadores de sistema em um único grupo:

1. No **[!UICONTROL Composição]** seção sob [!UICONTROL Grupos de campos], selecione **[!UICONTROL Adicionar]**.

1. Selecionar **[!UICONTROL Criar novo grupo de campos]**.

1. Adicionar `Luma Identifiers` como **[!UICONTROL Nome de exibição]**.

1. Adicionar `system identifiers for XDM Individual Profile class` como **[!UICONTROL Descrição]**.

1. Selecionar **[!UICONTROL Adicionar grupos de campos]**.

   ![Criar novo grupo de campos](assets/addnewfieldgroup.png)

#### Adicionar campos ao novo [!UICONTROL grupo de campos]

O novo grupo de campos vazio é adicionado ao esquema. Usando os botões + , é possível adicionar novos campos a qualquer local na hierarquia. Nesse caso, você deve adicionar campos no nível raiz:

1. Selecionar **[!UICONTROL +]** ao lado do nome do schema.

   Esta etapa adiciona um campo em **sua id do locatário** namespace , para gerenciar conflitos entre seus campos personalizados e quaisquer campos padrão.

1. No **[!UICONTROL Propriedades do campo]** na barra lateral, adicione os detalhes do novo campo:

   * **Nome do campo:** `systemIdentifier`

   * **[!UICONTROL Nome de exibição]:** `System Identifier`

   * **Tipo:** Objeto

   * **[!UICONTROL Atribuir grupo de campos]:** [!DNL Luma identifiers]

1. Selecionar **[!UICONTROL Aplicar]**.

   ![Adicionar Identificador de Sistema](assets/addsysteidentifier.png)

   Adicione dois campos sob a `systemIdentifier` objeto:

   | [!UICONTROL Fieldname] | [!UICONTROL Nome de exibição] | [!UICONTROL Tipo] |
   |-------------|-----------|----------|
   | `loyaltyId` | `Loyalty ID` | [!UICONTROL String] |
   | `crmId` | `CRM Id` | [!UICONTROL String] |

![campos](./assets/add_fields.png)

#### Definir identidades

Agora você tem o namespace e a variável [!DNL Luma] Esquema de fidelidade configurado. Antes de poder assimilar dados, você deve rotular os campos de identidade. Cada schema usado com [!UICONTROL Perfil do cliente em tempo real] é necessário ter uma identidade primária especificada e cada registro assimilado deve ter um valor para esse campo.

1. Defina as **identidade primária**:

   No `Luma Loyalty` schema:

   1. Selecione o `Luma Identifiers` grupo de campos.

   1. Selecione o campo `loyaltyId`.

   1. No **[!UICONTROL Propriedades do campo]**, ativar a **[!UICONTROL Identidade]** caixa.

   1. Ative o **[!UICONTROL Identidade principal]** caixa.

   1. Selecione o `Luma Loyalty Id` namespace de **[!UICONTROL Namespaces de identidade]** lista suspensa.

   1. Selecionar **[!UICONTROL Aplicar]**.

      ![identidade primária](/help/tutorial-configure-a-training-sandbox/assets/primary_identity.png)

1. Defina um **identidade secundária**:

   No `Luma Loyalty` schema:

   1. Selecione o `Luma Identifiers` grupo de campos.

   2. Selecione o campo `crmId`.

   3. No **[!UICONTROL Propriedades do campo]**, ativar a **[!UICONTROL Identidade]** caixa.

   4. Selecione o `Luma CRM Id` namespace de **[!UICONTROL Namespaces de identidade]** lista suspensa.

   5. Selecionar **[!UICONTROL Aplicar]**.

#### Ativar para perfil e salvar o esquema

1. Selecione o nó superior do schema.

1. No [!UICONTROL Propriedades do campo] habilitar **[!UICONTROL Perfil]**.

   O schema deve ter esta aparência:

   ![Esquema de fidelidade do Luma](assets/lumaloyaltyschema.png)

1. Selecione **[!UICONTROL Salvar]**.

### Criar [!DNL Luma Products] [!UICONTROL Esquema] {#create-luma-products-schema}

1. Ir para [!UICONTROL GERENCIAMENTO DE DADOS] -> **[!UICONTROL Esquemas]** no painel de navegação esquerdo.

1. Selecione o **[!UICONTROL Criar esquema]** no canto superior direito.

1. No menu suspenso , selecione **[!UICONTROL Procurar todos os tipos de esquema]**, que permite criar uma classe.

1. Selecionar **[!UICONTROL Criar nova classe].

1. Adicione o nome de exibição: `Luma Products`.

1. Atribuir classe.

1. Crie um [!UICONTROL grupo de campos]:

   * Nome de exibição: `Luma Product Info`

1. Adicione o seguinte campo à variável [!DNL Luma] [!UICONTROL Produto] Grupo de campos Informações.

   * Nome do campo: `product`

   * Nome de exibição: `Product`

   * Tipo: [!UICONTROL Objeto]

   * Grupo de campos: [!DNL Luma Product info]

1. Selecionar **[!UICONTROL Aplicar]**.

1. Adicione os seguintes campos à **[!DNL Product]** objeto:

   | [!UICONTROL Fieldname] | [!UICONTROL Nome de exibição] | [!UICONTROL Tipo] |
   |-------------|-----------|----------|
   | `sku` | `SKU` | [!UICONTROL String] |
   | `name` | `Name` | [!UICONTROL String] |
   | `category` | `Category` | [!UICONTROL String] |
   | `color` | `Color` | [!UICONTROL String] |
   | `size` | `Size` | [!UICONTROL String] |
   | `price` | `Price` | [!UICONTROL Duplo] |
   | `description` | `Description` | [!UICONTROL String] |
   | `productImageURL` | `Product Image URL` | [!UICONTROL String] |
   | `productURL` | `Product URL` | [!UICONTROL String] |
   | `stockQuantity` | `Stock Quantity` | [!UICONTROL String] |

1. Adicione o **[!UICONTROL Nome de exibição]** `Luma Products` ao schema.

1. Selecione **[!UICONTROL Salvar]**.

### Criar [!DNL Luma Product Inventory Event] [!UICONTROL Esquema] {#create-luma-product-inventory-event-schema}

1. Ir para **[!UICONTROL GERENCIAMENTO DE DADOS]** -> **[!UICONTROL Esquemas]** no painel de navegação esquerdo.

1. Selecione o **[!UICONTROL Criar esquema]** no canto superior direito.

1. No menu suspenso , selecione **[!UICONTROL Procurar todos os tipos de esquema]**.

1. Selecionar **[!UICONTROL Criar nova classe]**.

1. Adicione o nome de exibição: `Business Event`.

1. Selecionar tipo: *[!UICONTROL Série cronológica]*.

1. Atribuir classe.

1. Crie um [!UICONTROL grupo de campos]:

   * Nome de exibição: `Product Inventory Event Details`

1. Adicione o **[!UICONTROL Nome de exibição]** `Luma Product Inventory Event Schema` ao schema.

1. Adicione o seguinte campo ao grupo de campos Informações do produto Luma:

   * Nome do campo: `inventoryEvent`

   * Nome de exibição: `Inventory Event`

   * Tipo: [!UICONTROL Objeto]

   * Grupo de campos: [!DNL Product Inventory Event Details]

1. Adicione os seguintes campos à **[!DNL Product Inventory Event Details]** objeto:

   | [!UICONTROL Fieldname] | [!UICONTROL Nome de exibição] | [!UICONTROL Tipo] |
   |-------------|-----------|----------|
   | `productId` | `Product ID` | [!UICONTROL String] |
   | `sku` | `SKU` | [!UICONTROL String] |
   | `stockEventType` | `Stock Event Type` | **[!UICONTROL Enum]** com `restock` e `outOfStock` como valores |

   1. para definir a variável `stockEventType` para Enum, selecione tipo: `string`.

   1. Role para baixo até a parte inferior do **[!UICONTROL Propriedades do campo]**.

   1. Habilitar **[!UICONTROL Enum]**.

   1. Enter **[!UICONTROL values] ([!UICONTROL label)]**: `restock` (`restock`).

   1. Selecionar **[!UICONTROL Adicionar linha]**.

   1. Enter **[!UICONTROL values] ([!UICONTROL label)]**: `outOfStock` (`out of stock`).

   1. Selecionar **[!UICONTROL Aplicar]**.

      ![enum](assets/enum.png)

1. Definir `productId` campo como **[!UICONTROL identidade primária]** usar **[!DNL Luma Product namespace]**.

1. Selecione o `sku` e defina uma relação com o `product.sku` no campo **[!DNL Luma Products]** Esquema:

   1. Role para baixo até a parte inferior do **[!UICONTROL Propriedades do campo]**.

   1. Habilitar **[!UICONTROL Relação]**.

      1. **[!UICONTROL Esquema de referência]**: [!DNL Luma Products].

      1. **[!UICONTROL Namespace da identidade de referência]**: [!DNL Luma Product].
   1. Selecionar **[!UICONTROL Aplicar]**.

      O schema deve ter esta aparência:

      ![Relação SKU](assets/sku_relationship.png)


1. Ativar para **Perfil**.

1. Selecionar [!UICONTROL Salvar] para salvar o schema .

### Crie o [!DNL Luma CRM] e [!DNL Luma Product Interactions] esquemas {#create-luma-crm-and-luma-product-interactions-schemas}

Crie o seguinte [!UICONTROL esquemas]:

| [!UICONTROL Nome de exibição] | [!DNL Luma CRM] | [!DNL Luma Product Interactions] | [!DNL Luma Test Profiles] |
|  ---| ------- | ---- |----|
| **[!UICONTROL Tipo]** | [!UICONTROL Perfil individual XDM] | [!UICONTROL Evento de experiência XDM] | [!UICONTROL Perfil individual XDM] |
| **[!UICONTROL Adicionar grupo de campos existente]** | Identificadores Luma<br>Detalhes demográficos<br>Detalhes de contato pessoal | Mapa de identidade<br>Detalhes de comércio | Identificadores Luma<br>Detalhes demográficos<br>Detalhes de contato pessoal<br>Detalhes do teste de perfil |
| **[!UICONTROL Relação]** |  | *[!DNL productListItems.SKU]*:<br> Esquema de referência *[!DNL Luma Products]* <br>[!DNL Reference identity namespace] *[!DNL Luma Product]* schema |
| **[!UICONTROL Identidade principal] [!UICONTROL namespace])** | systemIdentifier.crmId<br>(ID do CRM Luma) |  | personalEmail.address<br>(Email) |
| **[!UICONTROL Identidade secundária] [!UICONTROL namespace]** | personalEmail.address (Email)<br>mobilePhone.number (Telefone) |  |
| **[!UICONTROL Ativar para perfil]** | sim | sim | sim |

## Próximas etapas

Agora que você criou a estrutura de dados, [criar conjuntos de dados e assimilar dados de amostra](/help/tutorial-configure-a-training-sandbox/manual-data-ingestion.md).