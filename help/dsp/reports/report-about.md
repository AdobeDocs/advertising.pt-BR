---
title: Sobre Relatórios Personalizados
description: Saiba mais sobre as opções para criar relatórios personalizados manualmente ou usar modelos de relatório pré-configurados.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Sobre Relatórios Personalizados

Relatórios personalizados permitem personalizar o conteúdo e a entrega dos dados de relatório usando as dimensões da campanha (como anunciante, posicionamento, sites ou geografia) e as métricas mais importantes para você. Você pode:

* Configure completamente relatórios de desempenho de campanha em nível detalhado.
* Escolha entre modelos de relatório pré-configurados e, como opção, personalize-os ainda mais.

Você pode gerar relatórios uma vez ou agendá-los para serem gerados diariamente, semanalmente ou mensalmente, às 03:00 no fuso horário especificado. Depois que um relatório é gerado, ele é entregue a cada recipient de email especificado ou vinculado [destinos de relatório](/help/dsp/reports/report-destinations/report-destination-about.md) dos seguintes tipos:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SFTP
* FTP SSL (na versão beta)

>[!NOTE]
>
>Você também pode visualizar dados sob demanda em todos os níveis de uma campanha (campanha, pacote, posicionamento ou anúncio) [na visualização relevante do gerenciamento de campanhas](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Tipos de Relatório Disponíveis

* **[!UICONTROL Custom]:** Este relatório é um modelo em branco que você pode usar para criar seu próprio relatório personalizado usando a maioria das dimensões e métricas. [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], e [!UICONTROL Site] os relatórios são variações desse modelo com colunas e dimensões pré-selecionadas para seus respectivos casos de uso.

* Modelos de relatório pré-configurados

   * **[!UICONTROL Billing]:** Use este relatório para entender as principais métricas de cobrança, como as métricas de gastos para cobrança de mídia por campanha.

      >[!NOTE]
      >
      >Este relatório inclui dados sobre o segmento de faturamento. Se um usuário ou dispositivo receber uma impressão que pertença a vários segmentos, somente um segmento faturável será creditado com a impressão.

   * **[!UICONTROL Conversion]:** Use este relatório para entender como está o desempenho de suas campanhas com base em métricas de conversão capturadas usando o rastreamento de conversão do Adobe Advertising. Este relatório inclui atribuição multitoque.

   * **[!UICONTROL Device]:** Use esse modelo pré-preenchido para ver as métricas principais por dimensões relacionadas ao dispositivo.

   * **[!UICONTROL Frequency (by Impression)]:** Use este relatório para entender a distribuição de impressões mostradas para visualizadores únicos (por exemplo, quantos visualizadores únicos visualizaram uma impressão, duas impressões, três impressões e assim por diante). Os dados estão disponíveis por disposição ou campanha.

      >[!NOTE]
      >
      >* Os dados estarão disponíveis após 1º de março de 2019.
      >* A frequência é estimada com base em uma amostra de dados.
      >* Para alguns inventários, os editores não transmitem um identificador de dispositivo, o que impede o rastreamento de frequência. Este relatório inclui somente impressões para as quais um identificador de dispositivo estava disponível.


   * **[!UICONTROL Frequency (by App/Site)]:** Use este relatório para entender quantos usuários únicos foram alcançados por aplicativo ou por site. Você também pode ver quantos usuários únicos foram atingidos por meio de apenas um aplicativo ou site específico (&quot;usuários únicos distintos&quot;).

      >[!NOTE]
      >
      >* Os dados estarão disponíveis após 15 de novembro de 2018.
      >* Para alguns inventários privados, os editores não transmitem um identificador de dispositivo, o que impede o rastreamento de frequência.


   * **[!UICONTROL Geo]**: use esse modelo pré-preenchido para ver as métricas principais por dimensões geográficas.

   * **[!UICONTROL Margin]:** Use este relatório para ver as métricas principais, como margem, lucro e outras métricas de gastos por campanha ou posicionamento.

   * **[!UICONTROL Segment]:** Use esse modelo pré-preenchido para ver as métricas principais por segmento.

      >[!NOTE]
      >
      >* Este relatório tem como objetivo mostrar o desempenho de diferentes segmentos direcionados. Ele usa dados de associação de segmento. Quando uma impressão é transmitida a uma pessoa ou dispositivo pertencente a dois ou mais segmentos direcionados, este relatório inclui uma linha para cada segmento. Por esse motivo, os totais neste relatório podem não corresponder à entrega real.
      >* Métricas de conversão e dados de meta personalizados para segmentos estão disponíveis após 2 de agosto de 2019. Todos os outros dados para segmentos estarão disponíveis após 1º de junho de 2018.


   * **[!UICONTROL Site]:** Por padrão, inclui métricas padrão, gasto líquido total de mídia e gasto líquido faturável total por site.

## Relatório entre contas {#cross-account-reporting}

Qualquer organização com várias contas DSP pode, opcionalmente, ativar dados entre contas em relatórios personalizados, de acordo com as necessidades da organização. Por exemplo, você pode conceder acesso à Conta A aos dados da Conta B e conceder acesso à Conta B aos dados da Conta C (mas não da Conta A). Para ativar e configurar esse recurso, entre em contato com a equipe de conta do Adobe.

Depois que o recurso for ativado para sua organização, você poderá [filtro](report-settings.md) qualquer um dos seguintes tipos de relatório por conta:  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)], e [!UICONTROL Conversion].

Suas configurações de conta em [!UICONTROL Settings] > [!UICONTROL Account] indique a) as outras contas cujos dados estão disponíveis para sua conta e b) as outras contas que podem acessar os dados de sua conta.

>[!MORELIKETHIS]
>
>* [Criar um relatório personalizado](/help/dsp/reports/report-create.md)
>* [Configurações do relatório personalizado](/help/dsp/reports/report-settings.md)
>* [Sobre Relatórios Na Plataforma](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Colunas de Relatório Disponíveis](/help/dsp/reports/report-columns.md)
>* [Sobre [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)

