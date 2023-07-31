---
title: Segurança da marca e qualidade da mídia
description: Saiba mais sobre os recursos de segurança da marca e qualidade da mídia.
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: 09ccb4790906e64834e52fb28956fe41997cbd1b
workflow-type: tm+mt
source-wordcount: '1354'
ht-degree: 0%

---

# Segurança da marca e qualidade da mídia

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

O Advertising DSP fornece um conjunto de recursos de proteção da marca para garantir que cada uma de suas campanhas atinja usuários reais em um ambiente seguro para a marca.

A nossa equipe de vigilância de fraudes trabalha em estreita colaboração com os principais parceiros do setor, como a [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)], e [!DNL WhiteOps], para preparar cuidadosamente o inventário na nossa plataforma. Por meio do gerenciamento pró-ativo de nosso suprimento, o DSP garante que todos os anunciantes na plataforma estejam protegidos contra tráfego não humano (bots, crawlers, tráfego de data center e fraude) e sejam entregues somente em contextos seguros para a marca.

Além de fornecer um gerenciamento de qualidade central, acreditamos em capacitar os anunciantes a projetar os controles que se alinham à sua marca. O DSP oferece integrações com [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud], e [!DNL Peer39], garantindo que cada anunciante possa escolher seu nível desejado de proteção contra fraudes, filtragem contextual e direcionamento por palavras-chave.

## Iniciativas de qualidade

### Verificação de inventário com [!DNL Ads.txt] Suporte

