---
title: Configurações da campanha
description: Consulte descrições das configurações de campanha disponíveis.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: d572a406be9271c6ca14d35740f04d15ddbf7364
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Configurações da campanha

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** O nome da campanha.

**[!UICONTROL Advertiser]:** (Somente leitura para campanhas existentes) O anunciante (marca) aplicável. Selecione um anunciante existente ou crie um novo.

**[!UICONTROL Advertiser URL]:** A página oficial do anunciante. Este campo acelera o processo de aprovação de anúncios com parceiros de inventário.

**[!UICONTROL Timezone]:** (Somente leitura para campanhas existentes) O fuso horário para relatórios e ofertas.

**[!UICONTROL Customer PO]:** (Opcional) Uma ordem de compra do cliente para a ordem de inserção/ordem de compra.

**[Datas da campanha]:** As datas de início e término da campanha.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Se gerenciar margens para a campanha: *[!UICONTROL Yes]* ou *[!UICONTROL No]* (o padrão).

Ao escolher *[!UICONTROL Yes],* especifique o tipo de margem e o valor:

* **[!UICONTROL Margin Type]:** O tipo de margem. Não é possível alterar o tipo de margem depois de habilitar o gerenciamento de margem e salvar a campanha.

   * *[!UICONTROL Fixed]:* (o padrão) Permite que o DSP calcule e limite automaticamente o gasto com base em uma porcentagem de margem fixa do [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Permite gerenciar margens até o nível de posicionamento especificando um [!UICONTROL Budget Reserve %] e [!UICONTROL Gross Budget] para cada pacote e posicionamento na campanha. O DSP otimiza com base na eficiência financeira de cada posicionamento, sem garantir uma margem específica. Use esta opção para ordens de inserção que consistem em vários itens de linha para os quais você concordou em distribuir uma quantia fixa de unidades ou tipos de unidade a uma taxa fixa.

* **[!UICONTROL Fixed Margin %]:** (Campanhas somente com margens fixas) A marcação padrão para cada ordem de inserção <!-- impression? -->, como uma porcentagem. Este montante é deduzido do montante [!UICONTROL Gross Budget] para definir o orçamento líquido da campanha.

* **[!UICONTROL Budget Reserve %]:** (Campanhas somente com margens fixas; opcional) Reserva uma porcentagem especificada do [!UICONTROL Gross Budget] a título de salvaguarda. Este montante é deduzido do montante [!UICONTROL Gross Budget] para definir o orçamento líquido da campanha.

**[!UICONTROL Gross Budget]:** (Campanhas somente com gerenciamento de margem) O orçamento bruto da campanha, antes da aplicação dos ajustes marginais especificados.

Opcionalmente, você pode adicionar um orçamento bruto diário, semanal ou mensal adicional:

1. Clique em **[!UICONTROL Add an additional Gross Budget]**.

1. Insira o **[!UICONTROL Gross Budget]** e selecione o intervalo orçamentário: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* ou *[!UICONTROL Monthly]*.

O orçamento líquido total, que é o limite de gastos da campanha, é calculado automaticamente com base nas configurações de margem e é indicado abaixo desse valor.

**[!UICONTROL Budget]:** (Campanhas sem gerenciamento de margem) O orçamento geral da campanha.

**[!UICONTROL Estimated Tax Withholding]:** Retém uma porcentagem do total gasto em taxas de publicidade, taxas de veiculação de anúncios e/ou taxas de dados no nível da conta para impostos locais ou do país. As taxas são estimativas para fins de orçamento e ritmo, portanto, as taxas de imposto faturadas podem variar.

Para estimar impostos a reter:

1. Clique em **[!UICONTROL Update rates here]**.

1. Especifique a **[!UICONTROL Estimated tax rate]**, como uma porcentagem.

1. Marque a caixa de seleção ao lado de cada tipo de taxa para o qual reter impostos. Os tipos de taxa incluem:

   * *[!UICONTROL Include estimated tax - ads fee]:* Aplica-se a todos os gastos com mídia DSP de publicidade, incluindo impostos sobre taxas de gerenciamento de campanha.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* Aplica-se a todos os gastos com DSP publicitário, exceto mídia e dados. Ele exclui impostos para taxas de gerenciamento de campanha

   * *[!UICONTROL Include estimated tax - data fee]:* Aplica-se a todos os dados gastos com publicidade de DSP.

1. Clique em **[!UICONTROL Submit]**.

>[!NOTE]
>
>* Nos EUA, os estados podem variar em sua inclusão de taxas fiscais entre anúncios, veiculação de anúncios e dados. Para organizações em outros países, inclua todas as três categorias de taxas de imposto para contabilizar IVA.
>
>* Você também pode configurar esses valores nas configurações de taxa da conta.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** (Somente leitura para campanhas existentes criadas desde 22 de junho de 2020; não disponível para campanhas criadas antes de 22 de junho de 2020) O nível no qual o DSP direciona anúncios e aplica limites de frequência: *Mesmo dispositivo* para direcionar um dispositivo ou *Pessoas* para direcionar uma pessoa em todos os dispositivos conhecidos. **Nota:** O suporte entre dispositivos não está disponível para posicionamentos que direcionam IDs universais.

**[!UICONTROL Device Graph]:** (Somente leitura para campanhas existentes; campanhas com direcionamento entre dispositivos baseado em pessoas somente) O gráfico de dispositivos a ser usado para direcionamento entre dispositivos e gerenciamento de frequência:

* *[!UICONTROL LiveRamp - U.S. only]:* Disponível para todos os anunciantes para direcionamento entre dispositivos a US$ 0,35 CPM para impressões fornecidas usando o [!DNL LiveRamp] gráfico de dispositivos (ou seja, para dispositivos não encontrados nos segmentos de público-alvo direcionados). Você pode configurar o direcionamento entre dispositivos no nível do posicionamento.

  Essa opção também está disponível para todos os anunciantes, sem taxas, para gestão de frequência e medição de atribuição.

  O suporte entre dispositivos se aplica somente a posicionamentos que direcionam IDs herdadas, mas não a posicionamentos que direcionam IDs universais (incluindo [!DNL LiveRamps]). O direcionamento, o gerenciamento de frequência e a atribuição de IDs universais são aplicados somente no nível de ID.

**[!UICONTROL Frequency Cap]:** (Opcional) O número de vezes que um dispositivo exclusivo, ID universal ou pessoa (dependendo do [!UICONTROL Cross Device Level] e o posicionamento [!UICONTROL Targeting] ) podem ser veiculadas com anúncios da campanha. As opções incluem *[!UICONTROL Unlimited]* ou uma quantidade específica por dia, semana ou mês.

>[!NOTE]
>
> Você pode definir limites de frequência nos níveis de campanha, pacote e posicionamento. O DSP respeita o limite de frequência mais rigoroso na hierarquia de campanha.

**[!UICONTROL Packages]:** A variável [pacotes](/help/dsp/campaign-management/packages/package-about.md) para incluir na campanha. Selecione pacotes existentes e/ou crie pacotes para incluir. Se você criar packages, consulte descrições sobre o [configurações de pacote](/help/dsp/campaign-management/packages/package-settings.md) para obter mais informações.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>As configurações a seguir ativam apenas os recursos de medição e relatório. A otimização de desempenho é executada somente no nível do pacote e do posicionamento.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Opcional) Ativa [!DNL IAS] medição e relatórios de visibilidade, fraude, segurança da marca e verificação de público-alvo, usando as configurações especificadas. Taxas adicionais são aplicadas.

