---
title: '[!UICONTROL Forecast Accuracy (Actuals) Report]'
description: Saiba mais sobre o [!UICONTROL Forecast Accuracy (Actuals) Report], incluindo as colunas de dados.
exl-id: 659e11c7-5fed-4d91-a73f-7c435d36634f
feature: Search Reports, Search Model Accuracy Reports
TQID: https://experienceleague.adobe.com/wQyO42Dt5McqK23z-adEP-BAxxTrBk9RJi0I-4noP0I
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 318
ht-degree: 0%

---

# O [!UICONTROL Forecast Accuracy (Actuals) Report]

Esse relatório mostra a impressão real, os cliques, os dados de custo e receita da rede de anúncios por dia para cada portfólio.

## Colunas disponíveis

Veja a seguir as colunas que são incluídas automaticamente em cada relatório. Não é possível adicionar mais colunas.

| Coluna | Padrão? | Descrição |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | Padrão | O nome do grupo de portfólio ao qual o portfólio pertence. |
| [!UICONTROL Portfolio ID] | Padrão | A ID numérica do portfólio. |
| [!UICONTROL EF Portfolio Group ID] | Padrão | A ID numérica do grupo de portfólios ao qual o portfólio pertence. |
| [!UICONTROL Portfolio] | Padrão | O portfólio. |
| [!UICONTROL Portfolio Status] | Padrão | O status do portfólio:<ul><li><i>[!UICONTROL Optimize]:</i> O recurso de otimização está coletando dados de cliques e receita para as campanhas relevantes, modelando os dados usados para otimização e otimizando ofertas, orçamentos de campanha e metas de estratégia de oferta de campanha (dependendo do tipo de otimização e das estratégias de oferta).</li><li><i>[!UICONTROL Active]:</i> o recurso de otimização está coletando dados de cliques e receita para as campanhas relevantes e está modelando os dados, mas não está otimizando ofertas ou orçamentos de campanha.</li><li><i>[!UICONTROL Inactive]:</i> o recurso de otimização está coletando dados de cliques para as campanhas relevantes para fins de relatório, mas não está modelando os dados nem otimizando ofertas ou orçamentos de campanha. |
| [!UICONTROL Day of Week] | Padrão | O dia da semana relatado: <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i> ou <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Event Date] | Padrão | A data do relatório. |
| [!UICONTROL Device] | Padrão | (Google Ads, [!DNL LY Ads], Microsoft Advertising, Yahoo! Exibir campanhas Nativas da Rede e do Yahoo) O tipo de dispositivo no qual os anúncios foram exibidos: <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i> ou <i>[!UICONTROL N/A]</i> (sem valor). As linhas de outras redes de anúncios têm valores de <i>[!UICONTROL N/A]</i>.<br><br>Em campanhas de pesquisa, se os modelos de rastreamento ou as URLs de destino das palavras-chave, anúncios e/ou extensões de anúncios incluírem parâmetros para rastrear dados por dispositivo (<code>&amp;ev_dvc={device}&amp;ev_dvm={devicemodel}</code>) no momento em que o anúncio foi clicado, os dados de conversão também serão incluídos na linha para cada tipo de dispositivo. Caso contrário, se os dados de conversão não puderem ser atribuídos a um tipo de dispositivo, eles serão agregados em uma linha separada com um valor &quot;[!UICONTROL Device]&quot; de <i>[!UICONTROL N/A]</i>. |
| [!UICONTROL Revenue] | Padrão | A receita total. |
| [!UICONTROL Impressions] | Padrão | O total de impressões. |
| [!UICONTROL Clicks] | Padrão | O total de cliques. |
| [!UICONTROL Cost] | Padrão | O custo total. |

>[!MORELIKETHIS]
>
>* [Sobre relatórios de precisão de modelo](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [O [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [Gerar um relatório de precisão de modelo](model-accuracy-report-generate.md)
>* [Configurações do relatório de precisão do modelo](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
