---
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---
# Campo de carregamento automático nas configurações da conta e da campanha

**[!UICONTROL Auto Upload]:** (Para campanhas sincronizadas com o [!UICONTROL EF Redirect] somente) Carrega automaticamente o seguinte conteúdo na rede de publicidade na próxima vez que o Search, Social e Commerce for sincronizado com ele: (a) Parâmetros de rastreamento de Search, Social e Commerce para modelos de rastreamento e os mesmos parâmetros anexados aos URLs finais ou (b) novos URLs de destino incorporados ao código de rastreamento de Search, Social e Commerce. Para anunciantes com uma [Integração Adobe Advertising-Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) e uma configuração de ID do AMO do lado do servidor (s_kwcid), o upload também inclui parâmetros de ID do AMO para o [!DNL Google Ads] e [!DNL Microsoft Advertising] contas. A configuração padrão no nível da conta é herdada das configurações de rastreamento do anunciante. Você pode substituir a configuração no nível da conta no nível da campanha.

**Nota:** Os URLs de rastreamento são atualizados diariamente apenas para entidades que estão fora de sincronia (ou seja, novas entidades que foram adicionadas e entidades existentes cujas propriedades foram alteradas). Portanto, se você alterar essa configuração de desativado para ativado para um anunciante/conta/campanha existente, os URLs de rastreamento não serão atualizados para entidades existentes que já estão em sincronia. Para adicionar rastreamento aos URLs de entidades em sincronia existentes, entre em contato com a Equipe de conta do Adobe e solicite um processo de sincronização manual e único. O processo de upload automático lidará com alterações futuras.
