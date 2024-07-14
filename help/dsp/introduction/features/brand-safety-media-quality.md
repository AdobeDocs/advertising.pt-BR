---
title: Segurança da marca e qualidade da mídia
description: Saiba mais sobre os recursos de segurança da marca e qualidade da mídia.
feature: DSP Introduction
exl-id: 8cdfd517-4cdb-4dbc-aae5-a8bda1e4e95e
source-git-commit: a927c073fd27e0b2c84bd1929eb4d6d233a29cb5
workflow-type: tm+mt
source-wordcount: '1436'
ht-degree: 0%

---

# Segurança da marca e qualidade da mídia

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

O Advertising DSP fornece um conjunto de recursos de proteção da marca para garantir que cada uma de suas campanhas atinja usuários reais em um ambiente seguro para a marca.

Nossa equipe de Vigilância de Fraudes trabalha em conjunto com parceiros líderes do setor, como o [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)] e [!DNL WhiteOps], para preparar cuidadosamente o inventário em nossa plataforma. Por meio do gerenciamento pró-ativo de nosso suprimento, o DSP garante que todos os anunciantes na plataforma estejam protegidos contra tráfego não humano (bots, crawlers, tráfego de data center e fraude) e sejam entregues somente em contextos seguros para a marca.

Além de fornecer um gerenciamento de qualidade central, acreditamos em capacitar os anunciantes a projetar os controles que se alinham à sua marca. O DSP oferece integrações com [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud] e [!DNL Peer39], garantindo que cada anunciante possa escolher seu nível desejado de proteção contra fraude, filtragem contextual e direcionamento por palavras-chave.

## Iniciativas de qualidade

### Verificação de inventário com suporte de [!DNL Ads.txt]

[[!DNL Ads.txt], que significa  [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) é uma iniciativa lançada pela [!DNL Interactive Advertising Bureau] ([!DNL IAB]) em junho de 2017 para facilitar a representação adequada de estoque no mercado aberto, combatendo assim fontes ilegítimas de tráfego e falsificação de domínio. Os editores e distribuidores participantes declaram publicamente as empresas autorizadas a vender seu inventário digital e a natureza desses relacionamentos, mantendo uma página `ads.txt` no nível superior do domínio (como `example.com/ads.txt`).

O DSP oferece suporte a [!DNL ads.txt] lendo o arquivo `ads.txt` de cada editor e dando a você a opção de comprar somente de [!DNL ads.txt] vendedores verificados. Por exemplo, ao corresponder os vendedores que vemos acessando `nytimes.com` ao arquivo `ads.txt` do New York Times, podemos identificar quais são legítimos e quais não são, e vamos bloquear os infratores se o posicionamento estiver configurado para comprar apenas de vendedores verificados. <!-- can we actually mention NY Times? -->

Você pode definir controles [!DNL ads.txt] padrão para cada anunciante<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> e, opcionalmente, [personalizar as configurações para cada posicionamento](/help/dsp/campaign-management/placements/placement-settings.md) para:

* comprar inventário somente de vendedores diretos autorizados de um domínio

* comprar estoque somente de revendedores e vendedores diretos autorizados de um domínio

* priorizar a compra de estoque dos vendedores diretos e revendedores autorizados de um domínio

* comprar estoque de todos os vendedores

### Vigilância de Fraude de Plataforma

O DSP criou ferramentas e sistemas internos sólidos para gerenciar fraudes em toda a nossa plataforma, em parceria com fornecedores líderes do setor, como o [!DNL Whiteops] e o [!DNL Integral Ad Science].

Além disso, o Adobe trabalha em conjunto com o [!DNL IAB] e o [!DNL TAG] para garantir um bloqueio robusto de fraudes padrão do setor para proteger nossos anunciantes, aproveitando ferramentas como o [!DNL ads.txt] (consulte a seção anterior), a lista de [!DNL IAB] Bots e Spiders e a lista de [!DNL TAG] Datacenter IP.

Por meio de nossa abordagem multidimensional à qualidade, nossa equipe monitora anomalias e padrões de tráfego inválidos, garantindo menos de 3% de tráfego inválido no inventário protegido. Qualquer inventário suspeito — incluindo inventário em domínios específicos ou de editores ou vendedores específicos — é imediatamente bloqueado na plataforma.

### Mapeamento de inventário, classificação por níveis e categorização

O mapeamento de inventário é o processo detalhado de revisão e integração necessário para todos os novos inventários antes de serem adicionados à nossa plataforma. Esse processo foi projetado para garantir a segurança e a qualidade de todo o inventário de DSP.

* **Mapeamento:** Nossa equipe de inventário analisa cuidadosamente cada domínio, avaliando aspectos como:

   * Segurança da marca

   * Verificação de tipo de anúncio

   * Conteúdo genérico, domínios duplicados e veiculação de anúncios falsos

* **Classificação por níveis:** examinamos de forma holística a presença da marca no ecossistema geral para classificar o inventário em diferentes níveis. Você pode [direcionar seus posicionamentos](/help/dsp/campaign-management/placements/placement-settings.md) para esses níveis para o nível desejado de alcance:

   * **[!UICONTROL T1]** — Nome da marca, sites reconhecidos internacionalmente

   * **[!UICONTROL T2]** — Sites com ótima aparência que estão atualizados, sem conteúdo gerado pelo usuário e geralmente sem reconhecimento global

   * **[!UICONTROL T3]** — Conteúdo gerado pelo usuário e conteúdo de nicho

* **Categorização do site:** para garantir o fácil direcionamento e bloqueio de conteúdo, marcamos cada propriedade com uma categoria de site definida pelo DSP com base no conteúdo da propriedade. Você pode [direcionar ou excluir essas categorias de site para cada posicionamento](/help/dsp/campaign-management/placements/placement-settings.md) com base nas metas de posicionamento.

### Suporte abrangente para bloqueio de sites

O DSP fornece uma lista de sites bloqueados globalmente e a opção de criar listas de sites bloqueados personalizadas para anunciantes e contas.

#### Lista de sites globalmente bloqueados no DSP {#global-blocked-sites}

O DSP mantém uma lista de sites bloqueados globalmente com sites considerados inseguros para a execução de anúncios. Esta lista contém sites com conteúdo censurável (como ódio ou terror) e sites infectados por bots, domínios falsos precedentes, domínios incompatíveis e outras atividades fraudulentas.

Como parte de nossa iniciativa de Segurança da marca para eliminar as atividades que defraudam anunciantes, todos os sites são verificados usando as medidas na lista de sites bloqueados do gráfico. Todos os sites que não passarem nas verificações de segurança da marca serão adicionados à lista de sites bloqueados globalmente. Como o DSP gerencia essa lista dinamicamente, os sites podem ser ativados ou desativados a qualquer momento, com base na análise mais recente de segurança da marca.

Quando você inclui um site na lista de sites globalmente bloqueados como um destino de posicionamento, o site é sinalizado com um ponto de exclamação vermelho (!). Isso indica que os anúncios não são executados no site sinalizado.

>[!NOTE]
>
>Você pode, opcionalmente, ignorar a lista global de sites bloqueados para anúncios de exibição padrão anexados a uma negociação privada confiável, habilitando a opção &quot;[!UICONTROL Allow unscreened sites]&quot; nas [configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md). Se necessário, a Equipe de conta do Adobe também pode, opcionalmente, desativar o bloqueio de sites para um negócio público (nível de leilão) nas configurações do editor para o negócio.

#### Listas de sites bloqueados no nível da conta e do anunciante

Os usuários também podem manter listas de sites bloqueados <!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) --> no nível da conta e do anunciante, que são usadas automaticamente para todos os posicionamentos. As listas de sites bloqueados de nível inferior são aplicadas além da lista de sites bloqueados globalmente.

