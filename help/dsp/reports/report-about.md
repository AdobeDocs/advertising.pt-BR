---
title: Sobre Relatórios Personalizados
description: Saiba mais sobre as opções para criar relatórios personalizados manualmente ou usar modelos de relatório pré-configurados.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 44f7f9b31afbe6b863acd389df641057b1e6dea1
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 0%

---

# Sobre Relatórios Personalizados

Relatórios personalizados permitem personalizar o conteúdo e a entrega dos dados de relatório usando as dimensões da campanha (como anunciante, posicionamento, sites ou geografia) e as métricas mais importantes para você. Você pode:

* Configure completamente relatórios de desempenho de campanha em nível detalhado.

* Escolha entre modelos de relatório pré-configurados e, como opção, personalize-os ainda mais.

Você pode gerar relatórios uma vez ou agendá-los para serem gerados diariamente, semanalmente ou mensalmente, às 03:00 no fuso horário especificado, de acordo com os critérios especificados (como a cada 15 dias ou no primeiro dia de cada mês). Depois que um relatório é gerado, você pode baixá-lo de [!UICONTROL Reports] > [!UICONTROL Custom Reports] ou dos [destinos de relatórios](/help/dsp/reports/report-destinations/report-destination-about.md) vinculados dos seguintes tipos:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SSL FTP <!-- (in beta) -->
* SFTP

>[!NOTE]
>
>Você também pode exibir dados sob demanda em todos os níveis de uma campanha (campanha, pacote, posicionamento ou anúncio) [na exibição de gerenciamento de campanha relevante](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Tipos de Relatório Disponíveis

* **[!UICONTROL Custom]:** Este relatório é um modelo em branco que você pode usar para criar seu próprio relatório personalizado usando a maioria das dimensões e métricas. Os relatórios [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo] e [!UICONTROL Site] são variações deste modelo com colunas e dimensões pré-selecionadas para seus respectivos casos de uso.

* Modelos de relatório pré-configurados

   * **[!UICONTROL Billing]:** use este relatório para entender as principais métricas de cobrança, como as métricas de gastos para cobrança de mídia por campanha. Os dados não estão disponíveis para posicionamentos que direcionam IDs universais.

     >[!NOTE]
     >
     >Este relatório inclui dados sobre o segmento de faturamento. Se um usuário ou dispositivo receber uma impressão que pertença a vários segmentos, somente um segmento faturável será creditado com a impressão.

   * **[!UICONTROL Conversion]:** Use este relatório para entender o desempenho de suas campanhas com base em métricas de conversão capturadas com o rastreamento de conversão de Adobe Advertising. Este relatório inclui atribuição multitoque.

   * **[!UICONTROL Device]:** Use este modelo pré-preenchido para ver as métricas principais por dimensões relacionadas ao dispositivo.

   * **[!UICONTROL Frequency (by Impression)]:** Use este relatório para entender a distribuição de impressões mostradas para visualizadores únicos (por exemplo, quantos visualizadores únicos viram uma impressão, duas impressões, três impressões e assim por diante). Os dados estão disponíveis por disposição ou campanha.

     >[!NOTE]
     >
     >* Os dados estarão disponíveis após 1º de março de 2019.
     >* A frequência é estimada com base em uma amostra de dados.
     >* Para alguns inventários, os editores não transmitem um identificador de dispositivo, o que impede o rastreamento de frequência. Este relatório inclui somente impressões para as quais um identificador de dispositivo estava disponível.

   * **[!UICONTROL Frequency (by App/Site)]:** Use este relatório para entender quantos usuários únicos foram atingidos por aplicativo ou por site. Você também pode ver quantos usuários únicos foram atingidos por meio de apenas um aplicativo ou site específico (&quot;usuários únicos distintos&quot;).

     >[!NOTE]
     >
     >* Os dados estarão disponíveis após 15 de novembro de 2018.
     >* Para alguns inventários privados, os editores não transmitem um identificador de dispositivo, o que impede o rastreamento de frequência.

   * **[!UICONTROL Geo]**: use este modelo pré-preenchido para ver as métricas principais por dimensões geográficas.

   * **[!UICONTROL Margin]:** Use este relatório para ver as métricas principais, como margem, lucro e outras métricas de gastos por campanha ou posicionamento. Os dados não estão disponíveis para posicionamentos que direcionam IDs universais.

   * **[!UICONTROL Segment]:** Use este modelo pré-preenchido para ver as métricas principais por segmento.

     >[!NOTE]
     >
     >* Este relatório tem como objetivo mostrar o desempenho de diferentes segmentos direcionados. Ele usa dados de associação de segmento. Quando uma impressão é transmitida a uma pessoa ou dispositivo pertencente a dois ou mais segmentos direcionados, este relatório inclui uma linha para cada segmento. Por esse motivo, os totais neste relatório podem não corresponder à entrega real.
     >* Métricas de conversão e dados de meta personalizados para segmentos estão disponíveis após 2 de agosto de 2019. Todos os outros dados para segmentos estarão disponíveis após 1º de junho de 2018.

   * **[!UICONTROL Site]:** Por padrão, inclui métricas padrão, gasto líquido total de mídia e gasto líquido faturável total por site.

   * **[!UICONTROL Household Reach & Frequency]:** use este relatório para ver as impressões, o alcance e a frequência de uma única dimensão em formatos de anúncio em um nível doméstico com base no endereço IP, em vez de em um nível de dispositivo/cookie. Use os insights para otimizar sua combinação de mídia, melhorar o desempenho e identificar oportunidades para alcance incremental. Consulte &quot;[Perguntas frequentes sobre Relatórios do Agregado Doméstico](/help/dsp/reports/faq-household-report.md)&quot; para obter mais informações. Os dados não estão disponíveis para posicionamentos que direcionam IDs universais.

   * **[!UICONTROL Household Conversions]:** Use este relatório para ver conversões de view-through no nível doméstico com base no endereço IP, em vez de no nível do dispositivo/cookie. Use os insights para medir e otimizar o desempenho da campanha. Consulte &quot;[Perguntas frequentes sobre Relatórios do Agregado Doméstico](/help/dsp/reports/faq-household-report.md)&quot; para obter mais informações. Os dados não estão disponíveis para posicionamentos que direcionam IDs universais.

## Relatório entre contas {#cross-account-reporting}

Qualquer organização com várias contas DSP pode, opcionalmente, ativar dados entre contas em relatórios personalizados, de acordo com as necessidades da organização. Por exemplo, você pode conceder acesso à Conta A aos dados da Conta B e conceder acesso à Conta B aos dados da Conta C (mas não da Conta A). Para ativar e configurar esse recurso, entre em contato com a equipe de conta do Adobe.

Depois que o recurso for habilitado para sua organização, você poderá [filtrar](report-settings.md) qualquer um dos seguintes tipos de relatório por conta: [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] e [!UICONTROL Conversion].

As configurações da sua conta em [!UICONTROL Settings] > [!UICONTROL Account] indicam a) as outras contas cujos dados estão disponíveis para a sua conta e b) as outras contas que podem acessar os dados da sua conta.

