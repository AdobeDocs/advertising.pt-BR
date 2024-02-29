---
title: Fazer upload de métricas de conversão para [!DNL Google Ads]
description: Saiba como fazer upload de métricas de conversão rastreadas por pesquisa, redes sociais e comércio para [!DNL Google Ads].
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
source-git-commit: a004f5025ee94c6a40c24124a9cb134a4e1668ce
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# Fazer upload de métricas de conversão para [!DNL Google Ads]

*Anunciantes com [!DNL Google Ads] Somente contas*

Search, Social e Commerce podem, opcionalmente, fazer upload para [!DNL Google Ads] todas as métricas de conversão que ele rastreia [!DNL Google Ads] que usam o serviço de rastreamento de conversão de Adobe Advertising. Essa opção não disponibiliza as conversões para otimização híbrida. Se quiser usar suas conversões de Adobe para otimização híbrida, consulte &quot;[Habilitar carregamento de objetivos para redes de anúncios](objective-upload-to-networks.md).&quot;

Os uploads diários incluem o `gclid` , o valor de conversão definido usando o modelo de atribuição no nível do anunciante e o carimbo de data e hora. Se o modelo de atribuição for atualizado, o próximo upload usará o novo modelo, mas os dados anteriores não serão atualizados para usar o novo modelo.

>[!NOTE]
>
>Os uploads não incluem métricas de conversão enviadas para o Adobe Advertising a partir de arquivos de feed.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Marque a caixa de seleção ao lado de **[!UICONTROL Upload Conversions to Google Ads]**.

1. (Anunciantes que fazem negócios no Espaço Econômico Europeu (EEE) ou Reino Unido (Reino Unido); opcional) Se você tiver o consentimento protegido de usuários do EEE e do Reino Unido para fazer upload de seus dados para fins de publicidade, marque a caixa de seleção ao lado de **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Clique em **[!UICONTROL Save]**.

1. (Se suas conversões forem rastreadas no nível de uma conta de gerente) [Adicionar credenciais para sua conta de gerente](/help/search-social-commerce/admin/manager-accounts.md) em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Habilitar carregamento de objetivos para redes de anúncios](objective-upload-to-networks.md)