## Integrações de terceiros

### Filtragem contextual

A filtragem contextual permite direcionar ou bloquear oportunidades de anúncios com base no contexto da página em que o anúncio seria veiculado. O Adobe fornece filtragem contextual por meio de integrações com os principais fornecedores do setor: [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] e [!DNL Peer39]. Exemplos de filtros atuais incluem [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics] e [!UICONTROL G-rated Sites].

Você pode definir controles de filtro contextual padrão para cada anunciante<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> e, opcionalmente, [personalizar as configurações para cada posicionamento](/help/dsp/campaign-management/placements/placement-settings.md). Taxas adicionais podem ser aplicadas quando você usar este recurso.

![Logotipo do Comscore](/help/dsp/assets/comscore-logo.png) ![Logotipo do DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logotipo Integral do Ad Science](/help/dsp/assets/ias-logo.png) ![Logotipo do Peer39](/help/dsp/assets/peer39-logo.png)

### Bloqueio de fraude pré-oferta

Aproveite nossas integrações de terceiros com o [!DNL DoubleVerify], [!DNL Integral Ad Science] e [!DNL Peer39] para bloquear tráfego não humano de suas campanhas. Essas integrações fornecem os melhores recursos de bloqueio pré-oferta do setor para minimizar o tráfego geral e o tráfego inválido sofisticado (GIVT e SIVT) em suas campanhas.

Você pode definir controles padrão de bloqueio de fraude pré-oferta para cada anunciante<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> e, opcionalmente, [personalizar as configurações para cada posicionamento](/help/dsp/campaign-management/placements/placement-settings.md). Taxas adicionais podem ser aplicadas quando você usar este recurso.

Para obter mais informações sobre a funcionalidade, entre em contato diretamente com o fornecedor de sua preferência ou com a equipe de conta do Adobe.

