---
title: "Converter IDs de usuário de [!DNL ActionIQ] para Universal IDs"
description: "Saiba como habilitar o DSP para assimilar seus [!DNL ActionIQ] segmentos primários."
feature: DSP Audiences
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Converter IDs de usuário de [!DNL ActionIQ] para Universal IDs

*Recurso do Beta*

Use a integração do DSP com o [!DNL ActionIQ] plataforma de dados do cliente para converter seus endereços de email com hash em IDs universais para publicidade direcionada.

Há <!-- NN --> etapas para compartilhar dados de [!DNL ActionIQ] com DSP:

1. [Criar uma fonte de público no DSP](#source-create).

1. ?

## Etapa 1: criar uma fonte de público-alvo no DSP {#source-create}

1. [Criar uma fonte de público-alvo](source-manage.md) para importar públicos para sua conta DSP ou uma conta de anunciante, especificando o [formatos de ID universal](source-about.md) para o qual você deseja converter os identificadores de usuário.

1. Depois de criar a origem do público-alvo, compartilhe a chave do código-fonte com a [!DNL ActionIQ] usuário.

## Etapa 2:

## Etapa 3:

1. Verifique na biblioteca de público-alvo (que está disponível ao criar ou editar um público-alvo em [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas configurações de posicionamento) que o segmento está preenchendo, e compare o número de IDs universais com o número de endereços de email com hash originais.

   Os segmentos devem estar disponíveis no DSP em 24 horas. Depois que o DSP receber os dados do segmento, a contagem de público-alvo deve estar visível dentro de nove (9) horas. Para obter informações sobre as taxas de conversão de ID aceitáveis e por que a contagem de segmentos pode variar, consulte &quot;[Variações de dados entre IDs de email e IDs universais](#universal-ids-data-variances).&quot;

Os segmentos são atualizados a cada 24 horas.

## Solução de problemas

Para solucionar problemas de taxa de conversão e contagem de usuários, consulte &quot;[Suporte para ativação de IDs universais](/help/dsp/audiences/universal-ids.md).&quot;

Para solucionar problemas com o procedimento de conversão, entre em contato com a equipe de conta do Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID](source-manage.md)
>* [Converter IDs de usuário de [!DNL Adobe Real-Time CDP] para Universal IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Converter IDs de usuário de [!DNL Tealium] para Universal IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Sobre o Gerenciamento de público-alvo](/help/dsp/audiences/audience-about.md)
