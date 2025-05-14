---
title: Duplicar um pacote
description: Saiba como duplicar um pacote.
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 051658d822253e5d0cac56e3d59e99386c68fb71
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Duplicar um pacote

Duplique um pacote para criar um pacote com configurações semelhantes. Você pode:

* Duplicar o pacote no anunciante e na campanha originais ou em anúncios diferentes

* Opcionalmente, duplicar os posicionamentos no pacote

* (Para pacotes duplicados nas campanhas originais) Opcionalmente, duplique os anúncios originais e os pixels do evento no nível do posicionamento

* Modificar as datas de início e término do novo pacote

Consulte &quot;[O que não está duplicado](#package-not-duplicated)&quot; para obter uma lista de configurações de posicionamento que não estão duplicadas.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha para abrir a exibição [!UICONTROL Packages].

1. Ao lado do nome do pacote, clique em **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Especifique as novas configurações de pacote:

   1. Insira o novo nome do pacote.

   1. (Opcional) Altere as configurações padrão.

      Por padrão:

      * O novo pacote é atribuído ao anunciante e à campanha originais.

      * O novo pacote fica ativo no dia atual.<!-- and the flight continues for NN  days. -->

      * Os posicionamentos dentro do pacote original são copiados para o novo pacote.

      * Os pixels do evento de nível de posicionamento e dos anúncios não são copiados para o novo pacote.

1. Clique em **[!UICONTROL Submit]**.

## O que não está duplicado {#package-not-duplicated}

Todas as configurações das disposições originais são duplicadas, exceto:

* Configurações de experimento
* (Se você alterar as datas de veiculação) Programação de anúncios personalizada
* (Se você não anexar anúncios) Peso e agendamento personalizados de anúncios
* Posicionamentos padrão para ofertas programáticas garantidas (PG) e posicionamentos para [!UICONTROL Simple Ad Serving] ofertas
* (Se você copiar disposições para uma campanha diferente):
   * Destinos geográficos
   * Pixels de evento
   * Anúncios
   * Segmentos no nível de posicionamento [!DNL DoubleVerify Authentic Brand Safety] (que substituem os segmentos no nível do anunciante)

## Práticas recomendadas para configurar o novo pacote

>[!TIP]
>
>* Use bulksheets para [fazer alterações em vários componentes da campanha de uma só vez](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Use folhas de marcas de publicidade para [carregar vários anúncios de terceiros](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Pause o novo pacote até estar pronto para ativá-lo.

* Considere o seguinte e edite as novas configurações do pacote conforme necessário:

   * A conta tem financiamento suficiente para acomodar o novo orçamento do pacote?

   * O novo pacote precisa de um orçamento diferente do pacote anterior?

   * Faça upload de criações, incluindo qualquer ponderação e agendamento de anúncio personalizado necessário, e anexe-as aos posicionamentos.

   * Anexe pixels do evento, conforme necessário, aos posicionamentos e anúncios.

   * Inclua destinos geográficos e segmentos de nível de posicionamento [!DNL DoubleVerify Authentic Brand Safety] conforme necessário para posicionamentos.

   * Para ofertas programáticas garantidas, use novas IDs de negócios e crie inserções padrão.

   * Crie novos posicionamentos para [!UICONTROL Simple Ad Serving] ofertas, conforme necessário.

* Para pacotes que usam metas de otimização personalizadas, use a [[!UICONTROL Linked Package for Optimization Learnings Carryover] configuração](/help/dsp/campaign-management/packages/package-settings.md) para cada pacote para usar os dados do histórico da campanha anterior como entrada para otimizar o pacote.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de Pacotes](package-about.md)
>* [Criar um pacote](package-create.md)
>* [Editar um pacote](package-edit.md)
>* [Exibir o Log de Alterações de um Pacote](package-change-log.md)
>* [Configurações do pacote](package-settings.md)
