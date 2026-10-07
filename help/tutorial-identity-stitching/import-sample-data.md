---
title: Importar dados de amostra do CRM para o conjunto de dados de perfil do AEP
description: Importe registros de amostra (por exemplo, com CRMID, email, renda, código postal) para validar se o AEP pode compilar corretamente esses perfis com visitantes anônimos da Web com base em identificadores compartilhados como ECID.
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00.000Z
recommendations: noDisplay, noCatalog
jira: KT-18089
exl-id: 33c8c386-f417-45a8-83cf-7312d415b47a
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: d2971708-e780-44bb-9e2a-72f139796afd
    internal-label: Customer
subfeature_v2:
  - id: ef9a83ca-eefa-47cf-aa34-f1a34715583a
    internal-label: Profiles
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: d4f3ee0d644b4f962763e6807f014efe132a9a05
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 4%
---
# Importar dados de amostra do CRM para o conjunto de dados de perfil do AEP

Para começar a compilação de identidade, importe dados de perfil de amostra do CRM para um conjunto de dados vinculado a um esquema habilitado para perfil no Adobe Experience Platform

## Criar um namespace personalizado

* Navegue até Cliente -> Identidades -> Criar namespace de identidade
* Selecione ID individual entre dispositivos e forneça o nome de exibição e o símbolo de identidade como mostrado na captura de tela abaixo.
  ![namespace-personalizado](assets/custom-namespace.png)

## Criar um esquema ativado por perfil

Crie um esquema de perfil individual chamado **_FinWiseProfileSchema_**. Inclua campos, como annualIncome, email, firstName, lastName e fidelizeStatus.
Adicione um campo de identidade **_crmid_** conforme mostrado. Marque o campo crmid como identidade e primário.


![perfil-esquema](assets/finwise-profile-schema.png)

## Preparar dados de amostra

Atualize os endereços de email fictícios para os reais. Eles serão usados posteriormente ao enviar mensagens com o Adobe Journey Optimizer.

|   | crmId | firstName | lastName | email | fidelizarStatus | zipCode | annualIncome |
|---|--------|-----------|----------|-------------------------|---------------|---------|--------------|
|   | FIN001 | Alice | Wong | alice.wong@example.com | Ouro | 92128 | 120000 |
|   | FIN002 | Bob | Smith | bob.smith@example.com | Prata | 92126 | 85000 |
|   | FIN003 | Charlie | Kim | charlie.kim@example.com | Platina | 60614 | 175000 |
|   | FIN004 | Diana | Lee | diana.lee@example.com | Ouro | 30303 | 98000 |
|   | FIN005 | Ethan | Marrom | ethan.brown@example.com | Bronze | 75201 | 60000 |

## Assimilar o arquivo CSV

* Crie um conjunto de dados chamado **_FinWiseCustomerDataSetWithAnnualIncome_** com base no **_FinWiseProfileSchema_** criado no anterior. Verifique se o conjunto de dados está habilitado para o perfil.

* Navegue até Conexões -> Fontes -> Sistema local
* Selecione o **_Adicionar dados_** em Carregamento de arquivo local. Selecione o _&#x200B;**FinWiseCustomerDataSetWithAnnualIncome**&#x200B;_ como o conjunto de dados de destino.
  ![ingest-csv](assets/ingest-csv-into-dataset.png)
* Navegue até a próxima tela. Carregue o [arquivo csv](assets/finwise_profiles.csv) e verifique os mapeamentos
  ![mapeamentos](assets/mappings.png)

* Clique em Concluir para iniciar o processo de assimilação de dados

## Verificar perfil

* Navegue até Cliente ->Perfis e procure por ID de CRM do FinWise igual a FIN001 ou qualquer outro valor válido
  ![verificar-perfil](assets/verify-profiles.png)
