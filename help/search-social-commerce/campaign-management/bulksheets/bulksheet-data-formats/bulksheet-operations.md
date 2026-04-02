---
title: Operações que você pode executar em bulksheets
description: Consulte informações gerais sobre adição, edição e exclusão de dados de campanha usando bulksheets.
exl-id: 17ec9307-6dfd-45cb-b8bd-d0d7fcbf2d41
feature: Search Bulksheets
TQID: https://experienceleague.adobe.com/v0lNqlMXWFmw8O1Tr51d-WoHC-X2dxdSh-ZRKIPxGQY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 381
ht-degree: 0%

---

# Operações que você pode executar em bulksheets

Você pode adicionar, editar e excluir dados da campanha em bulksheets para [redes de anúncios com suporte](../bulksheet-about.md#bulksheet-functionality-by-network).

Inclua uma linha de dados separada para cada componente da campanha (campanha, grupo de anúncios, palavra-chave ou anúncio de texto) que você deseja adicionar, editar ou excluir; ou cujas propriedades você deseja adicionar, editar ou excluir. Por exemplo, se você quiser criar uma campanha com um grupo de anúncios, uma palavra-chave e um anúncio, quatro componentes no total, serão necessárias quatro linhas de dados separadas. No entanto, para editar a [!UICONTROL Ad Group Name] de um grupo de anúncios (um componente), você precisa apenas de uma linha. Da mesma forma, para editar quatro propriedades diferentes para um grupo de anúncios (um componente), é necessário apenas uma linha.

As regras a seguir se aplicam ao trabalho com componentes de campanha e suas propriedades.

* Adicionando:

   * Para adicionar um componente, inclua todos os campos necessários para adicioná-lo, além de, opcionalmente, incluir campos para qualquer propriedade do componente.

   * Para adicionar uma propriedade para um componente existente, como [!UICONTROL Ad Group End Date] para um grupo de anúncios, inclua todos os campos necessários para editar esse componente (grupo de anúncios) mais o campo da propriedade ([!UICONTROL Ad Group End Date]).

* Para editar uma propriedade para um componente existente, inclua todos os campos necessários para editar esse componente, além do campo da propriedade.

  Se você deixar o campo de propriedade em branco, o valor existente será retido.

* Excluindo:

   * Para excluir um componente existente, inclua todos os campos necessários para editar esse componente e alterar seu status para [!UICONTROL Deleted]. Por exemplo, para excluir um grupo de anúncios [!DNL Google Ads], você deve incluir [!UICONTROL Campaign Name], [!UICONTROL Ad Group Name], [!UICONTROL Ad Group Status] com um valor de <i>[!UICONTROL Deleted]</i> e [!UICONTROL Ad Group ID].

   * ([!UICONTROL Param1], [!UICONTROL Param2] e [!UICONTROL Param3] valores somente) Para excluir um valor [!DNL paramN] existente de uma palavra-chave, inclua todos os campos necessários para editar a palavra-chave e também exclua o valor [!DNL paramN] existente inserindo o valor `[delete]` (incluindo os colchetes) no campo correspondente.

   * (Campos de propriedade permitidos) Para excluir um valor de propriedade existente para um componente, inclua todos os campos necessários para editar esse componente e também exclua o valor da propriedade inserindo o valor `[delete]` (incluindo os colchetes). Os campos permitidos incluem:

      * ([!UICONTROL Google Ads] somente) [!UICONTROL Description Line 1], [!UICONTROL Description Line 2]

      * ([!DNL Google Ads] e [!DNL Microsoft Advertising] somente) [!UICONTROL Product Scope Filter], [!UICONTROL Base URL/Final URL], [!UICONTROL Tracking Template]

>[!NOTE]
>
>Quando você inclui um valor em um campo que não é aplicável à ação, qualquer valor inserido no campo é ignorado.

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de dados de campanha usando bulksheets](../bulksheet-about.md)
>* [Formatos de arquivo de bulksheet com suporte](bulksheet-file-formats.md)
>* [Apêndice - Erros de bulksheet](../bulksheet-errors.md)
>* [Baixar/Criar um arquivo de bulksheet](../bulksheet-download.md)
