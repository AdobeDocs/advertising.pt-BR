---
title: Criar uma ação de conversão para uma  [!DNL Google Ads] conversão aprimorada para clientes potenciais
description: Saiba como criar uma ação de conversão  [!DNL Google Ads]  para uma conversão aprimorada de clientes potenciais.
feature: Conversions
exl-id: faf4a6de-e82f-4afd-bda5-2602fb45aee5
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Criar uma ação de conversão para uma conversão aprimorada de [!DNL Google Ads] para clientes potenciais

*[!DNL Google Ads]somente contas*

Você pode criar ações de conversão para [!DNL Google Ads] conversões avançadas para clientes potenciais a serem rastreados para contas [!DNL Google Ads] individuais, não conversões rastreadas no nível de uma conta de gerente.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**, que abre a guia **[!UICONTROL Summary]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar").

1. Especifique as [configurações da ação de conversão](#conversion-action-settings-google).

   1. Selecione a conta e o tipo de conversão: *[!UICONTROL Import conversion]*.

   1. Clique em **[!UICONTROL Next]**.

   1. Especifique as opções de ação de conversão.

   1. Clique em **[!UICONTROL Generate]**.

1. Leia informações sobre como criar uma marca de rastreamento para a conversão aprimorada de clientes potenciais e clique em **[!UICONTROL Next]**.

   Crie a tag de conversão e implemente-a conforme necessário nos sites dos quais deseja rastrear a métrica de conversão. Para obter instruções, consulte o seguinte:

   * Para usar a marca [!DNL Google], consulte as instruções de [!DNL Google Ads] para &quot;Definir configurações de marca [!DNL Google]&quot; em &quot;[Configurar conversões avançadas para clientes potenciais com a  [!DNL Google] marca](https://support.google.com/google-ads/answer/11347292).&quot;

   * Para usar o [!DNL Google Tag Manager], consulte as instruções do [!DNL Google Ads] para &quot;Definir as configurações de marca do [!DNL Google]&quot; e &quot;Verificar sua configuração e publicar o contêiner&quot; em &quot;[Configurar conversões avançadas para clientes potenciais com o  [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11021502?#configure).&quot;

1. Clique em **[!UICONTROL Done].**

Depois de criar a ação de conversão e implementar uma tag de rastreamento de conversão, você pode fazer upload dos dados de conversão offline que sua organização captura e atribuí-los à ação de conversão. Consulte &quot;[Carregar dados de conversão offline para conversões aprimoradas](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md).&quot;

## Configurações da ação de conversão {#conversion-action-settings-google}

**[!UICONTROL Select an Account]:** A conta do Google Ads aplicável.

**[!UICONTROL Type of Conversion]:** O tipo de conversão a ser rastreada: Selecione *[!UICONTROL Import conversion]*. Todos os outros tipos são usados para criar tags de rastreamento de conversão (não ações de conversão) para outros tipos de conversões.

**[!UICONTROL Conversion Name]:** Um nome exclusivo para a ação de conversão.

**\[Categoria de conversão\]:** A categoria de conversão, como *Cliente potencial qualificado* ou *Inscrever-se*.

**\[Tipo de ação\]:** Se a meta é um *[!UICONTROL Primary action used for bidding optimization]* ou um *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Como medir o [valor de cada conversão](https://support.google.com/google-ads/answer/13064207):

* *[!UICONTROL Use the same value for each conversion],*, que requer que você selecione uma moeda e insira o valor para cada conversão.

* *[!UICONTROL Use a different value for each conversion],*, que requer que você selecione uma moeda e insira um valor padrão para cada conversão. Você pode alterar o valor padrão na tag com um valor específico da transação ao implementar a tag em uma página da Web específica.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Quantas conversões contar por clique ou interação](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* ou *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** O número máximo de dias após uma interação de anúncio para a qual as conversões são registradas. Para campanhas de pesquisa, exibição e compras, a janela pode ser de 1 a 90 dias. Selecione um número ou selecione **[!UICONTROL Custom]** e insira um número.

**[!UICONTROL View Through Conversion Window]:** o número máximo de dias depois que um usuário exibe seus anúncios nos quais as conversões de view-through são registradas. Para campanhas de pesquisa, exibição e compras, a janela pode ser de 1 a 90 dias. Selecione um número ou selecione **[!UICONTROL Custom]** e insira um número.

**[!UICONTROL Attribution Model]:** [Quanto crédito cada interação de anúncio recebe](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]* ou *[!UICONTROL Last click]*.

>[!MORELIKETHIS]
>
>* [Carregar dados de conversão offline para conversões aprimoradas](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Implementar [!DNL Google Ads] conversões aprimoradas para clientes potenciais](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
