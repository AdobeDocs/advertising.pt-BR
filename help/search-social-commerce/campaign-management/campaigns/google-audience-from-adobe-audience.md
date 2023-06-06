---
title: Criar [!DNL Google Ads] públicos-alvo de correspondência do cliente de [!DNL Adobe] públicos
description: Saiba como criar [!DNL Google Ads] públicos-alvo de correspondência do cliente dos públicos-alvo Adobe Analytics e Audience Manager existentes.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# Criar [!DNL Google Ads] públicos-alvo de correspondência do cliente do Adobe Analytics e do Audience Manager

*[!DNL Google Ads]contas elegíveis somente para correspondência de cliente*

*Anunciantes com uma integração Adobe Advertising-Adobe Audience Manager ou Adobe Advertising-Adobe Analytics somente*

Os anunciantes aceitos podem criar [!DNL Google Ads] públicos-alvo de correspondência do cliente usando IDs de usuário de a) [!DNL Analytics] segmentos compartilhados com o Adobe Experience Cloud e b) segmentos Audience Manager que têm Pesquisa, Social e Comércio como destino, incluindo [!DNL Analytics] segmentos publicados na Adobe Experience Cloud e segmentos criados usando a Biblioteca de público-alvo da Adobe Experience Cloud. A Pesquisa, o Social e o Commerce enviam automaticamente um [!DNL Google] URL de rastreamento para cada [!DNL Analytics] ou segmento Audience Manager para que [!DNL Google] O pode rastrear o público-alvo.

Each [!DNL Adobe] o público-alvo pode ser usado somente para um [!DNL Google] público-alvo.

Cada novo [!DNL Google] o público-alvo tem o mesmo nome que o original [!DNL Adobe] público-alvo. [!DNL Google] determina o tamanho que o público-alvo deve ter para ser direcionado.

>[!TIP]
>
>Para segmentação em tempo real, use públicos criados por Audience Manager. Segmentos criados no [!DNL Analytics] e sincronizados com o Adobe Experience Cloud podem ter populações menores porque são sincronizados somente diariamente; um surfer que se qualifica para um segmento pode não ser incluído no segmento até o dia seguinte. Segmentos de [!DNL Analytics] têm uma fonte de dados do &quot;conjunto de relatórios - .&quot;

>[!NOTE]
>
>O Search, Social e Commerce não armazena dados do cliente de sua [!DNL Adobe] segmentos usados para criar ou editar um [!DNL Google] público-alvo.

1. Conclua os pré-requisitos conforme necessário:

   1. (Para criar públicos-alvo da lista de remarketing de ID de usuário) Uma [!DNL Adobe] o usuário administrador ou o gerente de conta deve selecionar a configuração no nível do anunciante para habilitar os públicos-alvo de correspondência do cliente. As configurações diferem entre anunciantes com Audience Manager e anunciantes com [!DNL Analytics] somente.

   1. Implementar o [Serviço de identidade da Adobe Experience Platform](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en) versão 2.0 ou superior.

   1. Implante a seguinte tag o mais alto possível nas páginas da Web do anunciante, a partir das quais o público-alvo deve ser rastreado

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      onde `Advertising_Cloud_UserID` é a ID de usuário exclusiva atribuída ao anunciante. Exemplo:  `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Se ainda não tiver sido concluído) Um usuário autorizado deve configurar a conta do anunciante para [sincronizar com a conta da organização do anunciante no Adobe Experience Cloud](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar").

1. Selecione a rede de publicidade e o nome da conta e clique em **[!UICONTROL Continue]**.

1. Especifique as informações do público:

   1. No **[!UICONTROL Data Source]** selecione **[!UICONTROL Adobe Audience]**.

   1. Selecione o [!UICONTROL Adobe Audience] em que basear a [!DNL Google] público-alvo.

      >[!NOTE]
      >
      >[!DNL Adobe] públicos-alvo que já estão sendo usados para outro [!DNL Google] O público-alvo não está disponível.

      Como opção, você pode pesquisar públicos-alvo que contenham uma sequência de texto específica com no mínimo três caracteres. Para qualquer público correspondente, clique em **[!UICONTROL Include]** para selecioná-la.

      Se você selecionar vários [!DNL Adobe] públicos-alvo, depois um [!DNL Google] O público-alvo é criado para cada um.

   1. Selecione o **[!UICONTROL Audience Type]** para criar: **[!UICONTROL Customer List_User ID]**.

      O do anunciante [!DNL Google Ads] a conta deve ser [qualificado para correspondência personalizada](https://support.google.com/adspolicy/answer/6299717) e optou por [remarketing de ID de usuário](https://support.google.com/google-ads/answer/9199250).

   1. Marque a caixa de seleção para indicar que você concorda com os termos da [!DNL Adobe] e políticas de privacidade de rede de anúncios.

   1. Especifique o número de **[!UICONTROL Membership Days]**, que é o número de dias que um cookie do usuário permanece no público-alvo.

      Use o período de tempo durante o qual você espera que seu anúncio seja relevante para o usuário. As listas de remarketing têm uma duração máxima de 540 dias. As listas de clientes não têm uma duração máxima; para indicar que o cookie nunca expira, digite 10000.

   1. Clique em **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] O pode levar até 24 horas para processar o arquivo.
>
>* Consulte [[!DNL Google Ads] documentação sobre como a correspondência do cliente funciona e limitações](https://support.google.com/displayvideo/answer/9539301).


>[!MORELIKETHIS]
>
>* [Sobre públicos](audience-about.md)
>* [Criar um [!DNL Google Ads] público-alvo de correspondência do cliente de uma lista de email da Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gerenciar públicos-alvo de correspondência do cliente usando listas de dados do cliente](audience-from-customer-data-list.md)
>* [Gerenciar públicos de remarketing dinâmicos](audience-dynamic-remarketing-manage.md)