[[!DNL Ads.txt], que significa [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) é uma iniciativa lançada pela [!DNL Interactive Advertising Bureau] ([!DNL IAB]), em junho de 2017, para facilitar a representação adequada dos inventários no mercado livre, combatendo assim as fontes ilegítimas de tráfego e a falsificação de domínios. Os editores e distribuidores participantes declaram publicamente as sociedades autorizadas a vender o seu inventário digital e a natureza dessas relações, `ads.txt` página no nível superior do domínio (como `example.com/ads.txt`).

Suporte para DSP [!DNL ads.txt] lendo o de cada editor `ads.txt` arquivo e dando a você a opção de comprar somente de produtos verificados [!DNL ads.txt] vendedores. Por exemplo, ao corresponder aos vendedores que vemos acessando `nytimes.com` para o New York Times `ads.txt` Identificamos quais são legítimos e quais não são e bloquearemos os infratores se o posicionamento estiver configurado para comprar somente de vendedores verificados. <!-- can we actually mention NY Times? -->

É possível definir o padrão [!DNL ads.txt] controles para cada anunciante<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->e, opcionalmente, [personalizar as configurações para cada posicionamento](/help/dsp/campaign-management/placements/placement-settings.md) para:

* comprar inventário somente de vendedores diretos autorizados de um domínio

* comprar estoque somente de revendedores e vendedores diretos autorizados de um domínio

* priorizar a compra de estoque dos vendedores diretos e revendedores autorizados de um domínio

* comprar estoque de todos os vendedores

### Vigilância de Fraude de Plataforma

A DSP criou ferramentas e sistemas internos sólidos para gerenciar fraudes em toda a nossa plataforma, em parceria com fornecedores líderes do setor, como [!DNL Whiteops] e [!DNL Integral Ad Science].

Além disso, o Adobe trabalha em estreita [!DNL IAB] e [!DNL TAG] garantir um bloqueio robusto e padrão do setor contra fraudes para proteger nossos anunciantes, aproveitando ferramentas como [!DNL ads.txt] (consulte a seção anterior), a variável [!DNL IAB] Lista de bots e aranhas e a [!DNL TAG] Lista de IPs do data center.

Por meio de nossa abordagem multidimensional à qualidade, nossa equipe monitora anomalias e padrões de tráfego inválidos, garantindo menos de 3% de tráfego inválido no inventário protegido. Qualquer inventário suspeito — incluindo inventário em domínios específicos ou de editores ou vendedores específicos — é imediatamente bloqueado na plataforma.

### Mapeamento de inventário, classificação por níveis e categorização

O mapeamento de inventário é o processo detalhado de revisão e integração necessário para todos os novos inventários antes de serem adicionados à nossa plataforma. Esse processo foi projetado para garantir a segurança e a qualidade de todo o inventário de DSP.

* **Mapeamento:** Nossa equipe de inventário analisa cada domínio cuidadosamente, avaliando aspectos como:

   * Segurança da marca

   * Verificação de tipo de anúncio

   * Conteúdo genérico, domínios duplicados e veiculação de anúncios falsos

* **Hierarquização:** Examinamos de forma holística a presença da marca no ecossistema geral para classificar o inventário em diferentes níveis. Você pode [direcionar seus posicionamentos](/help/dsp/campaign-management/placements/placement-settings.md) para esses níveis para o nível desejado de alcance:

   * **[!UICONTROL T1]** — Sites com nome comercial e reconhecidos internacionalmente

   * **[!UICONTROL T2]** — sites bonitos que estão atualizados, sem conteúdo gerado pelo usuário e geralmente carecem de reconhecimento global

   * **[!UICONTROL T3]** — Conteúdo gerado pelo utilizador e conteúdo de nicho

* **Categorização do site:** Para garantir o fácil direcionamento e bloqueio de conteúdo, marcamos cada propriedade com uma categoria de site definida pelo DSP com base no conteúdo da propriedade. Você pode [direcionar ou excluir essas categorias de site para cada posicionamento](/help/dsp/campaign-management/placements/placement-settings.md) com base nas metas de posicionamento.

### Suporte abrangente para bloqueio de sites

O DSP fornece uma lista de sites bloqueados globalmente e a opção de criar listas de sites bloqueados personalizadas para anunciantes e contas.

#### Lista de sites globalmente bloqueados no DSP {#global-blocked-sites}

O DSP mantém uma lista de sites bloqueados globalmente com sites considerados inseguros para a execução de anúncios. Esta lista contém sites com conteúdo censurável (como ódio ou terror) e sites infectados por bots, domínios falsos precedentes, domínios incompatíveis e outras atividades fraudulentas.

Como parte de nossa iniciativa de Segurança da marca para eliminar as atividades que defraudam anunciantes, todos os sites são verificados usando as medidas na lista de sites bloqueados do gráfico. Todos os sites que não passarem nas verificações de segurança da marca serão adicionados à lista de sites bloqueados globalmente. Como o DSP gerencia essa lista dinamicamente, os sites podem ser ativados ou desativados a qualquer momento, com base na análise mais recente de segurança da marca.

Quando você inclui um site na lista de sites globalmente bloqueados como um destino de posicionamento, o site é sinalizado com um ponto de exclamação vermelho (!). Isso indica que os anúncios não serão executados no site sinalizado.

>[!NOTE]
>
>Você pode, opcionalmente, ignorar a lista global de sites bloqueados para anúncios de exibição padrão anexados a uma negociação privada confiável ativando o &quot;[!UICONTROL Allow unscreened sites]&quot; na caixa de diálogo [configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md). Se necessário, a Equipe de conta do Adobe também pode, opcionalmente, desativar o bloqueio de sites para um negócio público (nível de leilão) nas configurações do editor para o negócio.

#### Listas de sites bloqueados no nível da conta e do anunciante

Os usuários também podem manter listas de sites bloqueados no nível da conta e do anunciante<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->, que são usados automaticamente para todos os posicionamentos. As listas de sites bloqueados de nível inferior são aplicadas além da lista de sites bloqueados globalmente.

## Integrações de terceiros

### Filtragem contextual

A filtragem contextual permite direcionar ou bloquear oportunidades de anúncios com base no contexto da página em que o anúncio seria veiculado. O Adobe fornece filtragem contextual por meio de integrações com os principais fornecedores do setor: [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], e [!DNL Peer39]. Exemplos de filtros atuais incluem [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics], e [!UICONTROL G-rated Sites].

É possível definir controles de filtro contextuais padrão para cada anunciante<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->e, opcionalmente, [personalizar as configurações para cada posicionamento](/help/dsp/campaign-management/placements/placement-settings.md). Taxas adicionais podem ser aplicadas quando você usar este recurso.

![Logotipo Comscore](/help/dsp/assets/comscore-logo.png) ![Logotipo do DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logotipo Integral Ad Science](/help/dsp/assets/ias-logo.png) ![Logotipo Peer39](/help/dsp/assets/peer39-logo.png)

### Bloqueio de fraude pré-oferta

Aproveite nossas integrações de terceiros com o [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], e [!DNL Peer39] para bloquear o tráfego não humano de suas campanhas. Essas integrações fornecem os melhores recursos de bloqueio pré-oferta do setor para minimizar o tráfego geral e o tráfego inválido sofisticado (GIVT e SIVT) em suas campanhas.

Você pode definir controles padrão de bloqueio de fraude pré-oferta para cada anunciante<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->e, opcionalmente, [personalizar as configurações para cada posicionamento](/help/dsp/campaign-management/placements/placement-settings.md). Taxas adicionais podem ser aplicadas quando você usar este recurso.

Para obter mais informações sobre a funcionalidade, entre em contato diretamente com o fornecedor de sua preferência ou com a equipe de conta do Adobe.

![Logotipo Comscore](/help/dsp/assets/comscore-logo.png) ![Logotipo do DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logotipo Integral Ad Science](/help/dsp/assets/ias-logo.png) ![Logotipo Peer39](/help/dsp/assets/peer39-logo.png)

### Visibilidade pré-oferta {#pre-bid-viewability}

Filtros de visibilidade pré-oferta viabilizados por nossos parceiros líderes do setor [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]) e [!DNL Integral Ad Science] permitir que os anunciantes garantam que suas campanhas atendam às metas de desempenho de visibilidade desejadas no inventário de vídeo e exibição.

