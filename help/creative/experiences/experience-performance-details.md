---
title: Relatórios de desempenho de nível de experiência
description: Saiba como visualizar relatórios de desempenho no nível da experiência.
feature: Creative Experiences
exl-id: 5e7c4c9d-b992-460a-9765-4276027f9a61
source-git-commit: 1718a7f5a7e3bbfeed336b195a2575275c8fd753
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 0%

---

# Relatórios de desempenho de nível de experiência

*Beta fechado*

Você pode ver dados detalhados do desempenho de qualquer experiência do.

## Dados em relatórios de desempenho no nível da experiência

A visualização Relatório inclui os seguintes dados:

* Guia **Visão geral**: uma visão geral do desempenho em todas as métricas de conversão para toda a experiência<!-- Currently, the only metric in the settings list at the top of this main tab is "Select All." -->, incluindo:

   * Seção **Desempenho Geral**:

      * **Desempenho Geral**: o total de impressões; cliques; taxa de cliques (CTR); e conversões de view-through e conversões de click-through.

     <!--
     ![Overall performance](/help/creative/assets/experience-report-overall-performance.png "Overall performance"){width="100" zoomable="yes"}
          -->

      * **Taxa padrão**: (experiências somente com direcionamento de árvore decisória) o número de impressões resultantes de criações direcionadas, criações genéricas sem um destino ou direcionadas para &quot;Todos os outros&quot; e o criativo padrão da experiência.

     <!--
     ![Default rate](/help/creative/assets/experience-report-default-rate.png "Default rate"){width="100" zoomable="yes"} 
     -->

   * Seção **Detalhamento do Desempenho**:

      * **Desempenho regional:*: métricas individuais por localização geográfica.

        <!--   
      ![Regional performance](/help/creative/assets/experience-report-regional-performance.png "Regional performance"){width="100" zoomable="yes"}
      -->

      * **Desempenho do Dispositivo:** métricas individuais por tipo de dispositivo, sistema operacional e navegador. Opcionalmente, clique no valor de qualquer categoria de dispositivo para ver uma lista das 10 principais criações atendidas com esse critério.

        <!--    
      ![Device performance](/help/creative/assets/experience-report-device-performance.png "Device performance"){width="100" zoomable="yes"}
      -->

* **Guia Desempenho do Creative***: uma visão geral de desempenho por criativo e pacote ou tag de anúncio, incluindo:

   * Subguia **Criations**: o número total de impressões, cliques e CTR de cada criativo na experiência.<!-- No breakdown yet for the individual ad elements and/or the served ads. -->

   * **Pacotes/Marcas** subguia: o número total de impressões, cliques e CTR de pacotes individuais (experiências com direcionamento de árvore de decisão) ou marcas de anúncio (experiências sem direcionamento de árvore de decisão) na experiência.

## Exibir relatórios de desempenho de uma experiência

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Opcional) [Personalize o modo de exibição](/help/creative/introduction/customize-data-views.md) para incluir experiências específicas.

1. Selecione a experiência:

   * No modo de exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome da experiência e, em seguida, clique em **[!UICONTROL Reports]**.

   * Na exibição de tabela, mantenha o cursor sobre a linha e clique em **[!UICONTROL Reports]**.

   A guia [!UICONTROL Overview] é aberta.

