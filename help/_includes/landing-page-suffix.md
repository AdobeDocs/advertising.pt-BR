---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---
# Campo Sufixo da página inicial nas configurações da conta GL e MS, configurações de campanha e algumas configurações de anúncios

**[!UICONTROL Landing Page Suffix]:** ([!DNL Google Ads] e [!DNL Microsoft Advertising] somente contas do; opcional) Quaisquer parâmetros a serem anexados ao final dos URLs finais para rastrear informações; inclua todos os parâmetros que sua empresa deve rastrear. Exemplo: `param1=value1&param2=value2`

As contas que usam o rastreamento de conversão de anúncio do Adobe devem incluir o identificador de cliques da rede de publicidade (`gclid` para [!DNL Google Ads] ou `msclkid` para [!DNL Microsoft Advertising]) no sufixo.

As contas com uma integração do Adobe Analytics devem usar o parâmetro s_kwcid. Se a conta tiver uma implementação s_kwcid do lado do servidor, o parâmetro será adicionado automaticamente quando um usuário clicar em um anúncio. Caso contrário, você deverá adicioná-lo manualmente aqui. Consulte a [formatos de sufixo obrigatórios para o Google Ads](/help/search-social-commerce/tracking/formats-click-tracking-google.md) e [formatos de sufixo obrigatórios para a Microsoft Advertising](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

**Notas:**

* Este campo não é atualizado pelo [!UICONTROL Auto Upload] configuração de rastreamento.

* Os sufixos de página de aterrissagem em níveis inferiores substituem o sufixo de nível de conta. Para facilitar a manutenção, use somente o sufixo no nível da conta, a menos que seja necessário um rastreamento diferente para componentes de conta individuais. Para configurar um sufixo no nível do grupo de anúncios ou inferior, use o editor da rede de anúncios.
