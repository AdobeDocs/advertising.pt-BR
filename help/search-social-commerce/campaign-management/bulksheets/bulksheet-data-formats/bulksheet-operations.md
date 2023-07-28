---
title: Operações que você pode executar em bulksheets
description: Consulte informações gerais sobre adição, edição e exclusão de dados de campanha usando bulksheets.
exl-id: 82969bb8-dff8-48e7-b37d-1446a2a90072
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Operações que você pode executar em bulksheets

É possível adicionar, editar e excluir dados de campanha por meio de bulksheets para [redes de publicidade suportadas](../bulksheet-about.md#bulksheet-functionality-by-network).

Inclua uma linha de dados separada para cada componente da campanha (campanha, grupo de anúncios, palavra-chave ou anúncio de texto) que você deseja adicionar, editar ou excluir; ou cujas propriedades você deseja adicionar, editar ou excluir. Por exemplo, se você quiser criar uma campanha com um grupo de anúncios, uma palavra-chave e um anúncio, quatro componentes no total, serão necessárias quatro linhas de dados separadas. Para editar a variável [!UICONTROL Ad Group Name] para um grupo de anúncios (um componente), no entanto, você precisa de apenas uma linha. Da mesma forma, para editar quatro propriedades diferentes para um grupo de anúncios (um componente), é necessário apenas uma linha.

As regras a seguir se aplicam ao trabalho com componentes de campanha e suas propriedades.

* Adicionando:

   * Para adicionar um componente, inclua todos os campos necessários para adicioná-lo, além de, opcionalmente, incluir campos para qualquer propriedade do componente.

   * Para adicionar uma propriedade a um componente existente, como a variável [!UICONTROL Ad Group End Date] para um grupo de anúncios, inclua todos os campos necessários para editar esse componente (grupo de anúncios) mais o campo da propriedade ([!UICONTROL Ad Group End Date]).

* Para editar uma propriedade para um componente existente, inclua todos os campos necessários para editar esse componente, além do campo da propriedade.

  Se você deixar o campo de propriedade em branco, o valor existente será retido.

* Excluindo:

   * Para excluir um componente existente, inclua todos os campos necessários para editar esse componente e alterar seu status para [!UICONTROL Deleted]. Por exemplo, para excluir um [!DNL Google Ads] grupo de publicidade, você deve incluir a variável [!UICONTROL Campaign Name], [!UICONTROL Ad Group Name], [!UICONTROL Ad Group Status] com um valor de <i>[!UICONTROL Deleted]</i>, e [!UICONTROL Ad Group ID].

   * ([!UICONTROL Param1], [!UICONTROL Param2], e [!UICONTROL Param3] somente valores) Para excluir um existente [!DNL paramN] para uma palavra-chave, inclua todos os campos necessários para editar a palavra-chave e também exclua os campos [!DNL paramN] inserindo o valor `[delete]` (incluindo os colchetes) no campo correspondente.

   * (Campos de propriedade permitidos) Para excluir um valor de propriedade existente para um componente, inclua todos os campos necessários para editar esse componente e também exclua o valor de propriedade inserindo o valor `[delete]` (incluindo os colchetes). Os campos permitidos incluem:

      * ([!UICONTROL Google Ads] somente) [!UICONTROL Description Line 1], [!UICONTROL Description Line 2]

      * ([!DNL Google Ads] e [!DNL Microsoft® Advertising] somente) [!UICONTROL Product Scope Filter], [!UICONTROL Base URL/Final URL], [!UICONTROL Tracking Template]

>[!NOTE]
>
>Quando você inclui um valor em um campo que não é aplicável à ação, qualquer valor inserido no campo é ignorado.

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de dados de campanha usando bulksheets](../bulksheet-about.md)
>* [Formatos de arquivo de bulksheet compatíveis](bulksheet-file-formats.md)
>* [Apêndice - Erros de bulksheet](../bulksheet-errors.md)
>* [Baixar/criar um arquivo de bulksheet](../bulksheet-download.md)
