---
title: Converter IDs de Usuário de  [!DNL ActionIQ]  em IDs Universais
description: Saiba como habilitar o DSP para assimilar seus [!DNL ActionIQ] segmentos primários.
feature: DSP Audiences
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Converter IDs de Usuário de [!DNL ActionIQ] em IDs Universais

*recurso do Beta*

Use a integração do DSP com a plataforma de dados do cliente [!DNL ActionIQ] para converter seus endereços de email com hash em IDs universais para publicidade direcionada.

Há <!-- NN --> etapas para compartilhar dados de [!DNL ActionIQ] com DSP:

1. [Criar uma fonte de público-alvo no DSP](#source-create).

1. ?

## Etapa 1: criar uma fonte de público-alvo no DSP {#source-create}

1. [Crie uma fonte de público-alvo](source-manage.md) para importar públicos para sua conta DSP ou para uma conta de anunciante, especificando os [formatos de ID universal](source-about.md) para os quais deseja converter os identificadores de usuário.

1. Depois de criar a origem do público-alvo, compartilhe a chave do código-fonte com o usuário [!DNL ActionIQ].

## Etapa 2:

## Etapa 3:

1. Verifique na biblioteca de público-alvo (que está disponível quando você cria ou edita um público a partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou nas configurações de posicionamento) se o segmento está preenchendo e compare o número de IDs universais com o número de endereços de email com hash originais.

   Os segmentos devem estar disponíveis no DSP em 24 horas. Depois que o DSP receber os dados do segmento, a contagem de público-alvo deve estar visível dentro de nove (9) horas. Para obter informações sobre taxas de conversão de ID aceitáveis e por que a contagem de segmentos pode variar, consulte &quot;[Variações de dados entre IDs de email e IDs universais](#universal-ids-data-variances)&quot;.

Os segmentos são atualizados a cada 24 horas.

## Solução de problemas

Para solucionar problemas de taxa de conversão e contagem de usuários, consulte &quot;[Suporte para Ativação de Universal IDs](/help/dsp/audiences/universal-ids.md)&quot;.

Para solucionar problemas com o procedimento de conversão, entre em contato com sua equipe de conta do Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Sobre fontes de público-alvo primárias](/help/dsp/audiences/sources/source-about.md)
>* [Gerenciar fontes de público-alvo para ativar públicos-alvo da Universal ID](source-manage.md)
>* [Converter IDs de Usuário de [!DNL Adobe Real-Time CDP] em IDs Universais](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Converter IDs de Usuário de [!DNL Tealium] em IDs Universais](/help/dsp/audiences/sources/source-tealium.md)
>* [Sobre o Gerenciamento de Público-Alvo](/help/dsp/audiences/audience-about.md)
