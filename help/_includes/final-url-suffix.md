---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---
# Definição do sufixo de URL final

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]:** ([!DNL Google Ads] e [!DNL Microsoft Advertising] somente contas do; opcional) Quaisquer parâmetros a serem anexados ao final dos URLs finais para rastrear informações; inclua todos os parâmetros que sua empresa deve rastrear. Exemplo:`param1=value1&param2=value2`

Em contas que usam o rastreamento de conversão de Adobe, o sufixo deve incluir o identificador de cliques da rede de publicidade (`msclkid` para [!DNL Microsoft Advertising]; `gclid` para [!DNL Google Ads]).

As contas com uma integração do Adobe Analytics devem usar o parâmetro s_kwcid. Se a conta tiver uma implementação s_kwcid do lado do servidor, o parâmetro será adicionado automaticamente quando um usuário clicar em um anúncio. Caso contrário, você deverá adicioná-lo manualmente aqui. Consulte a [formatos de sufixo obrigatórios para [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) e [formatos de sufixo obrigatórios para [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Este campo não é atualizado pelo [!UICONTROL Auto Upload] configuração de rastreamento.
>* Os sufixos de URL finais nos níveis inferiores substituem o sufixo de nível de conta. Para facilitar a manutenção, use somente o sufixo no nível da conta, a menos que seja necessário um rastreamento diferente para componentes de conta individuais. Para configurar um sufixo no nível do grupo de anúncios ou inferior, use o editor da rede de anúncios.

