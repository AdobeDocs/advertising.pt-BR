---
title: Sobre o [!UICONTROL Simple Ad Serving]
description: Saiba mais sobre as ofertas do [!UICONTROL Simple Ad Serving] usando pixels de rastreamento de eventos.
feature: DSP Simple Ad Serving
exl-id: 327a2c93-d729-42e1-856f-f0e05efab7ca
TQID: https://experienceleague.adobe.com/w4KFePatd7CZ1xC8dd1CItl88-6myAZw8TuatHzHnRI
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 227
ht-degree: 0%

---

# Sobre o [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] fornece entrega e relatórios de anúncios garantidos e não decididos para um editor especificado e um único tipo de anúncio usando um único posicionamento dedicado. Use o [!DNL Simple Ad Serving] quando o editor não puder executar sua oferta por meio de IDs de negócios. Todo o direcionamento, o ritmo e o limite de orçamento e o limite de frequência são manipulados pelo editor. Execute essas ofertas por meio de pixels de rastreamento de eventos.

Com [!UICONTROL Simple Ad Serving], cada anúncio é distribuído diretamente pelo editor (servidor do site), e a DSP fornece um pixel de rastreamento de eventos para enviar ao editor, que deve implementar o pixel e o tráfego dos anúncios da DSP. Dependendo do tipo de inventário, os pixels do evento medem os eventos de impressão, click-through e vídeo reproduzidos.

Os seguintes tipos de anúncios estão disponíveis:

* pré-implantação padrão de desktop
* tablet e dispositivo móvel padrão antes da exibição
* pré-exibição padrão de TV conectada
* exibição
* áudio

Você pode criar uma oferta do [!UICONTROL Simple Ad Serving] na exibição [!UICONTROL Inventory] > [!UICONTROL Deals]. O DSP gera automaticamente um posicionamento com o subtipo &quot;[!DNL Simple ad serving]&quot; para o anúncio. A disposição é direcionada ao negócio, mas não permite direcionamento, orçamento ou limite de frequência adicionais. Você pode editar apenas algumas das configurações do negócio, como nome do negócio, CPM, impressões e datas de voo.<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] posicionamentos não estão em conformidade com os fundos utilizáveis da conta ou com os orçamentos de campanha e pacote. No entanto, os gastos são rastreados e contados para esses orçamentos. Mesmo quando o CPM é $0, os dados do evento são sempre rastreados.

>[!MORELIKETHIS]
>
>* [Criar um negócio [!UICONTROL Simple Ad Serving]](simple-deal-create.md)
>* [Editar [!UICONTROL Simple Ad Serving] configurações do negócio](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving] configurações](simple-deal-settings.md)
>* [Exibir um relatório detalhado de um negócio](/help/dsp/inventory/deal-view-report.md)

<!--
 add back when reimplemented:
>* [View event-tracking pixels for a [!UICONTROL Simple Ad Serving] deal](simple-deal-show-pixels.md)
-->
