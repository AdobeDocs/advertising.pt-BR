---
title: '[!UICONTROL Label Classification Report]'
description: Saiba mais sobre o [!UICONTROL Label Classification Report].
exl-id: 847fa384-b9c6-446f-9ebf-da7679ed35ae
feature: Search Reports, Search Basic Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# [!UICONTROL Label Classification Report]

O [!UICONTROL Label Classification Report] inclui dados de custo, clique e conversão (opcionalmente) por classificação de rótulo em nível de palavra-chave ou nível de anúncio agregada em redes de anúncios, contas, campanhas ou grupos de anúncios. Por padrão, os dados incluem uma linha para cada classificação de rótulo no nível de palavra-chave aplicável para palavras-chave, anúncios e posicionamentos que receberam impressões para cada unidade de tempo no intervalo de datas especificado. As linhas estão em ordem crescente, primeiro pela data de início da unidade de tempo, depois por classificação de etiqueta e, em seguida, pelo valor da etiqueta, por padrão.

Você pode exibir dados dos últimos 36 meses.

>[!NOTE]
>
>* Relatórios por classificações de rótulo no nível de anúncio não estão disponíveis para [!DNL Microsoft Advertising] campanhas de anúncio de pesquisa dinâmica (DSA).
>* Mais de uma classificação de etiqueta pode ser aplicada à mesma entidade, portanto, o total de cada métrica pode ser maior que o total real da entidade. Por exemplo, digamos que a palavra-chave &quot;sapatos de camurça&quot; tenha dois valores de etiqueta, &quot;camurça&quot; e &quot;calçado&quot;, e a palavra-chave recebeu 100 cliques. A coluna Clicks mostraria &quot;100&quot; para cada um desses valores de rótulo, portanto, o total para ambas as linhas seria &quot;200&quot;.
* Quaisquer alterações feitas em classificações de rótulo e nos valores de rótulo filho de uma entidade serão visíveis em cerca de uma hora.

## Colunas padrão

Para obter descrições de todas as colunas padrão e personalizadas, consulte &quot;[Colunas de relatório para relatórios básicos e avançados](basic-advanced-report-columns.md)&quot;.

* [!UICONTROL Label Classification]
* [!UICONTROL Label Value]
* [!UICONTROL Start Date]
* [!UICONTROL End Date]
* [!UICONTROL Impressions]
* [!UICONTROL Cost]
* [!UICONTROL Clicks]
* [!UICONTROL CPC]
* [!UICONTROL Avg Position]
* [!UICONTROL Impr. (Abs. Top) %]
* [!UICONTROL Impr. (Top) %]

>[!MORELIKETHIS]
>
>* [Sobre relatórios básicos e avançados](basic-advanced-report-about.md)
>* [Gerar um relatório básico ou avançado](basic-advanced-report-generate.md)
>* [Configurações básicas e avançadas de relatório](basic-advanced-report-settings.md)
