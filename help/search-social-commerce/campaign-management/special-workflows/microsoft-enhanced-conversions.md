---
title: Implementar [!DNL Microsoft Advertising] conversões aprimoradas para conversões offline
description: Saiba mais sobre o fluxo de trabalho para configurar [!DNL Microsoft Advertising] conversões aprimoradas para conversões offline.
feature: Search Campaign Management, Conversions
source-git-commit: 8f87e5bdab25aa527e72d7e9c75411267fe63780
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# Implementar [!DNL Microsoft Advertising] conversões aprimoradas para conversões offline

*[!DNL Microsoft Advertising]somente contas*

[[!DNL Microsoft Advertising] as conversões aprimoradas](https://help.ads.microsoft.com/#apex/ads/en/60178) permitem mapear usuários para conversões offline usando seus dados de conversão primários. Use conversões aprimoradas em ambientes em que as IDs de clique não estão disponíveis, como para rastrear as vendas por telefone ou email resultantes de leads de sites.

No Search, Social e Commerce, você pode:

* Visualize suas conversões aprimoradas existentes para conversões offline.

  O Search, Social e Commerce sincroniza suas conversões aprimoradas existentes diariamente às 05:00 no fuso horário do anunciante.

* Faça upload de dados de conversão primários e offline para mapear para suas metas de conversão aprimoradas existentes.

* Inclua suas conversões aprimoradas como métricas nos relatórios e como métricas ponderadas nos objetivos de otimização.

Para usar esse recurso, conclua as etapas a seguir.

1. Siga todos os pré-requisitos na ajuda do [!DNL Microsoft Advertising] em &quot;[Conversões aprimoradas](https://help.ads.microsoft.com/#apex/ads/en/60178)&quot;.

1. [Configure uma meta de conversão aprimorada [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/60178).

1. Sempre que necessário, carregue dados primários, incluindo endereços de email com hash ou números de telefone, para atribuir à conversão de uma conta especificada. Você pode concluir esta etapa no [Search, Social e Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) ou no [!DNL Microsoft Advertising].

   * Em Pesquisa, Social e Commerce, você pode baixar um modelo no formato [!DNL Microsoft Excel], inserir seus dados de conversão e salvar o arquivo localmente e, em seguida, carregar o arquivo editado.

     Todos os dados carregados são sincronizados em tempo real para [!DNL Microsoft Advertising].

   * Para obter mais informações sobre como carregar dados no [!DNL Microsoft Advertising], consulte a seção &quot;Configurar conversões aprimoradas para conversões offline&quot; na ajuda do [!DNL Microsoft Advertising] em &quot;[Conversões aprimoradas](https://help.ads.microsoft.com/#apex/ads/en/60178).&quot;

>[!MORELIKETHIS]
>
>* [Carregar dados de conversão offline para conversões aprimoradas](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
