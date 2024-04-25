---
title: Gerar um URL de rastreamento de cliques
description: Saiba como gerar manualmente um URL de rastreamento de cliques do Search, Social e Commerce.
exl-id: 43a36869-146a-4c5f-b4f2-eddfb856480b
feature: Search Tools, Search Tracking
source-git-commit: a4d892b413dde26a96f03c797991c4df17da7562
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Gerar um URL de rastreamento de cliques de Pesquisa, Social e Comércio usando a ferramenta URLs de rastreamento

*Anunciantes com rastreamento de conversão de Adobe Advertising somente*

Para obter informações sobre quando você deve gerar e implementar manualmente um URL de rastreamento de cliques, consulte &quot;[Quando e como gerar URLs de rastreamento de cliques](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).&quot;

>[!NOTE]
>
>Esse recurso não implementa o modelo de rastreamento ou a URL de destino na conta de anúncio relevante.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**.

1. Selecione a conta da rede de publicidade na lista.

   ([!DNL Google Ads] palavras-chave; texto, instalação de aplicativos móveis e anúncios de pesquisa dinâmica; inserções; sitelinks; e grupos de produtos) As tags de rastreamento para o campo de modelo de rastreamento são exibidas. Eles não incluem parâmetros de acréscimo no nível da conta. Pule para a Etapa 4.

   Para todos os outros tipos de tags, insira informações para gerar uma tag.

1. (Se necessário) Gere uma tag:

   1. Especifique as páginas de aterrissagem, com sitelinks ou nomes de produtos, quando solicitado, de uma das seguintes maneiras:

      * Especifique um arquivo contendo as informações inserindo o caminho completo e o nome do arquivo ou clicando em **[!UICONTROL Browse]** para localizar o arquivo no dispositivo ou na rede. O arquivo deve ser um arquivo de texto delimitado por tabulação com um item por linha no seguinte formato:

         * (Criativos, Anúncios padrão) `**landing_page**`

           onde `landing_page` é um URL de página de aterrissagem ou URL de base válido.

           Exemplo: http://www.example.com/travel.html

         * ([!DNL Microsoft® Advertising] sitelinks) `sitelink <tab> ** <tab> landing_page`

           onde `sitelink` é o nome do sitelink e `landing_page` é um URL de página de aterrissagem ou URL de base válido.

           Exemplo: `Careers <tab> ** <tab> http://www.example.com/careers.html`

           O arquivo pode incluir até 10.000 linhas.

         * ([!DNL Google Merchant Center] grupos de produtos e [!DNL Microsoft® Advertising] anúncios de produto) `product name <tab> ** <tab> landing_page`

           onde `product name` é o nome e `landing_page` é um URL de página de aterrissagem ou URL de base válido.

           Exemplo: `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           O arquivo pode incluir até 10.000 linhas.

      * No campo de entrada, insira um item por linha no seguinte formato:

         * (Criativos, Anúncios padrão) `landing_page`

           onde `landing_page` é um URL de página de aterrissagem ou URL de base válido.

           Exemplo: http://www.example.com/travel.html

         * ([!DNL Microsoft® Advertising] sitelinks) `sitelink**landing_page`

           onde `sitelink` é o nome do sitelink e `landing_page` é um URL de página de aterrissagem ou URL de base válido.

           Exemplo: `Careers**http://www.example.com/careers.html`

         * ([!DNL Google Merchant Center] grupos de produtos e [!DNL Microsoft® Advertising] anúncios de produto) `product name**landing_page`

           onde `product name` é o nome e `landing_page` é um URL de página de aterrissagem ou URL de base válido.

           Exemplo: Acme PR208**http://www.example.com/travel.html

   1. Clique em **[!UICONTROL Generate Tracking URLs]**.

1. (Opcional) Copie os URLs (começando com &quot;http&quot; ou &quot;https&quot;) da tela ou página de saída e implemente-os na conta de pesquisa ou social.

Para contas com URLs de destino, insira os valores na variável [!UICONTROL Base URL] campos.

Para contas com URLs finais, insira o valor na tela nas configurações [!UICONTROL Tracking Template] campo. Você deve adicionar um parâmetro para o URL final após a variável `&url=` parâmetro (como `{lpurl}`). Para [!DNL Yahoo! Japan Ads] contas, use o parâmetro `{lpurl}`. Para obter uma lista de [!DNL Google Ads] e [!DNL Microsoft® Advertising] para indicar URLs finais em modelos de rastreamento, consulte a [[!DNL Google Ads] documentação](https://support.google.com/google-ads/answer/6305348) (Consulte os parâmetros &quot;Modelo de rastreamento somente&quot; na seção &quot;Modelo de rastreamento [!DNL ValueTrack] Parâmetros&quot;) e a [[!DNL Microsoft® Advertising] documentação](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [Sobre as ferramentas para criar e decodificar tags de rastreamento](tracking-tools-about.md)
>* [Quando e como gerar URLs de rastreamento de cliques](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [Decodificar um URL de rastreamento de cliques de Pesquisa, Social e Commerce](click-tracking-url-decode.md)
