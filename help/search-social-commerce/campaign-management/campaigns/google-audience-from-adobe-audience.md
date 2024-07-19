---
title: Criar [!DNL Google Ads] públicos-alvo de correspondência do cliente de [!DNL Adobe] públicos-alvo
description: Saiba como criar [!DNL Google Ads] públicos-alvo de correspondência do cliente a partir dos públicos-alvo existentes da Adobe Analytics e do Audience Manager.
exl-id: 7de95ebb-24b0-459f-83c0-7b85b0c0576d
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Criar [!DNL Google Ads] públicos-alvo de correspondência do cliente do Adobe Analytics e do Audience Manager

*[!DNL Google Ads]contas qualificadas somente para correspondência de cliente*

*Anunciantes somente com integração Adobe Advertising-Adobe Audience Manager ou Adobe Advertising-Adobe Analytics*

Os anunciantes aceitos podem criar [!DNL Google Ads] públicos-alvo de correspondência do cliente usando IDs de usuário de a) [!DNL Analytics] segmentos compartilhados com a Adobe Experience Cloud e b) segmentos Audience Manager que têm Search, Social e Commerce como destino, incluindo [!DNL Analytics] segmentos publicados na Adobe Experience Cloud e segmentos criados com a Biblioteca de público-alvo da Adobe Experience Cloud. O Search, Social e Commerce envia automaticamente uma URL de rastreamento [!DNL Google] de volta para cada segmento [!DNL Analytics] ou Audience Manager, para que [!DNL Google] possa rastrear o público.

Cada público-alvo [!DNL Adobe] pode ser usado somente para um público-alvo [!DNL Google].

Cada novo público-alvo de [!DNL Google] tem o mesmo nome que o público-alvo original de [!DNL Adobe]. [!DNL Google] determina o tamanho que o público-alvo deve ter para ser direcionado.

>[!TIP]
>
>Para segmentação em tempo real, use públicos criados por Audience Manager. Segmentos criados no [!DNL Analytics] e sincronizados com o Adobe Experience Cloud podem ter populações menores, pois são sincronizados apenas diariamente. Um surfer que se qualifica para um segmento não pode ser incluído no segmento até o dia seguinte. Segmentos de [!DNL Analytics] têm uma fonte de dados de &quot;conjunto de relatórios - .&quot;

>[!NOTE]
>
>A Search, Social e Commerce não armazena dados de clientes de seus segmentos do [!DNL Adobe] usados para criar ou editar um público-alvo do [!DNL Google].

1. Conclua os pré-requisitos conforme necessário:

   1. (Para criar públicos-alvo de lista de remarketing de ID de usuário) Um usuário administrador ou gerente de conta do [!DNL Adobe] deve selecionar a configuração no nível do anunciante para habilitar os públicos-alvo de correspondência do cliente.

   1. Implemente o [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) versão 2.0 ou superior.

   1. Implante a seguinte tag o mais alto possível nas páginas da Web do anunciante, a partir das quais o público-alvo deve ser rastreado

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      onde `Advertising_Cloud_UserID` é o identificador de usuário numérico exclusivo atribuído ao anunciante.

      Exemplo: `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Se ainda não tiver sido concluído) Um usuário autorizado deve configurar a conta do anunciante para [sincronizar com a conta da organização do anunciante no Adobe Experience Cloud](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar").

1. Selecione a rede de publicidade e o nome da conta e clique em **[!UICONTROL Continue]**.

1. Especifique as informações do público:

   1. No menu **[!UICONTROL Data Source]**, selecione **[!UICONTROL Adobe Audience]**.

   1. Selecione o [!UICONTROL Adobe Audience] no qual basear o público-alvo [!DNL Google].

      >[!NOTE]
      >
      >[!DNL Adobe] públicos-alvo que já estão sendo usados para outro público-alvo de [!DNL Google] não estão disponíveis.

      Como opção, você pode pesquisar públicos-alvo que contenham uma sequência de texto específica com no mínimo três caracteres. Para qualquer público correspondente, clique em **[!UICONTROL Include]** para selecioná-lo.

      Se você selecionar vários públicos-alvo de [!DNL Adobe], um público-alvo [!DNL Google] separado será criado para cada um.

   1. Selecione o **[!UICONTROL Audience Type]** para criar: **[!UICONTROL Customer List_User ID]**.

      A conta [!DNL Google Ads] do anunciante deve ser [qualificada para correspondência personalizada](https://support.google.com/adspolicy/answer/6299717) e aceita para [remarketing de ID de usuário](https://support.google.com/google-ads/answer/9199250).

   1. Marque a caixa de seleção para indicar que você concorda com os termos do [!DNL Adobe] e com as políticas de privacidade de rede de anúncios.

   1. Especifique o número de **[!UICONTROL Membership Days]**, que é o número de dias que um cookie do usuário permanece no público-alvo.

      Use o período de tempo durante o qual você espera que seu anúncio seja relevante para o usuário. As listas de remarketing têm uma duração máxima de 540 dias. As listas de clientes não têm uma duração máxima; para indicar que o cookie nunca expira, digite 10000.

   1. Clique em **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] pode levar até 24 horas para processar o arquivo.
>
>* Consulte [[!DNL Google Ads] documentação sobre como a correspondência entre clientes funciona e limitações](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [Sobre públicos-alvo](audience-about.md)
>* [Criar um [!DNL Google Ads] público-alvo de correspondência do cliente a partir de uma lista de emails do Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gerenciar públicos-alvo de correspondência do cliente usando listas de dados do cliente](audience-from-customer-data-list.md)
>* [Gerenciar públicos de remarketing dinâmicos](audience-dynamic-remarketing-manage.md)
