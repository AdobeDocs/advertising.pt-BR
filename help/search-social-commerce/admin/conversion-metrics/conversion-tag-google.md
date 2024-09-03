---
title: Criar uma marca de conversão para  [!DNL Google Ads]
description: Saiba como criar uma tag de conversão  [!DNL Google Ads] .
feature: Conversions
exl-id: 214611f0-bd38-499e-a7de-3a5878995fb5
source-git-commit: 2c20d2138ee797b6ed2f27d9baa9eda7d413da8d
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Criar uma marca de conversão para [!DNL Google Ads]

É possível criar marcas de conversão para novas conversões a serem rastreadas para contas individuais do [!DNL Google Ads], não rastreadas no nível de uma conta de gerente.

Para gerar tags de conversão para conversões existentes, use o editor da rede de publicidade.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**, que abrirá a guia **[!UICONTROL Summary]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar").

1. Especifique as [configurações da marca de conversão](#conversion-tag-settings-google).

   1. Selecione a conta e o tipo de conversão.

   1. Clique em **[!UICONTROL Next]**.

   1. Especifique as opções de conversão.

   1. Clique em **[!UICONTROL Generate]**.

1. Copie a tag de conversão e implemente-a nos sites a partir dos quais deseja rastrear a métrica de conversão.

   Consulte &quot;Instalando a marca [!DNL Google]&quot; na ajuda do [!DNL Google Ads] para &quot;[2. Configure sua marca Google](https://support.google.com/google-ads/answer/12215519).&quot;

1. Clique em **[!UICONTROL Done].**

Depois que você adicionar as tags ao seu site e elas começarem a disparar, [!DNL Google Ads] registrará as conversões no site. O Search, Social e Commerce sincroniza as conversões diariamente. Para obter mais informações sobre os dados sincronizados, consulte &quot;[[!DNL Google Ads] dados de conversão em Pesquisa, Social e Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## Configurações da tag de conversão {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** A conta do Google Ads aplicável.

**[!UICONTROL Type of Conversion]:** O tipo de conversão a ser rastreada: *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]* ou *[!UICONTROL Clicks to your number on your mobile website]*. **Observação:** *[!UICONTROL Import conversion]* é usado para uma finalidade diferente; consulte &quot;[Criar uma ação de conversão para uma [!DNL Google Ads] conversão aprimorada para clientes potenciais](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md).&quot;

**[!UICONTROL Conversion Name]:** Um nome exclusivo para a métrica de conversão.

**\[Categoria de conversão\]:** A categoria de conversão. As categorias disponíveis variam de acordo com o tipo de conversão. Para *[!UICONTROL Calls to a phone number on your website]* e *[!UICONTROL Clicks to your number on your mobile website]*, &quot;[!UICONTROL Phone Call Lead]&quot; é selecionado por padrão.

**\[Tipo de ação\]:** Se a meta é um *[!UICONTROL Primary action used for bidding optimization]* ou um *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Como medir o [valor de cada conversão](https://support.google.com/google-ads/answer/3419241):

* *[!UICONTROL Use the same value for each conversion],*, que requer que você selecione uma moeda e insira o valor para cada conversão.

* *[!UICONTROL Use a different value for each conversion],*, que requer que você selecione uma moeda e insira um valor padrão para cada conversão. Você pode alterar o valor padrão na tag com um valor específico da transação ao implementar a tag em uma página da Web específica.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Quantas conversões contar por clique ou interação](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* ou *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** O número máximo de dias após uma interação de anúncio para a qual as conversões são registradas. Para campanhas de pesquisa, exibição e compras, a janela pode ser de 1 a 90 dias. Selecione um número ou selecione **[!UICONTROL Custom]** e insira um número.

**[!UICONTROL View Through Conversion Window]:** o número máximo de dias depois que um usuário exibe seus anúncios nos quais as conversões de view-through são registradas. Para campanhas de pesquisa, exibição e compras, a janela pode ser de 1 a 90 dias. Selecione um número ou selecione **[!UICONTROL Custom]** e insira um número.

**[!UICONTROL Attribution Model]:** [Quanto crédito cada interação de anúncio recebe](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]* ou *[!UICONTROL Last click]*. **Observação:** As ações de conversão que anteriormente usavam os modelos *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]* ou *[!UICONTROL Position based]* agora sem suporte agora usam o modelo *[!UICONTROL Data driven]*.

>[!MORELIKETHIS]
>
>* [Carregar dados de conversão offline para conversões aprimoradas](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [[!DNL Google Ads] dados de conversão em Pesquisa, Social e Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
