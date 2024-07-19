---
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---
# Definição do sufixo de URL final

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]:** contas ([!DNL Google Ads] e [!DNL Microsoft Advertising] somente; opcional) Quaisquer parâmetros a serem anexados ao final das URLs finais para rastrear informações; inclua todos os parâmetros que sua empresa deve rastrear. Exemplo:`param1=value1&param2=value2`

Em contas que usam o rastreamento de conversão de Adobe Advertising, o sufixo deve incluir o identificador de cliques da rede de publicidade (`msclkid` para [!DNL Microsoft Advertising]; `gclid` para [!DNL Google Ads]).

Contas com uma integração do Adobe Analytics devem usar o parâmetro [AMO ID](/help/integrations/analytics/ids.md). Se a conta tiver uma implementação de ID do AMO do lado do servidor, o parâmetro será adicionado automaticamente quando um usuário clicar em um anúncio. Caso contrário, você deverá adicioná-lo manualmente aqui. Consulte os [formatos de sufixo obrigatórios para [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) e [formatos de sufixo obrigatórios para [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Este campo não é atualizado pela configuração de rastreamento [!UICONTROL Auto Upload].
>* Os sufixos de URL finais nos níveis inferiores substituem o sufixo de nível de conta. Para facilitar a manutenção, use somente o sufixo no nível da conta, a menos que seja necessário um rastreamento diferente para componentes de conta individuais. Para configurar um sufixo no nível do grupo de anúncios ou inferior, use o editor da rede de anúncios.