## A Visão [!UICONTROL Custom Reports]

[!UICONTROL Reports] > [!UICONTROL Custom Reports] lista seus relatórios existentes, incluindo relatórios que foram gerados, aqueles que estão agendados para geração futura e aqueles que falharam. A coluna &quot;[!UICONTROL Report Run]&quot; mostra as datas em que o relatório foi acionado a partir de 22 de agosto de 2024. Por padrão, todos os relatórios não arquivados criados pelo usuário são listados, com o mais recente no topo. Você pode filtrar ainda mais a lista por status, se o relatório é recorrente ou ocasional, o tipo de relatório, o tipo de destino e o criador do relatório.

Você pode criar novos relatórios personalizados, editar relatórios existentes ou duplicá-los para criar novos relatórios, executar relatórios imediatamente, baixar qualquer instância de relatório dos últimos quatro meses e excluir relatórios.

## Status do relatório {#custom-report-status}

* **[!UICONTROL Yet to start]:** O relatório nunca foi executado.

* **[!UICONTROL Report generating]:** O relatório está sendo criado.

* **[!UICONTROL Ready to download]:** (Somente relatórios recorrentes) Uma ou mais instâncias do relatório estão disponíveis para download e mais instâncias de relatório estão agendadas.

* **[!UICONTROL Failed]:** Falha no trabalho de relatório. Para ver por que as instâncias de relatório individuais falharam em um cabo de relatório, clique em ![seta para baixo](/help/dsp/assets/chevron-down.png "seta para baixo") ao lado de [!UICONTROL Download]. Os trabalhos de relatório com falha são indicados com um ícone de erro (![indicador de erro](/help/dsp/assets/indicator-critical.png "indicador de erro")). Mantenha o cursor sobre o ícone de erro para obter uma descrição do erro.

* **[!UICONTROL Completed]:** Para relatórios não recorrentes, o relatório foi concluído. Para relatórios recorrentes, todas as instâncias de relatório são concluídas. É possível baixar todos os relatórios concluídos nos últimos quatro meses.

* **[!UICONTROL Archived]:** O relatório está arquivado e não pode ser executado. Esse status é definido quando a geração de relatório falha várias vezes em um relatório. No momento, não é possível definir esse status na interface.

>[!MORELIKETHIS]
>
>* [Criar um relatório personalizado](/help/dsp/reports/report-create.md)
>* [Baixar um Relatório Personalizado](/help/dsp/reports/report-download.md)
>* [Configurações de Relatório Personalizado](/help/dsp/reports/report-settings.md)
>* [Perguntas Frequentes sobre Relatórios Domésticos](/help/dsp/reports/faq-household-report.md)
>* [Tipos de Relatórios de Desempenho em Exibições do Campaign Management](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Colunas de Relatório Disponíveis](/help/dsp/reports/report-columns.md)
>* [Sobre [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
