---
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---
# Anexar o campo Parâmetros nas configurações da conta e da campanha

**[!UICONTROL Append Parameters]:** (Opcional) Quaisquer parâmetros de rastreamento adicionais a serem anexados às URLs de base.<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. Os parâmetros de acréscimo no nível do anunciante são incluídos por padrão no nível da conta e no nível da campanha, mas você pode substituir ambos.

Você pode usar qualquer cadeia de caracteres de texto estático, incluindo parâmetros de rastreamento de terceiros, ou qualquer um dos [parâmetros de rastreamento compatíveis](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md), que inserem um valor de dados apropriado na URL base.

Separe vários parâmetros com vírgulas ou sinal gráfico (&amp;). Colchetes aninhados não são suportados.

**Notas:**

* As alterações nos parâmetros de acréscimo não são controladas pela opção [!UICONTROL Auto Upload]. Se você alterar os parâmetros de acréscimo para URLs base existentes, os novos URLs não serão gerados automaticamente. Adicione os novos parâmetros baixando um arquivo de bulksheet para a conta ou campanha, atualizando os campos [!UICONTROL Base URL/Final URL] e, em seguida, carregando e lançando a bulksheet.

* (Adicione redes com rastreamento paralelo) Evite usar macros, que não são substituídas por cliques de fontes que permitem rastreamento paralelo. Se o anunciante precisar usar macros, a Equipe de conta do Adobe deverá trabalhar com o Suporte ao cliente ou a equipe de implementação para adicioná-las.

* (Anunciantes com integração Adobe Advertising-Adobe Analytics) Para incluir um parâmetro de ID AMO para enviar dados de Pesquisa, Social e Commerce para [!DNL Analytics], consulte os [formatos específicos de rede de anúncios](/help/integrations/analytics/ids.md#amo-id-formats). Não é necessário adicionar manualmente o parâmetro para contas do [!DNL Google Ads] e do [!DNL Microsoft Advertising] com uma implementação de ID do AMO do lado do servidor.
