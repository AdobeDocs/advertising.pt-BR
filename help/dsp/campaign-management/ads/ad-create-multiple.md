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

Você pode fazer upload de [!DNL DoubleClick] e [!DNL Flashtalking] ou um arquivo preenchido manualmente usando o modelo fornecido.

>[!TIP]
>
> A prática recomendada é usar anúncios de terceiros veiculados com segurança usando HTTPS. Os URLs fornecidos usando HTTPS começam com &quot;https&quot;.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha na qual deseja incluir o anúncio.

1. Acima da tabela de dados, clique em **[!UICONTROL Create]**. Na seção Tipos de anúncio do menu, clique em **[!UICONTROL Bulk upload ads]**.

1. Selecione o servidor de publicidade no qual o anúncio está hospedado: *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]* ou *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] e [!DNL Flashtalking] anúncios) Selecione o tipo de tag a ser usado para cada ativo de vídeo e cada ativo de exibição. As opções disponíveis variam de acordo com o servidor de anúncios.

1. (Anúncios em todos os servidores de anúncios, exceto [!DNL DoubleClick] e [!DNL Flashtalking]) Clique em **[!UICONTROL Download this template]** para baixar um modelo em [!DNL Microsoft Excel] formato de planilha eletrônica (XLSX), que pode ser preenchido com dados de publicidade e salvo localmente. As colunas necessárias incluem [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag], e [!UICONTROL Ad Types].

1. Clique em **[!UICONTROL Upload]** e selecione um arquivo nos formatos .xlsx ou .xls no dispositivo ou na rede.

   Para [!DNL DoubleClick] e [!DNL Flashtalking] anúncios, carregue folhas de tags não editadas do servidor de publicidade. Para outros servidores de publicidade, use o modelo baixado na Etapa 3.

1. Após concluir o upload, clique em **[!UICONTROL Start Building Ads]**.

1. Analise os detalhes e o status de cada anúncio:

   1. (Anúncios de vídeo universais usando [!DNL Google] ou [!DNL Flashtalking] tags) Clique no link **[!UICONTROL Ad Type]** e selecione **[!UICONTROL Universal Video]**.

   1. (Anúncios de vídeo universais) Para cada novo anúncio, clique em ![editar](/help/dsp/assets/edit.png), selecione o [formato de vídeo aplicável](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)e clique em **Salvar**.

   1. Analise o status de cada anúncio, que se baseia nas verificações de validação na tag carregada.

   1. (Opcional) Siga um destes procedimentos para cada anúncio:

      * Para visualizar um anúncio, clique em ![play](/help/dsp/assets/play.png) na linha de anúncio.

      * Para editar os detalhes do anúncio, clique em ![editar](/help/dsp/assets/edit.png), edite os detalhes e clique em **Salvar**.

      * Para remover um anúncio, clique em **[!UICONTROL X]** na linha de anúncio.

1. Clique em **[!UICONTROL Create *N *Anúncio(s)]**.

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
>* [Sobre o gerenciamento de anúncios](ad-about.md)
>* [Especificações de publicidade](ad-specs.md)
>* [Crie um único anúncio](ad-create.md)
>* [Vídeo: como fazer upload em massa de tags de anúncios de terceiros](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)
>* [Perguntas frequentes sobre o Universal Video](/help/dsp/campaign-management/faq-universal-video.md)
