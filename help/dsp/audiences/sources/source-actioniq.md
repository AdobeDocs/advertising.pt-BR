---
title: Converter IDs de usuário de  [!DNL ActionIQ]  em IDs universais
description: Saiba como habilitar o DSP para assimilar seus [!DNL ActionIQ] segmentos primários.
feature: DSP Audiences
source-git-commit: 658c8a10c4085690ce4dd7e791883dbf31f1cb10
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Converter IDs de usuário de [!DNL ActionIQ] em IDs universais

*recurso do Beta*

Use a integração do DSP com a plataforma de dados do cliente [!DNL ActionIQ] para converter seus endereços de email com hash em IDs universais para publicidade direcionada.

Há <!-- NN --> etapas para compartilhar dados de [!DNL ActionIQ] com a DSP:

1. [Criar uma origem de público-alvo no DSP](#source-create).

1. ?

## Etapa 1: criar uma fonte de público-alvo no DSP {#source-create}

1. [Crie uma fonte de público-alvo](source-manage.md) para importar públicos para sua conta da DSP ou uma conta de anunciante, especificando os [formatos de ID universal](source-about.md) para os quais você deseja converter seus identificadores de usuário.

1. Depois de criar a origem do público-alvo, compartilhe a chave do código-fonte com o usuário [!DNL ActionIQ].

## Etapa 2:

## Etapa 3:

1. Verifique na biblioteca de público-alvo (que está disponível quando você cria ou edita um público a partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas configurações de posicionamento) se o segmento está preenchendo e compare o número de IDs universais com o número de endereços de email com hash originais.

   Os segmentos devem estar disponíveis no DSP em 24 horas. Depois que a DSP receber os dados do segmento, o contagem de público-alvo deverá ficar visível dentro de nove (9) horas. Para obter informações sobre taxas de conversão de ID aceitáveis e por que a contagem de segmentos pode variar, consulte &quot;[Variações de dados entre IDs de email e IDs universais](#universal-ids-data-variances)&quot;.

Os segmentos são atualizados a cada 24 horas.

## Solução de problemas

Para solucionar problemas de taxa de conversão e contagem de usuários, consulte &quot;[Suporte para ativação de IDs universais](/help/dsp/audiences/universal-ids.md)&quot;.

Para solucionar problemas com o procedimento de conversão, entre em contato com sua equipe de conta da Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo de ID universal](source-manage.md)
>* [Converter IDs de usuário de [!DNL Adobe Real-Time CDP] em IDs universais](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Converter IDs de usuário de [!DNL Tealium] em IDs universais](/help/dsp/audiences/sources/source-tealium.md)
>* [Sobre o gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
