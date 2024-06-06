---
title: "Converter IDs de usuário de [!DNL ActionIQ] para Universal IDs"
description: "Saiba como habilitar o DSP para assimilar seus [!DNL ActionIQ] segmentos primários."
feature: DSP Audiences
source-git-commit: 729098f01fb9d076efb2b945be4011df9ab1c905
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Converter IDs de usuário de [!DNL ActionIQ] para Universal IDs

*Recurso beta*

Use a integração do DSP com o [!DNL ActionIQ] plataforma de dados do cliente para converter seus endereços de email com hash em IDs universais para publicidade direcionada.

Há <!-- NN --> etapas para compartilhar dados de [!DNL ActionIQ] com DSP:

1. [Criar uma fonte de público no DSP](#source-create).

1. ?

## Etapa 1: criar uma fonte de público-alvo no DSP {#source-create}

1. [Criar uma fonte de público-alvo](source-manage.md) para importar públicos para sua conta DSP ou uma conta de anunciante, especificando o [formatos de ID universal](source-about.md) para o qual você deseja converter os identificadores de usuário.

1. Depois de criar a origem do público-alvo, compartilhe a chave do código-fonte com a [!DNL ActionIQ] usuário.

1. Após concluir todas as etapas, verifique na biblioteca de público-alvo (que está disponível ao criar ou editar um público-alvo em [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas configurações de posicionamento) que o segmento está preenchendo em 24 horas. Compare o número de IDs universais com o número de endereços de email com hash originais.

   A taxa de conversão de endereços de email com hash em IDs universais deve ser superior a 90%. Por exemplo, se você enviar 100 endereços de email com hash da plataforma de dados do cliente, eles deverão ser traduzidos para mais de 90 IDs universais. Uma taxa de tradução de 90% ou menos é um problema. Para obter mais informações sobre como as contagens de segmentos podem variar, consulte &quot;[Causas para variações de dados entre IDs de email e IDs universais](#universal-ids-data-variances).&quot;

   Para obter suporte para solução de problemas, entre em contato com a equipe de conta da Adobe ou `adcloud-support@adobe.com`.

Os segmentos são atualizados a cada 24 horas.

## Etapa 2:

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID](source-manage.md)
>* [Configurações de fonte de público](source-settings.md)
>* [Converter IDs de usuário de [!DNL Adobe Real-Time CDP] para Universal IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Converter IDs de usuário de [!DNL Tealium] para Universal IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)

<!--
>* [Convert User IDs from [!DNL Optimizely] to Universal IDs](/help/dsp/audiences/sources/source-optimizely.md)
-->
