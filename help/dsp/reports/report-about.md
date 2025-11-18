---
title: Sobre Relatórios Personalizados
description: Saiba mais sobre as opções para criar relatórios personalizados manualmente ou usar modelos de relatório pré-configurados.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: a643a2d255431c5ce93f2df092d92932d4cccc02
workflow-type: tm+mt
source-wordcount: '1623'
ht-degree: 0%

---

# Sobre Relatórios Personalizados

Relatórios personalizados permitem personalizar o conteúdo e a entrega dos dados de relatório usando as dimensões da campanha (como anunciante, posicionamento, sites ou geografia) e as métricas mais importantes para você. Você pode:

* Configure completamente relatórios de desempenho de campanha em nível detalhado.

* Escolha entre modelos de relatório pré-configurados e, como opção, personalize-os ainda mais.

Você pode gerar relatórios uma vez ou agendá-los diariamente, semanalmente ou mensalmente às 03:00 no fuso horário especificado, de acordo com os critérios especificados (como a cada 15 dias ou no primeiro dia de cada mês). Depois que um relatório é gerado, você pode baixá-lo de [!UICONTROL Reports] > [!UICONTROL Custom Reports] ou dos [destinos de relatórios](/help/dsp/reports/report-destinations/report-destination-about.md) vinculados dos seguintes tipos:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SSL FTP <!-- (in beta) -->
* SFTP

