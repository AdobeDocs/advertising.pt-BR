---
title: Sobre públicos
description: Saiba mais sobre as opções para rastrear, criar e gerenciar públicos-alvo de  [!DNL Google Ads]  e  [!DNL Microsoft Advertising] .
exl-id: f85cbc82-ddbc-4ecd-a17b-b4cb4808cfbc
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Sobre o gerenciamento de [!DNL Google Ads] e [!DNL Microsoft Advertising] públicos-alvo em Pesquisa, Social e Commerce

*[!DNL Google Ads]e [!DNL Microsoft Advertising] somente*

A Biblioteca de Públicos-alvo lista todos os seus públicos-alvo do [!DNL Google Ads] baseados em dados do cliente, no mercado e semelhantes, e os públicos-alvo de remarketing e remarketing dinâmico do [!DNL Microsoft Advertising], personalizado, correspondência do cliente, no mercado e semelhantes. Você pode usar qualquer um dos públicos-alvo de [!DNL Google Ads] como exclusões e destinos de nível de campanha e de nível de grupo de anúncios [!DNL Google Ads] e pode usar qualquer um dos públicos-alvo de [!DNL Microsoft Advertising] como exclusões e destinos de nível de campanha e de nível de grupo de anúncios (somente públicos de remarketing dinâmicos). [!DNL Microsoft Advertising] É possível adicionar ou editar um ajuste de oferta para qualquer meta de público-alvo.

Você também pode criar e gerenciar públicos-alvo usando segmentos ou listas de email de seus públicos-alvo existentes da Adobe Experience Cloud e de vários tipos de dados do cliente de seu sistema de gerenciamento de relacionamento com o cliente (CRM):

* **Segmentos de público-alvo do Adobe:** anunciantes com contas Adobe Audience Manager ou Adobe Analytics aceitas podem criar [!DNL Google Ads] públicos-alvo de correspondência do cliente a partir de seus [!DNL Adobe] segmentos:

   * (Anunciantes com contas do [!DNL Analytics] que também não têm o Audience Manager) Você pode criar [!DNL Google Ads] públicos-alvo de correspondência do cliente usando IDs de usuário de [!DNL Analytics] segmentos que são compartilhados com o Adobe Experience Cloud.

   * (Anunciantes com contas Audience Manager) Você pode criar [!DNL Google Ads] públicos-alvo de correspondência de clientes usando IDs de usuários dos segmentos Audience Manager que têm Pesquisa, Social e Commerce como destino. Isso pode incluir segmentos do Adobe Analytics publicados na Adobe Experience Cloud e segmentos criados usando a Biblioteca de público-alvo da Adobe Experience Cloud.

  Para criar públicos-alvo de correspondência do cliente, a conta [!DNL Google Ads] do anunciante deve ser [qualificada para correspondência personalizada](https://support.google.com/adspolicy/answer/6299717) e aceita a inclusão de [segmentos de ID de usuário](https://support.google.com/google-ads/answer/9199250). Além disso, a conta do anunciante em Search, Social e Commerce deve ser configurada para permitir a criação de públicos-alvo de correspondência do cliente.

  [!DNL Adobe] dados de segmento e arquivos de sincronização de cookies para públicos com base em dados do cliente são sincronizados com [!DNL Google Ads] diariamente.

* **Listas de email do Adobe Campaign:** A sua equipe de conta do Adobe pode ajudá-lo a configurar um fluxo de trabalho para criar e atualizar uma audiência de correspondência com o cliente [!DNL Google Ads] de uma lista de email no [!DNL Campaign].

* **Listas de dados do cliente:** anunciantes com contas [!DNL Google Ads] ou [!DNL Microsoft Advertising] qualificados para correspondência do cliente podem criar e atualizar um público-alvo baseado em dados do cliente específico da rede de anúncios &lt;!— ou público de remarketing dinâmico — incluído no público com base em dados do cliente, pelo menos para [!DNL Google Ads]?—> carregando um arquivo CSV com identificadores primários.

* **Listas de remarketing dinâmicas:** anunciantes com contas do [!DNL Microsoft Advertising] podem criar e gerenciar públicos de remarketing dinâmicos, que você pode usar para redirecionar clientes em potencial que tenham interagido recentemente com seus produtos de várias maneiras (como visualizadores de produtos ou compradores anteriores). Os públicos de remarketing dinâmicos exigem que você use a tag de rastreamento de conversão e público-alvo do JavaScript da rede de anúncios em suas páginas da Web. Use listas de remarketing dinâmicas com campanhas de compras nas redes de pesquisa e público-alvo para redirecionar públicos-alvo com anúncios de produtos, bem como com campanhas de pesquisa para redirecionar públicos-alvo com anúncios de texto e anúncios de pesquisa dinâmicos. <!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >Os modificadores de oferta para públicos alvo de remarketing dinâmico não são otimizados em portfólios com a configuração &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

>[!NOTE]
>
>O Search, Social e Commerce não armazena dados de clientes que você carrega ou que sejam dos [!DNL Adobe] segmentos usados para criar ou editar um público-alvo do [!DNL Google Ads] ou do [!DNL Microsoft Advertising].

>[!MORELIKETHIS]
>
>* [Criar [!DNL Google Ads] públicos-alvo de correspondência do cliente de [!DNL Adobe] públicos-alvo](google-audience-from-adobe-audience.md)
>* [Criar um [!DNL Google Ads] público-alvo de correspondência do cliente a partir de uma lista de emails do Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Gerenciar públicos-alvo de correspondência do cliente usando listas de dados do cliente](audience-from-customer-data-list.md)
>* [Gerenciar públicos de remarketing dinâmicos](audience-dynamic-remarketing-manage.md)
>* [Gerenciar metas de público-alvo para campanhas e grupos de anúncios](audience-targets-manage.md)
>* [Gerenciar exclusões de público alvo para campanhas e grupos de anúncios](audience-exclusions-manage.md)