* **[!UICONTROL Measure On]:** O inventário no qual medir: *[!UICONTROL Display and VPAID video inventory]* (o padrão) ou *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >A visibilidade do vídeo pode ser medida somente no inventário VPAID.

* **[!UICONTROL IAS Account ID (AnID)]:** (Anunciantes com seus próprios [!DNL IAS] contas; opcional) As contas da organização [!DNL IAS] ID da conta, que [!DNL IAS] cobrará diretamente pelo uso.

* **[!UICONTROL IAS Team ID]:** (Anunciantes com seus próprios [!DNL IAS] contas; opcional) a ID da equipe para a organização [!DNL IAS] conta, que [!DNL IAS] cobrará diretamente pelo uso. <!-- verify -->

**[!UICONTROL MOAT]:** (Opcional) Ativa [!DNL MOAT] medição e relatórios de visibilidade, fraude, segurança da marca e verificação de público-alvo. Taxas adicionais são aplicadas.

#### Verificação de público-alvo

**[!UICONTROL comScore Campaign Ratings]:** (Opcional) Ativa [!DNL Comscore] validado [!DNL Campaign Ratings] medição e relatórios da verificação de público-alvo, usando as configurações especificadas. Taxas adicionais são aplicadas.

* **[!UICONTROL Target Gender]:** O gênero a ser direcionado: *[!UICONTROL Both]* (o padrão), *[!UICONTROL Male]* ou *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** A faixa etária a ser atingida. Use os controles deslizantes esquerdo e direito para reduzir o intervalo conforme necessário.

* **[!UICONTROL Target Country]:** (Opcional) Um país a ser direcionado. [!DNL Comscore] O mede somente impressões veiculadas em países suportados.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** Ativa o rastreamento para o nível de posicionamento [!UICONTROL Attention Score] métrica (o número médio ponderado de [!DNL Adelaide] &quot;[!DNL Attention Units]&quot; em impressões). As métricas estão disponíveis para todos os tipos de posicionamento, exceto para [!DNL Roku] TV conectada, pré-lançamento somente VPAID e áudio que não é um podcast. O DSP anexa automaticamente uma tag JavaScript a todas as criações associadas e [!DNL Adelaide] O rastreia os dados de exposição e os envia para o DSP diariamente. Você pode usar a data para otimizar manualmente seus gastos com táticas de posicionamento com melhores pontuações de atenção.

A variável [!UICONTROL Attention Score] O campo está disponível no [!UICONTROL Metrics] seção de relatórios; no prazo de [!UICONTROL Campaigns], [!UICONTROL Packages], e [!UICONTROL Placements] visualizações; e no [!UICONTROL Sites], [!UICONTROL Ads], e [!UICONTROL Inventory] guias da [exibição de detalhes da disposição](/help/dsp/campaign-management/reports/placement-details-view.md).

Usar [!DNL Adelaide] segmentos para medição incorre em uma taxa de CPM para cada impressão fornecida pelos anúncios com [!DNL Adelaide] marcas de medição. Essa taxa é separada das taxas de [direcionamento de atenção no nível de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Permite a medição e o relatório de visibilidade próprios usando o [!DNL IAB Open Video Viewability (OpenVV)] com base no nível de sensibilidade especificado:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Sobre o Campaign Management](campaign-about.md)
>* [Criar uma campanha](campaign-create.md)
>* [Editar uma campanha](campaign-edit.md)
>* [Exibir o Log de Alterações de uma Campanha](campaign-change-log.md)