>[!NOTE]
>
>Você também pode exibir dados sob demanda em todos os níveis de uma campanha (campanha, pacote, posicionamento ou anúncio) [na exibição de gerenciamento de campanha relevante](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Tipos de Relatório Disponíveis

* **[!UICONTROL Custom]:** Este relatório é um modelo em branco que pode ser usado para criar seu próprio relatório personalizado usando a maioria das dimensões e métricas. Os relatórios [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo] e [!UICONTROL Site] são variações deste modelo com colunas e dimensões pré-selecionadas para seus respectivos casos de uso.

* Modelos de relatório pré-configurados

   * **[!UICONTROL All-in Cost BETA]**: (anunciantes somente com Advertising Creative e Advertising DSP; recurso beta) Use este relatório para ver quanto o Advertising DSP gastou foi atribuído à veiculação de anúncios do Adobe Creative. Você pode exibir dados criativos, de atributos, de público-alvo e outros dados nos níveis de campanha, pacote, posicionamento e anúncio.

   * **[!UICONTROL Billing]:** use este relatório para entender as principais métricas de cobrança, como as métricas de gastos para cobrança de mídia por campanha. Os dados não estão disponíveis para posicionamentos que direcionam IDs universais.

     >[!NOTE]
     >
     >Este relatório inclui dados sobre o segmento de faturamento. Se um usuário ou dispositivo receber uma impressão que pertença a vários segmentos, somente um segmento faturável será creditado com a impressão.

   * **[!UICONTROL Content]:** use este relatório para entender a entrega de impressões e outras métricas por dimensões de conteúdo especificadas (como gênero, qualidade de produção e classificação de conteúdo), de modo que você possa otimizar o direcionamento e garantir a segurança da marca. Além das dimensões de conteúdo, o relatório inclui a maioria das dimensões, métricas e filtros padrão. Os dados por dimensão de conteúdo estão disponíveis para [!DNL Freewheel], [!DNL Index], [!DNL Magnite], [!DNL Microsoft], [!DNL Nexxen], [!DNL Pubmatic], [!DNL Sharethrough] e [!DNL Triplelift]. Os sinais de conteúdo são transmitidos pelos editores durante a transmissão de ofertas e estão sujeitos à disponibilidade.

   * **[!UICONTROL Conversion]:** Use este relatório para entender o desempenho de suas campanhas com base em métricas de conversão capturadas com o rastreamento de conversão do Adobe Advertising. Este relatório inclui atribuição multitoque.

   * **[!UICONTROL Custom Creative]:** (Somente anunciantes com o Advertising Creative) Use este relatório para monitorar o desempenho em suas experiências de anúncios do Advertising Creative.

   * **[!UICONTROL Device]:** Use este modelo pré-preenchido para ver as métricas principais por dimensões relacionadas ao dispositivo.

   * **[!UICONTROL Frequency (by Impression)]:** Use este relatório para entender a distribuição de impressões mostradas para visualizadores únicos (por exemplo, quantos visualizadores únicos viram uma impressão, duas impressões, três impressões e assim por diante). Os dados estão disponíveis por disposição ou campanha.

     >[!NOTE]
     >
     >* Os dados estarão disponíveis após 1 de março de 2019.
     >* A frequência é estimada com base em uma amostra de dados.
     >* Para alguns inventários, os editores não transmitem um identificador de dispositivo, o que impede o rastreamento de frequência. Este relatório inclui somente impressões para as quais um identificador de dispositivo estava disponível.

   * **[!UICONTROL Frequency (by App/Site)]:** Use este relatório para entender quantos usuários únicos seus anúncios atingiram por aplicativo ou por site. Você também pode ver quantos usuários únicos seus anúncios atingiram por meio de apenas um aplicativo ou site específico (&quot;usuários únicos distintos&quot;).

     >[!NOTE]
     >
     >* Os dados estarão disponíveis após 15 de novembro de 2018.
     >* Para alguns inventários privados, os editores não transmitem um identificador de dispositivo, o que impede o rastreamento de frequência.

   * **[!UICONTROL Geo]**: use este modelo pré-preenchido para ver as métricas principais por dimensões geográficas.

   * **[!UICONTROL Household Conversions]:** Use este relatório para ver conversões de view-through no nível doméstico com base no endereço IP, em vez de no nível do dispositivo/cookie. Use os insights para medir e otimizar o desempenho da campanha. Consulte &quot;[Perguntas frequentes sobre Relatórios do Agregado Doméstico](/help/dsp/reports/faq-reports.md)&quot; para obter mais informações. Os dados não estão disponíveis para posicionamentos que direcionam IDs universais.

   * **[!UICONTROL Household Reach & Frequency]:** use este relatório para ver as impressões, o alcance e a frequência de uma única dimensão em formatos de anúncio em um nível doméstico com base no endereço IP, em vez de em um nível de dispositivo/cookie. Use os insights para otimizar sua combinação de mídia, melhorar o desempenho e identificar oportunidades para alcance incremental. Consulte &quot;[Perguntas frequentes sobre Relatórios do Agregado Doméstico](/help/dsp/reports/faq-reports.md)&quot; para obter mais informações. Os dados não estão disponíveis para posicionamentos que direcionam IDs universais.

   * **[!UICONTROL Margin]:** Use este relatório para ver as métricas principais, como margem, lucro e outras métricas de gastos por campanha ou posicionamento. Os dados não estão disponíveis para posicionamentos que direcionam IDs universais.

   * **[!UICONTROL Path to Conversion]:** use este relatório para identificar como otimizar orçamentos e personalizar anúncios com base em sequências de interação de anúncios de melhor desempenho. O relatório mostra a sequência de pontos de interação na mesma família que resultam em cada uma das métricas de conversão selecionadas no intervalo de dados especificado. O relatório usa um período de lookback especificado entre a primeira interação e uma conversão e pode incluir uma dimensão:

      * [!UICONTROL Channel Assist Type]: Mostra como os seguintes canais de marketing auxiliaram o processo de conversão: [!UICONTROL Audio Impression], [!UICONTROL CTV Impression], [!UICONTROL Display Click], [!UICONTROL Display Impression], [!UICONTROL Native Click], [!UICONTROL Native Impression], [!UICONTROL Search Click], [!UICONTROL Video Click] ou [!UICONTROL Video Impression].

      * [!UICONTROL Campaign ID] ou [!UICONTROL Campaign Name]: mostra quais campanhas ajudaram no processo de conversão.

      * [!UICONTROL Ad ID] ou [!UICONTROL Ad Name] mostra quais anúncios do DSP resultaram em conversões.

      * [!UICONTROL Ad ID & Paid Keyword (SSC)] ou [!UICONTROL Ad Name & Paid Keyword (SSC)] mostra quais palavras-chave do Search, Social e Commerce resultaram em conversões.

     As colunas no relatório incluem de &quot;[!UICONTROL Event #1]&quot; a &quot;[!UICONTROL Event #10],&quot;[!UICONTROL Path Length],&quot; &quot;% \&lt;Nome da Métrica de Conversão 1\>,&quot; &quot;% \&lt;Nome da Métrica de Conversão 2\>&quot; e assim por diante.

     Até os 10 pontos de interação mais recentes são incluídos. As linhas de caminho são ordenadas pelo número de conversões.

     Para uma comparação deste relatório com relatórios criados por [!DNL Advanced Measurement Services] e o Adobe Analytics, consulte &quot;[Perguntas frequentes sobre Relatórios Personalizados](/help/dsp/reports/faq-reports.md).&quot;

   * **[!UICONTROL Path Length]:** use este relatório para rastrear o número de pontos de interação do usuário necessários para conversões ao longo do tempo, para que você possa escolher a frequência de anúncio ideal. O relatório mostra o número de conversões por comprimento de caminho (pontos de interação), por exemplo, quantas conversões ocorreram depois que os usuários tinham apenas uma interação de anúncio, duas interações de anúncio e assim por diante. O relatório pode incluir dados de várias métricas de conversão e usa um período de pesquisa especificado entre a primeira interação e uma conversão. As colunas no relatório incluem &quot;[!UICONTROL Path Length],&quot; &quot;[!UICONTROL Number of] \&lt;Nome da métrica de conversão 1\>,&quot; &quot;% \&lt;Nome da métrica de conversão 1\>,&quot; \&lt;Nome da métrica de conversão 2\>,&quot; &quot;% \&lt;Nome da métrica de conversão 2\>&quot; e assim por diante.

     Os dados são exibidos para cada comprimento de caminho de até 10; os dados para comprimentos de caminho superiores a 10 são agrupados.

   * **[!UICONTROL Segment]:** Use este modelo pré-preenchido para ver as métricas principais por segmento.

     >[!NOTE]
     >
     >* Este relatório tem como objetivo mostrar o desempenho de diferentes segmentos direcionados. Ele usa dados de associação de segmento. Quando uma impressão é transmitida a uma pessoa ou dispositivo pertencente a dois ou mais segmentos direcionados, este relatório inclui uma linha para cada segmento. Por esse motivo, os totais neste relatório podem não corresponder à entrega real.
     >* Métricas de conversão e dados de meta personalizados para segmentos estão disponíveis após 2 de agosto de 2019. Todos os outros dados para segmentos estarão disponíveis a partir de 1 de junho de 2018.

   * **[!UICONTROL Site]:** Por padrão, inclui métricas padrão, gasto líquido total de mídia e gasto líquido faturável total por site.

   * **[!UICONTROL Time to Conversion]:** Use este relatório para determinar a janela de retrospectiva de atribuição ideal e identificar campanhas com tempos mais longos de conversão, que podem se beneficiar do redirecionamento. O relatório mostra o número de conversões por duração em dias da última interação (exposição do anúncio ou clique) para conversão. O relatório pode incluir dados de várias métricas de conversão e usa um período de pesquisa especificado entre a primeira interação e uma conversão. As colunas no relatório incluem &quot;[!UICONTROL Time Taken (in days)],&quot; &quot;[!UICONTROL Number of] \&lt;Nome da métrica de conversão 1\>,&quot; &quot;% \&lt;Nome da métrica de conversão 1\>,&quot; \&lt;Nome da métrica de conversão 2\>,&quot; &quot;% \&lt;Nome da métrica de conversão 2\>&quot; e assim por diante. As conversões que demoram mais do que o período de lookback são agrupadas em uma linha (por exemplo, se o relatório usar um período de lookback de 30 dias, todas as conversões que demoram mais de 30 dias para ocorrer são agrupadas em uma linha com o valor &quot;[!UICONTROL Time Taken (in days)]&quot; de &quot;30+&quot;).

## Relatório entre contas {#cross-account-reporting}

Qualquer organização com várias contas do DSP pode, opcionalmente, ativar dados entre contas em relatórios personalizados, de acordo com as necessidades da organização. Por exemplo, você pode conceder acesso à Conta A aos dados da Conta B e conceder acesso à Conta B aos dados da Conta C (mas não da Conta A). Para habilitar e configurar esse recurso, entre em contato com a equipe de conta da Adobe.

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
>* [Perguntas Frequentes sobre Relatórios Domésticos](/help/dsp/reports/faq-reports.md)
>* [Tipos de Relatórios de Desempenho em Exibições de Gerenciamento de Campanha](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Colunas de Relatório Disponíveis](/help/dsp/reports/report-columns.md)
>* [Sobre [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
