---
title: Requisitos de dados para métricas de tráfego e conversão de  [!DNL Naver] contas somente de rastreamento
description: Referencie os requisitos de carregamento de dados para  [!DNL Naver] contas somente de rastreamento.
exl-id: cc8ee5de-2bf2-48fd-9fa7-28421aed673f
feature: Search Tools
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Requisitos de dados de métrica para [!DNL Naver] contas somente de rastreamento

A seguir estão os requisitos de dados para as métricas de tráfego e conversão do [!DNL Naver] para contas somente de rastreamento.

Os arquivos de dados devem estar no formato TSV, CSV ou TXT.

Os seguintes campos de cabeçalho são obrigatórios e opcionais. Cada linha de dados deve incluir um valor agregado diário para pelo menos um campo de métrica.

| Campo de cabeçalho/Nome da coluna | Tipo | Descrição |
| ---- | ---- | ---- |
| Período | DateTime | A data à qual os dados se aplicam, no formato `YYYY.MM.DD.` (como `2019.11.15.`, com um período após o dia). |
| Campaign | String que diferencia maiúsculas de minúsculas | O nome da campanha. |
| Adgroup (como uma palavra) | String que diferencia maiúsculas de minúsculas | O nome do grupo de anúncios. |
| Palavra-chave | String que diferencia maiúsculas de minúsculas | (Anúncios de palavra-chave) A palavra-chave que gerou o anúncio. |
| [Métrica] | Integer | (Opcional) O número de [qualquer que seja a métrica que está medindo].</br><br>As métricas padrão incluem Impressões, Custo e Cliques. É possível incluir qualquer métrica adicional desejada na rede de anúncios. Inclua cada métrica em uma coluna separada.<br><br><b>Notas:</b><ul><li>O cabeçalho da coluna para Custo deve ser &quot;Custo (KRW)&quot;.</li><li>Para incluir o Custo (KRW) para anúncios de marca, divida manualmente o custo mensal fixo por dia no nível do grupo de anúncios.</li><li>Remova todas as vírgulas dos valores de métricas padrão. Por exemplo, use 1000 em vez de 1.000.</li><li>Para valores nulos, use 0.</li></ul> |

>[!MORELIKETHIS]
>
>* [Implementar [!DNL Naver] contas somente de rastreamento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Apêndice - Dados de bulksheet necessários para  [!DNL Naver] contas](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [Carregar métricas de tráfego e conversão para [!DNL Naver] contas somente de rastreamento](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
