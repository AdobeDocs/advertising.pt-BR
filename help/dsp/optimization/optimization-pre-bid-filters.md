---
title: Filtros pré-oferta no nível de posicionamento e como usá-los
description: Faça referência aos filtros de pré-oferta em nível de posicionamento disponíveis e veja como usá-los.
feature: DSP Optimization
exl-id: 34a15666-7ca2-416d-9064-8638ca81e5b3
TQID: https://experienceleague.adobe.com/3-OOibzlRa5ethq6xkaHBngX2kwENFWhCSA-qzJQ-h4
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: af280ddc-b4d0-4416-86be-8f3ea3c6ebe7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 452
ht-degree: 0%

---

# Filtros pré-oferta no nível de posicionamento e como usá-los

| Filtro pré-oferta | Descrição | Quando usar este filtro |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | Define um limite de previsão mínimo para a probabilidade de um leilão resultar em um click-through. Por exemplo, se o limite for definido como 0,1%, você só dará lances em leilões quando a probabilidade prevista de um clique for maior ou igual a 0,1%.<br><br><b>Observação:</b> filtros são aplicados antes das metas de otimização. Como resultado, filtros muito rigorosos podem evitar gastos. | Use quando você tiver uma meta mínima de KPI para a taxa de cliques (CTR) e não quiser gastar seu orçamento quando o CTR estiver abaixo do limite. Esse filtro pode ser bastante restritivo, portanto, é importante definir metas realistas. Dependendo de outras restrições na colocação, uma meta de 0,03 a 0,07% geralmente é um bom ponto de partida. Você pode otimizar isso no nível do site, conforme necessário, para ajudar a melhorar as métricas.<br><br>Se o objetivo for atingir um CTR mínimo e a melhor CPM possível, a configuração recomendada é combinar um filtro [!UICONTROL Click Through Rate] com a meta de otimização &quot;[!UICONTROL Lowest CPM].&quot; Se sua meta for uma CPM máxima sem nenhum benefício real para ultrapassar e um CTR mínimo, emparelhar um filtro [!UICONTROL Click Through Rate] com a meta de otimização &quot;[!UICONTROL Always Max Bid + Highest CTR]&quot; poderá ser mais apropriado. |
| [!UICONTROL 100% Completion Rate] | Define uma taxa de conclusão mínima necessária que deve ser atingida antes que você lance uma impressão. | Use esse filtro quando a meta principal da campanha for taxas de conclusão. Fator em outros parâmetros de direcionamento, mas 65% é a porcentagem inicial recomendada. |
| [!UICONTROL Player Size - Adobe] | Define um tamanho mínimo de player necessário, usando dados da DSP. Você pode gerar uma impressão quando o limite de [!UICONTROL Player Size] for atingido. | Use o para garantir que você esteja fornecendo um inventário completo do player usando dados da DSP. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Define um tamanho mínimo de player necessário, usando dados de [!DNL Moat] ou [!DNL Integral Ad Science] ([!DNL IAS]). Você pode gerar uma impressão quando o limite de [!UICONTROL Player Size] for atingido. | Use para garantir que você esteja fornecendo um inventário completo do player usando dados [!DNL Moat] ou [!DNL IAS] de toda a plataforma.<br><br><b>Observação:</b> use este filtro somente quando a campanha estiver configurada para usar os dados [!DNL Moat] ou [!DNL IAS]. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Define uma porcentagem mínima necessária de visibilidade, usando números e medidas de visibilidade do DSP. Você pode licitar em uma impressão quando o limite especificado for atingido.<br><br><b>Notas:</b><ul><li>Se a configuração [!UICONTROL Viewability Sensitivity] da campanha for &quot;[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]&quot;, o padrão de medição de visibilidade [!DNL Media Rating Council] (MRC) será usado para a campanha. Se a configuração [!UICONTROL Viewability Sensitivity] for &quot;[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]&quot;, o padrão de medição de visibilidade [!DNL GroupM] será usado para a campanha.</li><li>As definições de medição do Adobe diferem das definições de terceiros, portanto, pode haver pequenas discrepâncias com dados de terceiros.</li></ul> | A prática recomendada é corresponder a meta de otimização e qualquer configuração de filtro de pré-oferta com a configuração [!UICONTROL Viewability Sensitivity] da campanha. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Como a DSP otimiza suas campanhas](optimization-how-dsp-optimizes-campaigns.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Configurações da campanha](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Metas de otimização e como usá-las](optimization-goals.md)
