---
source-git-commit: bef353542ee73d32b8ac53e6abd3265528be154f
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---
# Campo de carregamento automático nas configurações da conta e da campanha

**[!UICONTROL Auto Upload]:** (Somente para campanhas sincronizadas com [!UICONTROL EF Redirect]) Carrega automaticamente os itens a seguir na rede de publicidade na próxima vez que o Search, Social e Commerce for sincronizado com ele: (a) Parâmetros de rastreamento do Search, Social e Commerce para modelos de rastreamento e os mesmos parâmetros anexados às URLs finais ou (b) novas URLs de destino incorporadas ao código de rastreamento do Search, Social e Commerce. Para anunciantes com uma [integração Adobe Advertising-Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=pt-BR) e uma configuração de ID AMO do lado do servidor (s_kwcid), o carregamento também inclui [parâmetros de ID do AMO](/help/integrations/analytics/ids.md#amo-id) para suas contas do [!DNL Google Ads] e do [!DNL Microsoft Advertising]. A configuração padrão no nível da conta é herdada das configurações de rastreamento do anunciante. Você pode substituir a configuração no nível da conta no nível da campanha.

**Observação:** as URLs de rastreamento são atualizadas diariamente apenas para entidades que estão fora de sincronia (ou seja, novas entidades que foram adicionadas e entidades existentes cujas propriedades foram alteradas). Portanto, se você alterar essa configuração de desativado para ativado para um anunciante/conta/campanha existente, os URLs de rastreamento não serão atualizados para entidades existentes que já estão em sincronia. Para adicionar rastreamento aos URLs de entidades em sincronia existentes, entre em contato com a Equipe de conta do Adobe e solicite um processo de sincronização manual e único. O processo de upload automático lidará com alterações futuras.
