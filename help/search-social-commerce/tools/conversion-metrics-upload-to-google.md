---
title: Carregar métricas de conversão rastreadas por Commerce, Social e Pesquisa para [!DNL Google Ads]
description: Saiba como carregar métricas de conversão rastreadas por Search, Social e Commerce para  [!DNL Google Ads].
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Carregar métricas de conversão rastreadas por Commerce, Social e Pesquisa para [!DNL Google Ads]

*Somente anunciantes com contas [!DNL Google Ads] e controle de conversão do Adobe Advertising*

Como opção, o Search, Social e Commerce pode carregar [!DNL Google Ads] todas as métricas de conversão que ele rastrear para [!DNL Google Ads] campanhas que usam o serviço de rastreamento de conversão da Adobe Advertising. Essa opção não disponibiliza as conversões para otimização híbrida. Se você quiser usar suas conversões do Adobe para otimização híbrida, consulte &quot;[Habilitar carregamento de objetivos para redes de anúncios](objective-upload-to-networks.md).&quot;

Os uploads diários incluem o valor `gclid` rastreado, o valor de conversão definido com o modelo de atribuição no nível do anunciante e o carimbo de data/hora. Se o modelo de atribuição for atualizado, o próximo upload usará o novo modelo, mas os dados anteriores não serão atualizados para usar o novo modelo.

>[!NOTE]
>
>Os uploads não incluem métricas de conversão enviadas para o Adobe Advertising a partir de arquivos de feed.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Marque a caixa de seleção ao lado de **[!UICONTROL Upload Conversions to Google Ads]**.

1. (Anunciantes que fazem negócios no Espaço Econômico Europeu (EEE) ou Reino Unido (Reino Unido); opcional) Se você coletou o consentimento de usuários do EEE e do Reino Unido para carregar seus dados para fins de publicidade, marque a caixa de seleção ao lado de **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Clique em **[!UICONTROL Save]**.

1. (Se suas conversões forem rastreadas no nível de uma conta de gerente) [Adicionar credenciais para sua conta de gerente](/help/search-social-commerce/admin/manager-accounts.md) em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Habilitar carregamento de objetivos em redes de anúncios](objective-upload-to-networks.md)
