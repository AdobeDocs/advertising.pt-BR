---
title: '[!UICONTROL AdWords Shopping Performance Report]'
description: Saiba mais sobre o [!UICONTROL AdWords Shopping Performance Report].
feature: Search Reports, Search Specialty Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
  - id: 7de556b7-2c2a-599d-853b-8c282aafa6e3
    internal-label: Search Specialty Reports
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%
---
# [!UICONTROL AdWords Shopping Performance Report]

*[!DNL Google Ads]somente contas*

O [!UICONTROL AdWords Shopping Performance Report] inclui dados de custo, clique e impressão; dados de clique e conversão convertidos rastreados pelo [!DNL Google Ads Conversion Optimizer]; e (opcionalmente) dados de conversão rastreados por [!DNL Adobe] e dados de métrica derivada agregados no nível de ID do produto para um ou mais grupos de anúncios em campanhas de compras. Por padrão, os dados incluem uma linha para cada ID de produto e categoria de produto por grupo de publicidade para cada unidade de tempo no intervalo de datas especificado. As linhas estão em ordem crescente pelo nome da conta, nome da campanha e nome do grupo de anúncios por padrão.

Você pode exibir dados dos dois meses anteriores. Os dados anteriores a 21 de setembro de 2018 podem ser exibidos em duas linhas: uma linha com dados de custo e clique e uma linha com dados de conversão rastreados pelo Adobe. Os dados subsequentes são mostrados em uma linha.

>[!NOTE]
>
>* Se o produto incluir a coluna [!UICONTROL Product Category] e um produto aparecer em várias categorias, o produto aparecerá em várias linhas e a contagem de conversão será duplicada em cada uma das linhas aplicáveis. Como os totais de dados de conversão não são precisos, classifique os dados por categoria somente para obter uma compreensão geral de como as conversões estão em tendência por categoria.
>* Os dados deste relatório são extraídos para o dia anterior às 23:00 (23:00) diariamente. Por exemplo, às 23h de 18 de junho, ele extrai dados para 17 de junho. Se você executar o relatório em 19 de junho às 09:00 — antes que os dados de 18 de junho sejam extraídos — o relatório incluirá os dados até 17 de junho às 23:00.

## Colunas padrão

Para obter descrições de todas as colunas padrão e personalizadas, consulte &quot;[Colunas de relatório para relatórios especializados](specialty-report-columns.md)&quot;.

* [!UICONTROL Account Name]
* [!UICONTROL Campaign Name]
* [!UICONTROL Ad Group Name]
* [!UICONTROL Product ID]
* [!UICONTROL Category (1st level - 5th level)]
* [!UICONTROL Product Type (1st level - 5th level)]
* [!UICONTROL Start Date]
* [!UICONTROL End Date]
* [!UICONTROL Impressions]
* [!UICONTROL Clicks]
* [!UICONTROL Cost]
* [!UICONTROL Google Converted Clicks]
* [!UICONTROL Google Conversions]
* [!UICONTROL CTR]
* [!UICONTROL CPC]

>[!MORELIKETHIS]
>
>* [Sobre relatórios especializados](specialty-report-about.md)
>* [Gerenciar relatórios agendados](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [Configurações do relatório de especialidades](specialty-report-settings.md)
