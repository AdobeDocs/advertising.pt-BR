---
title: '[!UICONTROL Forecast Accuracy (Actuals) Report]'
description: Saiba mais sobre o [!UICONTROL Forecast Accuracy (Actuals) Report], incluindo as colunas de dados.
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: bfca434eacf52ec7236804c54b7740442aa12961
workflow-type: tm+mt
source-wordcount: '319'
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
| [!UICONTROL Device] | Padrão | (Google Ads, Microsoft Advertising, Yahoo! Rede de exibição, Yahoo! Anúncios do Japão e campanhas nativas do Yahoo) O tipo de dispositivo no qual os anúncios foram exibidos: <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i> ou <i>[!UICONTROL N/A]</i> (sem valor). As linhas de outras redes de anúncios têm valores de <i>[!UICONTROL N/A]</i>.<br><br>Em campanhas de pesquisa, se os modelos de rastreamento ou as URLs de destino das palavras-chave, anúncios e/ou extensões de anúncios incluírem parâmetros para rastrear dados por dispositivo (<code>&amp;ev_dvc={device}&amp;ev_dvm={devicemodel}</code>) no momento em que o anúncio foi clicado, os dados de conversão também serão incluídos na linha para cada tipo de dispositivo. Caso contrário, se os dados de conversão não puderem ser atribuídos a um tipo de dispositivo, eles serão agregados em uma linha separada com um valor &quot;[!UICONTROL Device]&quot; de <i>[!UICONTROL N/A]</i>. |
| [!UICONTROL Revenue] | Padrão | A receita total. |
| [!UICONTROL Impressions] | Padrão | O total de impressões. |
| [!UICONTROL Clicks] | Padrão | O total de cliques. |
| [!UICONTROL Cost] | Padrão | O custo total. |

>[!MORELIKETHIS]
>
>* [Sobre relatórios de precisão de modelo](model-accuracy-report-about.md)
>* [O [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [Gerenciar relatórios agendados](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [Configurações do relatório de precisão do modelo](model-accuracy-report-settings.md)
