---
title: Importar dados de amostra do CRM para o conjunto de dados de perfil do AEP
description: Importe registros de amostra (por exemplo, com CRMID, email, renda, código postal) para validar se o AEP pode compilar corretamente esses perfis com visitantes anônimos da Web com base em identificadores compartilhados como ECID.
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18089
exl-id: 33c8c386-f417-45a8-83cf-7312d415b47a
source-git-commit: 83b23f54594b796ec528526a360c5c40164fb5cb
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 5%

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
Adicione o grupo de campos _&#x200B;**Detalhes de Consentimentos e Preferências**&#x200B;_ ao esquema. [Consentimentos e Preferências](https://experienceleague.adobe.com/pt-br/docs/experience-platform/xdm/field-groups/profile/consents) é um grupo de campos padrão para a classe Perfil Individual XDM que captura informações de consentimento e preferência de um cliente individual.As preferências armazenadas aqui determinam as preferências de comunicação no nível do canal.


![perfil-esquema](assets/finwise-profile-schema.png)

## Preparar dados de amostra

Atualize os endereços de email fictícios para os reais. Eles serão usados posteriormente ao enviar mensagens com o Adobe Journey Optimizer. Defina emailConsent como y para ativar a entrega de email para os perfis.

|   | crmId | firstName | lastName | email | fidelizarStatus | zipCode | annualIncome | emailConsent |
|---|--------|-----------|----------|-------------------------|---------------|---------|--------------|--------------|
|   | FIN001 | Alice | Wong | alice.wong@example.com | Ouro | 92128 | 120000 | y |
|   | FIN002 | Bob | Smith | bob.smith@example.com | Prata | 92126 | 85000 | y |
|   | FIN003 | Charlie | Kim | charlie.kim@example.com | Platina | 60614 | 175000 | y |
|   | FIN004 | Diana | Lee | diana.lee@example.com | Ouro | 30303 | 98000 | y |
|   | FIN005 | Ethan | Marrom | ethan.brown@example.com | Bronze | 75201 | 60000 | y |

## Assimilar o arquivo CSV

* Crie um conjunto de dados chamado **_FinWiseCustomerDataSetWithAnnualIncome_** com base no **_FinWiseProfileSchema_** criado na etapa anterior

* Navegue até Conexões -> Fontes -> Sistema local
* Selecione o **_Adicionar dados_** em Carregamento de arquivo local. Selecione o _&#x200B;**FinWiseCustomerDataSetWithAnnualIncome**&#x200B;_ como o conjunto de dados de destino.
  ![ingest-csv](assets/ingest-csv-into-dataset.png)
* Navegue até a próxima tela. Carregue o [arquivo csv](assets/finwise_profiles.csv) e verifique os mapeamentos
  ![mapeamentos](assets/mappings.png)

* Clique em Concluir para iniciar o processo de assimilação de dados

## Verificar perfil

* Navegue até Cliente ->Perfis e procure por ID de CRM do FinWise igual a FIN001 ou qualquer outro valor válido
  ![verificar-perfil](assets/verify-profiles.png)
