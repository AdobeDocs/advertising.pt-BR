---
title: Enviar um anúncio de um contrato PG para  [!DNL FreeWheel]
description: Saiba como solicitar aprovação para um anúncio para um negócio programático garantido com um editor em  [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
TQID: https://experienceleague.adobe.com/f6Cu6mG77YOjwshI4xVbkLSkykAhqXonfSMg5ynDK5g
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: ac506c20-96f2-48f6-9096-77706e336bdaid: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 0%

---

# Enviar um anúncio para uma oferta programática garantida para [!DNL FreeWheel]

*Contas com a [!DNL FreeWheel] permissão programática garantida apenas*

Depois de [aceitar um contrato programático garantido com um editor no FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox), incluindo a seleção de um anúncio e a criação da disposição padrão programática garantida a ser usada para o contrato, você deverá enviar o anúncio para [!DNL FreeWheel] para aprovação.

>[!PREREQUISITES]
>
>Trabalhe com a equipe de conta da Adobe para garantir que a conta [!DNL DSP] tenha permissão para usar o fluxo de trabalho programático garantido [!DNL FreeWheel].

1. Copie a chave do anúncio para o anúncio usado com a oferta [!DNL FreeWheel]:

   1. Clique no nome da campanha.

   1. No submenu, clique em **[!UICONTROL Ads]**.

   1. Clique em **[!UICONTROL ...]** > **[!UICONTROL Edit]** ao lado do nome do anúncio.

   1. Quando as configurações do anúncio forem abertas, copie a chave alfanumérica do anúncio no URL que é exibido na barra de endereços do navegador.

      Por exemplo, na URL a seguir, a chave do anúncio é `3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. Enviar o anúncio para [!DNL FreeWheel]:

   1. Siga um destes procedimentos:

      * Ao lado do nome do anúncio, clique em **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**.

      * No menu principal, clique em **[!UICONTROL Inventory]** > **[!UICONTROL Deals]**. Na linha de negócios, clique em ![Menu de opções](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**.

   1. Verifique a ID de negócios, insira o **[!UICONTROL Ad Key]** que você copiou na Etapa 1 e clique em **[!UICONTROL Submit]**.

   O anúncio deve ser enviado e aprovado antes de ser executado.

1. [Verifique o status de envio do anúncio](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Visão geral da configuração de ofertas programáticas garantidas no [!DNL FreeWheel]](freewheel-overview.md)
>* [Aceitar um contrato no [!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)
>* [Verificar o status dos anúncios de um [!DNL FreeWheel] PG_deal](freewheel-check-status.md)
>* [Códigos de erro para [!DNL FreeWheel] envios de anúncios](freewheel-error-codes.md)
