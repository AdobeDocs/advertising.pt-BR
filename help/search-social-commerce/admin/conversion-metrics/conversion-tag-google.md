---
title: Criar uma tag de conversão para [!DNL Google Ads]
description: Saiba como criar um [!DNL Google Ads] tag de conversão.
feature: Conversions
source-git-commit: af32aea1c50edb6b22b0b15c920cb8c2dcdc37e9
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Criar uma tag de conversão para [!DNL Google Ads]

É possível criar tags de conversão para novas conversões a serem rastreadas para eventos individuais [!DNL Google Ads] contas, não rastreadas no nível de uma conta de gerente.

Para gerar tags de conversão para conversões existentes, use o editor da rede de publicidade.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar").

1. Especifique a [configurações da tag de conversão](#conversion-tag-settings-google).

   1. Selecione a conta e o tipo de conversão.

   1. Clique em **[!UICONTROL Next]**.

   1. Especifique as opções de conversão.

   1. Clique em **[!UICONTROL Generate]**.

1. Copie a tag de conversão e implemente-a nos sites a partir dos quais deseja rastrear a métrica de conversão.

   Consulte &quot;Instalar o [!DNL Google] &quot; na caixa [!DNL Google Ads] ajuda para &quot;[2. Configurar a tag do Google](https://support.google.com/google-ads/answer/12215519).&quot;

1. Clique em **[!UICONTROL Done].**

Depois de adicionar as tags ao site e elas começarem a disparar, [!DNL Google Ads] O registra conversões no site. O Search, Social e Commerce sincroniza as conversões diariamente. Para obter mais informações sobre os dados sincronizados, consulte &quot;[[!DNL Google Ads] dados de conversão no Search, Social e Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## Configurações da tag de conversão {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** A conta do Google Ads aplicável.

**[!UICONTROL Type of Conversion]:** O tipo de conversão a ser rastreado: *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]* ou *[!UICONTROL Clicks to your number on your mobile website]*.

**[!UICONTROL Conversion Name]:** Um nome exclusivo para a métrica de conversão.

**\[Categoria da meta\]:** A meta de conversão. As metas disponíveis variam de acordo com o tipo de conversão. Para *[!UICONTROL Calls to a phone number on your website]* e *[!UICONTROL Clicks to your number on your mobile website]*, &quot;[!UICONTROL Phone Call Lead]&quot; é selecionado por padrão.

**\[Tipo de ação\]:** Se a meta é um *[!UICONTROL Primary action used for bidding optimization]* ou um *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Como medir a [valor de cada conversão](https://support.google.com/google-ads/answer/3419241):

* *[!UICONTROL Use the same value for each conversion],* que requer que você selecione uma moeda e insira o valor para cada conversão.

* *[!UICONTROL Use a different value for each conversion],* que requer que você selecione uma moeda e insira um valor padrão para cada conversão. Você pode alterar o valor padrão na tag com um valor específico da transação ao implementar a tag em uma página da Web específica.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Quantas conversões devem ser contadas por clique ou interação](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* ou *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** O número máximo de dias após uma interação com anúncio para a qual as conversões são registradas. Para campanhas de pesquisa, exibição e compras, a janela pode ser de 1 a 90 dias. Selecione um número ou selecione **[!UICONTROL Custom]** e insira um número.

**[!UICONTROL View Through Conversion Window]:** O número máximo de dias depois que um usuário visualiza seus anúncios para os quais as conversões de view-through são registradas. Para campanhas de pesquisa, exibição e compras, a janela pode ser de 1 a 90 dias. Selecione um número ou selecione **[!UICONTROL Custom]** e insira um número.

**[!UICONTROL Attribution Model]:** [Quanto crédito cada interação de anúncio recebe](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]*, *[!UICONTROL Last click]*, *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]* ou *[!UICONTROL Position based]*.

>[!MORELIKETHIS]
>
>* [[!DNL Google Ads] dados de conversão no Search, Social e Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
