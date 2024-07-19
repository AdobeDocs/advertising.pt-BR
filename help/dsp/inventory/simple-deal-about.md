---
title: Sobre o [!UICONTROL Simple Ad Serving]
description: Saiba mais sobre as ofertas do [!UICONTROL Simple Ad Serving] usando pixels de rastreamento de eventos.
feature: DSP Simple Ad Serving
exl-id: 327a2c93-d729-42e1-856f-f0e05efab7ca
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Sobre o [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] fornece entrega e relatórios de anúncios garantidos e não decididos para um editor especificado e um único tipo de anúncio usando um único posicionamento dedicado. Use o [!DNL Simple Ad Serving] quando o editor não puder executar sua oferta por meio de IDs de negócios. Todo o direcionamento, o ritmo e o limite de orçamento e o limite de frequência são manipulados pelo editor. Execute essas ofertas por meio de pixels de rastreamento de eventos.

Com [!UICONTROL Simple Ad Serving], cada anúncio é veiculado diretamente pelo editor (servidor do site), e o DSP fornece um pixel de rastreamento de eventos para enviar ao editor, que deve implementar o pixel e o tráfego dos anúncios DSP. Dependendo do tipo de inventário, os pixels do evento medem os eventos de impressão, click-through e vídeo reproduzidos.

Os seguintes tipos de anúncios estão disponíveis:

* pré-implantação padrão de desktop
* tablet e dispositivo móvel padrão antes da exibição
* pré-exibição padrão de TV conectada
* exibição
* áudio

Você pode criar uma oferta do [!UICONTROL Simple Ad Serving] na exibição [!UICONTROL Inventory] > [!UICONTROL Deals]. O DSP gera automaticamente um posicionamento com o subtipo &quot;[!DNL Simple ad serving]&quot; para o anúncio. A disposição é direcionada ao negócio, mas não permite direcionamento, orçamento ou limite de frequência adicionais. Você pode editar apenas algumas das configurações do negócio, como nome do negócio, CPM, impressões e datas de voo.<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] posicionamentos não estão em conformidade com os fundos utilizáveis da conta ou com os orçamentos de campanha e pacote. No entanto, os gastos são rastreados e contados para esses orçamentos. Mesmo quando o CPM é de US$ 0, os dados do evento são sempre rastreados.

>[!MORELIKETHIS]
>
>* [Criar um Contrato [!UICONTROL Simple Ad Serving]](simple-deal-create.md)
>* [Editar [!UICONTROL Simple Ad Serving] Configurações de oferta](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving] Configurações](simple-deal-settings.md)
>* [Exibir um Relatório Detalhado de um Acordo](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