É possível definir filtros de visibilidade padrão para cada anunciante<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->e, opcionalmente, [personalizar as configurações para cada posicionamento](/help/dsp/campaign-management/placements/placement-settings.md). Taxas adicionais podem ser aplicadas quando você usar este recurso.

![Logotipo do DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logotipo da Oracle Advertising](/help/dsp/assets/oracle-advertising-logo.png) ![Logotipo Integral Ad Science](/help/dsp/assets/ias-logo.png)

### Direcionamento de tópico

O direcionamento de tópico do DSP permite direcionar ou bloquear listas de palavras-chave aproveitando nossos parceiros contextuais líderes do setor [!DNL Comscore] e [!DNL Oracle Data Cloud] ([!DNL Grapeshot]). O direcionamento de tópico ajuda a garantir que seus anúncios sejam sempre veiculados em um ambiente que se alinha à sua marca, seja bloqueando conteúdo prejudicial ou garantindo que sejam gastos em um contexto que garanta um resultado melhor.

O direcionamento de tópico exige que você crie segmentos de tópico personalizados diretamente com o [!DNL Comscore] ou [!DNL Grapeshot] (usando [!DNL Oracle Data Cloud]). Depois que eles forem criados na plataforma do parceiro, você poderá [direcionar ou excluir uma ID de segmento no [!UICONTROL Audience Targeting] seção para cada posicionamento](/help/dsp/campaign-management/placements/placement-settings.md). Taxas adicionais podem ser aplicadas para este recurso.

Para criar segmentos de tópico personalizados:

* Para criar um [!DNL Comscore] conta e criar segmentos personalizados, é possível solicitar um logon para [!DNL Activation Segment Manager] em [https://agents.comscore.com](https://agents.comscore.com). Consulte a [[!DNL Comscore] centro de ajuda](https://comscoreactivation.zendesk.com/hc/) para obter instruções completas sobre como configurar segmentos personalizados. As taxas para segmentos personalizados estão visíveis no [!DNL Segment Manager] à medida que você as cria.

* Para começar com [!DNL Oracle Data Cloud], entre em contato [!DNL Oracle Data Cloud] ou a equipe de conta do Adobe.

![Logotipo Comscore](/help/dsp/assets/comscore-logo.png) ![Logotipo da Grapeshot](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

O DSP fez parceria com a [!DNL DoubleVerify] para oferecer seus [!DNL Authentic Brand Safety] solução de direcionamento, que permite criar um conjunto centralizado de requisitos de segurança da marca para segmentar todas as suas plataformas de compra por consistência.

Depois de criar um [!DNL DoubleVerify] segmento de segurança da marca com o direcionamento necessário, você pode usá-lo no DSP para replicar suas regras de bloqueio pós-oferta com pré-oferta em ambientes da Web.

Você pode especificar um [!DNL DoubleVerify] ID de segmento para cada anunciante<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->e, opcionalmente, [ativar ou desativar [!UICONTROL Authentic Brand Safety] para cada posicionamento](/help/dsp/campaign-management/placements/placement-settings.md). O DSP fatura sua conta pelo uso da ID do segmento.

Para obter mais informações sobre a funcionalidade, entre em contato com [!DNL DoubleVerify] diretamente ou entre em contato com a equipe de conta da Adobe.

![Logotipo do DoubleVerify](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
