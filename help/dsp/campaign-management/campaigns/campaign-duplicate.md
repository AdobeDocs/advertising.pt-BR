---
title: Duplicar uma campanha
description: Saiba como duplicar uma campanha.
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
source-git-commit: 4085c1b21c0fe84653978e449321868921841367
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Duplicar uma campanha

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplique uma campanha para criar uma nova campanha com configurações semelhantes. Você pode:

* Duplique a campanha para o anunciante original ou para uma campanha diferente
* Opcionalmente, duplicar os pacotes e posicionamentos originais
* Modificar as datas de voo da nova campanha

Consulte &quot;[O que não está duplicado](#campaign-not-duplicated)&quot; para obter uma lista de configurações de posicionamento que não estão duplicadas.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Ao lado do nome da campanha, clique em **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Especifique as novas configurações de campanha:

   1. Insira o novo nome da campanha e a data de término da veiculação.

   1. (Opcional) Altere as configurações padrão.

      Por padrão, a nova campanha é atribuída ao anunciante original, tem uma programação de voo que começa no dia atual e inclui os pacotes e disposições originais.

1. Clique em **[!UICONTROL Submit]**.

## O que não está duplicado {#campaign-not-duplicated}

Todas as configurações das disposições originais são duplicadas, exceto:

* Configurações de experimento
* (Se você alterar as datas de veiculação) Programação de anúncios personalizada
* (Se você não anexar anúncios) Peso e agendamento personalizados de anúncios
* Posicionamentos padrão para ofertas programáticas garantidas (PG) e posicionamentos para [!UICONTROL Simple Ad Serving] ofertas
* (Se você copiar disposições para uma campanha diferente):
   * Destinos geográficos
   * Pixels de evento
   * Anúncios
   * Nível de posicionamento [!DNL DoubleVerify Authentic Brand Safety] segmentos (que substituem os segmentos de nível do anunciante)

>[!MORELIKETHIS]
>
>* [Sobre o Campaign Management](campaign-about.md)
>* [Criar uma campanha](campaign-create.md)
>* [Editar uma campanha](campaign-edit.md)
>* [Exibir o Log de Alterações de uma Campanha](campaign-change-log.md)
>* [Configurações da campanha](campaign-settings.md)

