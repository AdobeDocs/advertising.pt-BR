---
title: Criar vários anúncios de terceiros
description: Saiba como criar vários anúncios de terceiros de uma só vez.
feature: DSP Ads
exl-id: be7c1cc4-3c17-4e37-aae7-c8601d2222a0
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Criar vários anúncios de terceiros

Você pode criar até 500 anúncios de terceiros de cada vez carregando tags que apontam para ativos criativos hospedados em servidores de anúncios de terceiros. É possível incluir pixels de rastreamento para os anúncios.<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

Você pode carregar as folhas de marcas [!DNL DoubleClick] e [!DNL Flashtalking] ou um arquivo preenchido manualmente usando o modelo fornecido.

>[!TIP]
>
> A prática recomendada é usar anúncios de terceiros veiculados com segurança usando HTTPS. Os URLs fornecidos usando HTTPS começam com &quot;https&quot;.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha na qual deseja incluir o anúncio.

1. Acima da tabela de dados, clique em **[!UICONTROL Create]**. Na seção Tipos de anúncio do menu, clique em **[!UICONTROL Bulk upload ads]**.

1. Selecione o servidor de anúncios no qual o anúncio está hospedado: *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]* ou *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] e [!DNL Flashtalking] anúncios) Selecione o tipo de marca a ser usado para cada ativo de vídeo e cada ativo de exibição. As opções disponíveis variam de acordo com o servidor de anúncios.

1. (Anúncios em todos os servidores de publicidade, exceto [!DNL DoubleClick] e [!DNL Flashtalking]) Clique em **[!UICONTROL Download this template]** para baixar um modelo no formato de planilha [!DNL Microsoft Excel] (XLSX), que você pode preencher com dados de publicidade e salvar localmente. As colunas necessárias incluem [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag] e [!UICONTROL Ad Types].

1. Clique em **[!UICONTROL Upload]** e selecione um arquivo nos formatos .xlsx ou .xls no dispositivo ou na rede.

   Para os anúncios [!DNL DoubleClick] e [!DNL Flashtalking], carregue as folhas de tags não editadas do servidor de anúncios. Para outros servidores de publicidade, use o modelo baixado na Etapa 3.

1. Após a conclusão do carregamento, clique em **[!UICONTROL Start Building Ads]**.

1. Analise os detalhes e o status de cada anúncio:

   1. (Anúncios de vídeo universais usando [!DNL Google] ou [!DNL Flashtalking] tags) Clique no campo **[!UICONTROL Ad Type]** e selecione **[!UICONTROL Universal Video]**.

   1. (Anúncios de vídeo universais) Para cada novo anúncio, clique em ![editar](/help/dsp/assets/edit.png), selecione o [formato de vídeo aplicável](/help/dsp/campaign-management/ads/ad-settings-universal-video.md) e clique em **Salvar**.

   1. Analise o status de cada anúncio, que se baseia nas verificações de validação na tag carregada.

   1. (Opcional) Siga um destes procedimentos para cada anúncio:

      * Para visualizar um anúncio, clique em ![reproduzir](/help/dsp/assets/play.png) na linha do anúncio.

      * Para editar os detalhes do anúncio, clique em ![editar](/help/dsp/assets/edit.png), edite os detalhes e clique em **Salvar**.

      * Para remover um anúncio, clique em **[!UICONTROL X]** na linha de anúncio.

1. Clique em **[!UICONTROL Create *N *anúncio(s)]**.

1. Siga um destes procedimentos:

   * Clique em **[!UICONTROL Done]**.

   * (Se um anúncio for rejeitado; opcional) Para editar o registro do anúncio e reenviá-lo para análise:

      1. Clique no nome do anúncio.

      1. Edite as configurações do anúncio.

      1. Clique em **[!UICONTROL Save & submit for review]**.

>[!NOTE]
>
>Anúncios de vídeo universais podem ser anexados somente a inserções de vídeo universais.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de Anúncios](ad-about.md)
>* [Especificações do anúncio](ad-specs.md)
>* [Criar um único anúncio](ad-create.md)
>* [Vídeo: como fazer upload em massa de tags de anúncios de terceiros](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)
>* [Perguntas Frequentes sobre Vídeo Universal](/help/dsp/campaign-management/faq-universal-video.md)