1. (Opcional) Na barra de ferramentas superior direita, especifique o intervalo de datas, a regra de atribuição de conversão e as conversões relatadas em todos os relatórios de desempenho:

   * (Opcional) Para alterar o intervalo de datas dos dados de desempenho, escolha uma opção no menu de datas:

      * Para especificar um período predefinido, selecione o relatório: (*[!UICONTROL Last Month-to-date],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Today],* ou *[!UICONTROL Yesterday]*.

      * Para especificar um intervalo de datas personalizado, insira a data de início e a data de término ou clique em ![ícone de calendário](/help/search-social-commerce/assets/calendar.png) ao lado de um campo e selecione uma data.

   * (Opcional) Para alterar a regra usada para atribuir dados de conversão em uma série de eventos que levam a uma conversão, clique em ![Configurações](/help/creative/assets/settings.png) e altere a **[!UICONTROL Attribution Rule]**.

     Para obter mais informações sobre regras de atribuição, consulte &quot;[Como as regras de atribuição são calculadas](/help/search-social-commerce/reports/attribution-rules.md)&quot;.

   * (Opcional) Para alterar as conversões relatadas, clique em ![Configurações](/help/creative/assets/settings.png) e selecione os nomes das conversões no menu **[!UICONTROL Conversions]**. Atualmente, a única métrica disponível é &quot;Selecionar tudo&quot; para incluir todas as métricas de conversão.

     As colunas de conversão disponíveis incluem as conversões disponíveis no Advertising Search, Social e Commerce, independentemente de você ser ou não cliente do Search, Social e Commerce. A lista pode incluir métricas de conversão e envolvimento do site sincronizadas do Adobe Analytics quando o anunciante tiver [uma [!DNL Adobe Analytics for Advertising] integração](/help/integrations/analytics/overview.md). [!DNL Analytics] métricas calculadas e métricas calculadas avançadas não estão disponíveis. Para obter mais informações sobre como incluir conversões coletadas em relatórios, consulte o tópico do Guia de Pesquisa, Social e Commerce &quot;[Sobre o gerenciamento das métricas de conversão de um anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md).&quot;

1. (Na guia [!UICONTROL Overview]):

   * (Opcional) Na seção [!UICONTROL Overall Regional Performance], mantenha o cursor sobre um ponto no gráfico para ver os dados desse ponto.

   * (Opcional) Na seção [!UICONTROL Regional Performance], siga um destes procedimentos:

      * Clique em um nome de métrica (como [!UICONTROL Impressions]) para visualizar essa métrica.

      * Selecione a região no menu [!UICONTROL Region].

      * Mantenha o cursor sobre um país ou estado para ver os dados dessa região.

   * (Opcional) Na seção [!UICONTROL Device Performance], siga um destes procedimentos:

      * Mantenha o cursor sobre o valor de qualquer categoria de dispositivo para ver os dados desse critério.

      * Clique no valor de qualquer categoria de dispositivo para ver uma lista das <!-- NN--> principais criações atendidas com esse critério.

1. (Opcional) Para exibir dados por criativo e por pacote ou tag de anúncio, clique na guia **[!UICONTROL Creative Performance]**.

   * Na subguia [!UICONTROL Creatives], você pode executar um dos seguintes procedimentos:

      * (Opcional) Para alternar entre a exibição de gráfico e a exibição de grade, clique em ![Gráfico](/help/creative/assets/chart-view-button.png "Gráfico") e ![Grade](/help/creative/assets/table-view-button.png "Grade"), respectivamente.

      * (Opcional) Na exibição de gráfico, mantenha o cursor sobre um ponto no gráfico para ver os dados desse ponto.

      * (Experiências somente com direcionamento de árvore de decisão; opcional) Para dividir o desempenho para cada direcionamento de anúncio aplicado, habilite **[!UICONTROL Split targeting]**.

1. Para exibir dados por conjunto (experiências com direcionamento de árvore decisória) ou tag de anúncio (experiências sem direcionamento de árvore decisória), clique na subguia **[!UICONTROL Bundles]**. Você pode executar qualquer um dos seguintes procedimentos:

   * (Opcional) Para alternar entre a exibição de gráfico e a exibição de grade, clique em ![Gráfico](/help/creative/assets/chart-view-button.png "Gráfico") e ![Grade](/help/creative/assets/table-view-button.png "Grade"), respectivamente.

   * (Opcional) Na exibição de gráfico, mantenha o cursor sobre um ponto no gráfico para ver os dados desse ponto.

   * (Experiências somente com direcionamento de árvore de decisão; opcional) Para dividir o desempenho para cada direcionamento de anúncio aplicado, habilite **[!UICONTROL Split targeting]**.

## Baixar relatórios de desempenho para uma experiência

* Na barra de ferramentas na parte superior dos relatórios de desempenho, clique em ![Baixar](/help/creative/assets/download.png "Baixar").

  O arquivo é baixado em um arquivo [!DNL Microsoft Excel] no formato de planilha (XLSX), de acordo com o procedimento normal do navegador.

>[!MORELIKETHIS]
>
>* [Relatório Creative personalizado](/help/creative/report-custom-creative.md)
>* [Baixar todas as experiências no modo de exibição](/help/creative/experiences/experience-download-view.md)
>* [Sobre experiências no Advertising Creative](/help/creative/experiences/experience-about.md)
