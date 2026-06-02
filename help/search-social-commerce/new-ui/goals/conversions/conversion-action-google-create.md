---
title: (Nova interface) Criar uma ação de conversão para uma  [!DNL Google Ads] conversão aprimorada para clientes potenciais
description: Saiba como criar uma ação de conversão  [!DNL Google Ads]  para uma conversão aprimorada de clientes potenciais.
feature: Conversions
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
subfeature_v2: id: d068b149-b9d1-421c-9033-a51495366ddc
source-git-commit: 0bfee2b52410b5cab8e9b3dfba35effc36fc40e1
workflow-type: tm+mt
source-wordcount: 510
ht-degree: 0%

---

# (Nova interface) Criar uma ação de conversão para uma conversão aprimorada de [!DNL Google Ads] para clientes potenciais

*recurso do Beta*

*[!DNL Google Ads]somente contas*

Você pode criar ações de conversão para [!DNL Google Ads] conversões avançadas para clientes potenciais a serem rastreados para contas [!DNL Google Ads] individuais, não conversões rastreadas no nível de uma conta de gerente.

Depois de criar a ação de conversão e implementar uma marca de rastreamento de conversão, você pode [carregar os dados de conversão offline que sua organização captura](conversions-upload-offline-enhanced-conversions.md) e atribuí-los à ação de conversão.

Suporte indisponível para contas do [!DNL Microsoft Advertising].

## Criar uma ação de conversão

1. No menu principal, clique em **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Acima da tabela de dados, clique em **[!UICONTROL Set up Conversion]**.

1. Especifique as [configurações da ação de conversão](#conversion-action-settings-google).

   1. Selecione o [!UICONTROL Setup Method] *[!UICONTROL Create Conversion]*.

   1. Selecione a conta e o tipo de conversão: *[!UICONTROL Import conversion]*.

   1. Clique em **[!UICONTROL Next]**.

   1. Especifique as opções de ação de conversão.

   1. Clique em **[!UICONTROL Review and Save]** para examinar as configurações.

   1. Clique em **[!UICONTROL Generate]**.

1. Leia informações sobre como criar uma marca de rastreamento para a conversão aprimorada de clientes potenciais e clique em **[!UICONTROL Next]**.

   Você deve criar a tag de conversão e implementá-la conforme necessário nos sites dos quais deseja rastrear a métrica de conversão. Você também precisará habilitar conversões aprimoradas para clientes potenciais e concordar com os termos e condições dos dados do cliente. Para obter instruções, consulte as [!DNL Google Ads] instruções para &quot;[Configurar a [!DNL Google] marca para conversões avançadas para clientes potenciais](https://support.google.com/google-ads/answer/11021502).&quot;

   Se você deseja rastrear os valores de conversão específicos da transação, [personalize seu trecho de evento](https://support.google.com/google-ads/answer/6095947).

1. Clique em **[!UICONTROL Close].**

## Configurações da ação de conversão {#conversion-action-settings-google}

### Seção Configurar Caminho

**[!UICONTROL Setup Method]:** O tipo de ação: *[!UICONTROL Create Conversion]*

**[!UICONTROL Platform]:** A rede de anúncios: *[!UICONTROL Google]*.

### Seção de detalhes da conversão

**[!UICONTROL Select Account]:** A conta [!DNL Google Ads] aplicável.

**[!UICONTROL Type of conversions]:** O tipo de conversão a ser rastreada: Selecione *[!UICONTROL Import conversion]*. Todos os outros tipos são usados para criar tags de rastreamento de conversão (não ações de conversão) para outros tipos de conversões.

### Seção Configurações de conversão

**[!UICONTROL Conversion Name]:** Um nome exclusivo para a ação de conversão.

**[!UICONTROL Goal Category]:** A categoria de conversão, como *Cliente potencial qualificado* ou *Inscrever-se*.

**[!UICONTROL Preferred Action optimization]:** Se a meta é *[!UICONTROL Primary action used for bidding optimization]* ou *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Conversion Value]:** Como medir o [valor de cada conversão](https://support.google.com/google-ads/answer/13064207):

* *[!UICONTROL Use the same value for each conversion],*, que requer que você selecione uma moeda e insira o valor para cada conversão.

* *[!UICONTROL Use different values for each conversion],*, que requer que você selecione uma moeda e insira um valor padrão para cada conversão. Você pode alterar o valor padrão na tag com um valor específico da transação ao implementar a tag em uma página da Web específica.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Quantas conversões contar por clique ou interação](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* ou *[!UICONTROL One (Recommended for leads, sign-ups and other conversions for which only the first interaction is valuable)]*.

**[!UICONTROL Click-Through Conversion Window]:** O número máximo de dias após uma interação de anúncio para a qual as conversões são registradas. Para campanhas de pesquisa, exibição e compras, a janela pode ser de 1 a 90 dias. Selecione um número ou selecione **[!UICONTROL Custom]** e insira um número.

**[!UICONTROL View-Through Conversion Window]:** o número máximo de dias depois que um usuário exibe seus anúncios nos quais as conversões de view-through são registradas. Para campanhas de pesquisa, exibição e compras, a janela pode ser de 1 a 90 dias. Selecione um número ou selecione **[!UICONTROL Custom]** e insira um número.

**[!UICONTROL Attribution Model]:** [O modelo de atribuição que determina quanto crédito cada interação de anúncio recebe](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]* ou *[!UICONTROL Last click]*.

>[!MORELIKETHIS]
>
>* [(Nova interface do usuário) Carregar dados de conversão offline para conversões aprimoradas](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Carregar dados de conversão offline para conversões aprimoradas](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Implementar [!DNL Google Ads] conversões aprimoradas para clientes potenciais](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