![Logotipo do DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logotipo Integral do Ad Science](/help/dsp/assets/ias-logo.png) ![Logotipo do Peer39](/help/dsp/assets/peer39-logo.png)

### Visibilidade pré-oferta {#pre-bid-viewability}

Os filtros de visibilidade pré-oferta viabilizados pelos nossos parceiros líderes do setor [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]) e [!DNL Integral Ad Science] permitem que os anunciantes garantam que suas campanhas atendam às metas de desempenho de visibilidade desejadas no inventário de vídeo e exibição.

>[!NOTE]
>
>O [!DNL Oracle] encerrará seus negócios de publicidade até 30 de setembro de 2024, incluindo todos os serviços a partir de [!DNL MOAT].

Você pode definir filtros de visibilidade padrão para cada anunciante<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) --> e, opcionalmente, [personalizar as configurações para cada posicionamento](/help/dsp/campaign-management/placements/placement-settings.md). Taxas adicionais podem ser aplicadas quando você usar este recurso.

![Logotipo do DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logotipo do Oracle Advertising](/help/dsp/assets/oracle-advertising-logo.png) ![Logotipo Integral do Ad Science](/help/dsp/assets/ias-logo.png)

### Direcionamento de atenção e medição

A parceria da [!DNL Adobe's] com a [!DNL Adelaide] fornece aos anunciantes suporte para a métrica de Adelaide &quot;[!DNL Attention Units]&quot;, que mede a qualidade da mídia com base no rastreamento ocular, exposição e dados de resultados.

[O direcionamento de atenção pré-oferta no nível de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md) permite que os anunciantes direcionem níveis de atenção específicos para melhorar o engajamento do cliente.

Além disso, os anunciantes podem habilitar o [rastreamento para a métrica [!UICONTROL Attention Score] do nível de posicionamento](/help/dsp/campaign-management/campaigns/campaign-settings.md#attention-measurement) (o número médio ponderado de [!DNL Attention Units] entre impressões) para qualquer campanha para entender quais táticas de posicionamento produzem os melhores resultados de negócios.

Taxas adicionais se aplicam a cada recurso separado.

### Direcionamento de tópico

O direcionamento de tópico do DSP permite direcionar ou bloquear listas de palavras-chave aproveitando nossos parceiros contextuais líderes do setor [!DNL Comscore] e [!DNL Oracle Data Cloud] (anteriormente [!DNL Grapeshot]). O direcionamento de tópico ajuda a garantir que seus anúncios sejam sempre veiculados em um ambiente que se alinha à sua marca, seja bloqueando conteúdo prejudicial ou garantindo que sejam gastos em um contexto que garanta um resultado melhor.

>[!NOTE]
>
>O [!DNL Oracle] encerrará seu negócio de publicidade até 30 de setembro de 2024, incluindo todos os serviços do [!DNL Oracle Data Cloud] (antigo [!DNL Grapeshot]).

O direcionamento de tópico exige que você crie segmentos de tópico personalizados diretamente com a plataforma de parceiro. Depois que os segmentos forem criados, você poderá [direcionar ou excluir uma ID de segmento na seção [!UICONTROL Audience Targeting] para cada posicionamento](/help/dsp/campaign-management/placements/placement-settings.md). Taxas adicionais podem ser aplicadas para este recurso.

Para criar uma conta do [!DNL Comscore] e segmentos de tópicos personalizados, você pode solicitar um logon para [!DNL Activation Segment Manager] em [https://agents.comscore.com](https://agents.comscore.com). Consulte a [[!DNL Comscore] central de ajuda](https://comscoreactivation.zendesk.com/hc/) para obter instruções completas sobre como configurar segmentos personalizados. As tarifas para segmentos personalizados estão visíveis em [!DNL Segment Manager] à medida que você os cria.

![Logotipo do Comscore](/help/dsp/assets/comscore-logo.png) ![Logotipo da Grapeshot](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

A DSP fez parceria com a [!DNL DoubleVerify] para oferecer a solução de direcionamento [!DNL Authentic Brand Safety], que permite criar um conjunto centralizado de requisitos de segurança da marca para segmentar todas as suas plataformas de compra por consistência.

Depois de criar um segmento de segurança da marca [!DNL DoubleVerify] com o direcionamento necessário, você pode usá-lo no DSP para replicar suas regras de bloqueio pós-oferta com pré-oferta em ambientes da Web.

Você pode especificar uma ID de segmento [!DNL DoubleVerify] para cada anunciante<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) --> e, opcionalmente, [habilitar ou desabilitar [!UICONTROL Authentic Brand Safety] para cada posicionamento](/help/dsp/campaign-management/placements/placement-settings.md). O DSP fatura sua conta pelo uso da ID do segmento.

Para obter mais informações sobre a funcionalidade, contate o [!DNL DoubleVerify] diretamente ou a Equipe de Conta do Adobe.

![Logotipo do DoubleVerify](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
