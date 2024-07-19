---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---
# Camada 2 - Campos de camada 8 em modelos de anúncios de compras

**[!UICONTROL Tier  2 - Tier 8]:** (Ao adicionar camadas de grupos de produtos) Um tipo de atributo de produto pelo qual direcionar produtos e os critérios de qualificação para o tipo de atributo selecionado (por exemplo, Brand=Acme ou Condition=New). Os valores são aplicados hierarquicamente para determinar os produtos elegíveis. Selecione um tipo de atributo e informe os critérios de qualificação. Os caracteres proibidos incluem o seguinte: `[ ] < > >>` (dois sinais consecutivos de &quot;maior que&quot;), que são usados para designar nomes de colunas no modelo, nomes de modificadores no modelo e separadores de camada na coluna [!UICONTROL Parent Product Grouping] em bulksheets.

É possível incluir até oito camadas (níveis) de grupos de produtos, incluindo &quot;[!UICONTROL All Products]&quot; (Camada 1). Cada camada pode incluir vários grupos de produtos, mas eles devem pertencer ao mesmo tipo de atributo (como &quot;Condição&quot;).

>[!NOTE]
>
>* ([!DNL Google Ads] somente) Os valores possíveis para [!UICONTROL Channel] são &quot;[!UICONTROL Local]&quot; ou &quot;[!UICONTROL Online]&quot;, e os valores possíveis para [!UICONTROL ChannelExclusivity] são &quot;[!UICONTROL SingleChannel]&quot; e &quot;[!UICONTROL MultiChannel].&quot;
>* Ao criar um grupo de produtos de segunda camada (filho) para um grupo de anúncios na guia [!UICONTROL Product Groups] da exibição [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns], outro grupo de produtos, chamado &quot;[!UICONTROL Everything Else]&quot;, é criado automaticamente usando a oferta padrão do grupo de anúncios. Usando modelos de feed de estoque, no entanto, &quot;[!UICONTROL Everything Else]&quot; grupos de produtos foram excluídos.
>* Quando você inclui vários níveis e nenhum valor está disponível para o nível final (com a numeração mais alta), o próximo nível mais alto é usado como o grupo de produtos licitáveis. Por exemplo, se você incluir cinco níveis e nenhum valor estiver disponível para o Nível 5, o Nível 4 será usado como o grupo de produtos licitáveis (unidade). No entanto, se nenhum valor estiver disponível para uma camada intermediária, a linha será ignorada. Por exemplo, se você incluir cinco camadas e a Camada 5 tiver um valor, mas a Camada 4 não, a Linha 4 será ignorada.
