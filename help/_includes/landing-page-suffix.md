---
source-git-commit: a1a8c1b563d419090ddbefacc55be869c1ee7bcf
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---
# Campo Sufixo da página inicial nas configurações da conta GL e MS, configurações de campanha e algumas configurações de anúncios

**[!UICONTROL Landing Page Suffix]:** contas ([!DNL Google Ads] e [!DNL Microsoft Advertising] somente; opcional) Quaisquer parâmetros a serem anexados ao final das URLs finais para rastrear informações; inclua todos os parâmetros que sua empresa deve rastrear. Exemplo: `param1=value1&param2=value2`

As contas que usam o rastreamento de conversão de Adobe Advertising devem incluir o identificador de cliques da rede de publicidade (`gclid` para [!DNL Google Ads] ou `msclkid` para [!DNL Microsoft Advertising]) no sufixo.

As contas com uma integração do Adobe Analytics devem usar o parâmetro s_kwcid. Se a conta tiver uma implementação s_kwcid do lado do servidor, o parâmetro será adicionado automaticamente quando um usuário clicar em um anúncio. Caso contrário, você deverá adicioná-lo manualmente aqui. Consulte os [formatos de sufixo obrigatórios para o Google Ads](/help/search-social-commerce/tracking/formats-click-tracking-google.md) e [formatos de sufixo obrigatórios para o Microsoft Advertising](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

**Notas:**

* Este campo não é atualizado pela configuração de rastreamento [!UICONTROL Auto Upload].

* Os sufixos de página de aterrissagem em níveis inferiores substituem o sufixo de nível de conta. Para facilitar a manutenção, use somente o sufixo no nível da conta, a menos que seja necessário um rastreamento diferente para componentes de conta individuais. Para configurar um sufixo no nível do grupo de anúncios ou inferior, use o editor da rede de anúncios.
