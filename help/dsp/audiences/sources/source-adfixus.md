---
title: Importar segmentos próprios de  [!DNL AdFixus]
description: Saiba como importar seus [!DNL AdFixus] segmentos primários que consistem em [!DNL AdFixus] IDs universais para o DSP.
feature: DSP Audiences
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 79f0b3872a0d5d3765093ce83cc8f1c284a8255c
workflow-type: tm+mt
source-wordcount: 448
ht-degree: 0%

---

# Importar segmentos próprios de [!DNL AdFixus]

*Aplicável somente a anunciantes na Austrália*

Use a integração do Advertising DSP com o [!DNL AdFixus] para importar suas IDs universais do [!DNL AdFixus] com mapeamentos de segmentos para publicidade direcionada. [!DNL AdFixus] As IDs estão disponíveis somente na Austrália. O DSP não altera IDs do [!DNL AdFixus] para outros tipos de ID, nem converte outros tipos de ID para IDs do [!DNL AdFixus]. A DSP não cobra uma taxa para importar as IDs.

Depois de importar os segmentos do [!DNL AdFixus] para o DSP, você pode direcionar posicionamentos para [!DNL AdFixus] IDs e para segmentos primários específicos do [!DNL AdFixus]. Você também pode adicionar [!DNL AdFixus] segmentos a públicos-alvo reutilizáveis. Os detalhes de qualquer segmento incluem a contagem de [!DNL AdFixus] IDs aplicáveis.

Você pode exibir a impressão, os cliques, a frequência e outras métricas para usuários com [!DNL AdFixus] IDs em relatórios personalizados. Os anunciantes com [!DNL Analytics for Advertising] também podem exibir dados de view-through para [!DNL AdFixus] IDs da Adobe Analytics, bem como dados do Adobe Analytics no DSP.

1. Use o [!DNL AdFixus] para converter os dados primários de sua organização em segmentos com [!DNL AdFixus] IDs.

   Isso requer uma conta separada com [!DNL AdFixus] e uma chave de licença ativa. Você também precisará implementar o código específico [!DNL AdFixus] para as propriedades e domínios do seu site. Trabalhe diretamente com [!DNL AdFixus] para gerar segmentos com IDs.

1. (Anunciantes com [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Configurar rastreamento para [!DNL Analytics] medição:

   1. (Se ainda não tiver feito isso) Conclua todos os [pré-requisitos para implementar o [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e a [ID do AMO e a ID do EF nas URLs de rastreamento](/help/integrations/analytics/ids.md).

   1. Implante o código específico do [!DNL AdFixus] em suas páginas da Web para corresponder a conversões de [!DNL AdFixus] IDs em navegadores da Web móveis e para desktop (mas não em aplicativos móveis) para view-throughs.

1. Importar os [!DNL AdFixus] segmentos próprios:

   1. [Criar uma origem de público-alvo](source-manage.md) de [!UICONTROL Type] **[!UICONTROL AdFixus ID]**. Você deve consentir com os termos do contrato de serviço.

      As configurações de origem incluirão uma chave de origem gerada automaticamente.

   1. Compartilhe a chave de origem com sua equipe do [!DNL AdFixus] para que eles possam transmitir os segmentos necessários para a DSP.

1. Verifique na seção [!UICONTROL First Party Segments] da biblioteca de público-alvo (que está disponível ao criar ou editar um público a partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas configurações de posicionamento) se o segmento está sendo preenchido. Compare o número de [!DNL AdFixus] IDs com o número de IDs de usuário em [!DNL AdFixus].

   Os segmentos estão disponíveis no DSP assim que são criados.

Os segmentos são atualizados e disponibilizados para direcionamento a cada três horas, embora a contagem mostrada no DSP seja atualizada a cada 24 horas. **Observação:** a inclusão em um segmento expira após um período de expiração especificado, que você configura em [!DNL AdFixus]. Atualize seus segmentos reenviando por push a partir de [!DNL AdFixus] antes da expiração.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo de ID universal](source-manage.md)
>* [conexão com o Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Visão geral do catálogo de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html) do Adobe Experience Platform
>* [Suporte para ativação de IDs universais](/help/dsp/audiences/universal-ids.md)
>* [Sobre o gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
