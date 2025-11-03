---
title: Configurações da campanha
description: Consulte descrições das configurações de campanha disponíveis.
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 9d26e097f007b570c0f0e3b7f02c683a84d5e647
workflow-type: tm+mt
source-wordcount: '1434'
ht-degree: 0%

---

# Configurações da campanha

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** O nome da campanha.

**[!UICONTROL Advertiser]:** (Somente leitura para campanhas existentes) O anunciante (marca) aplicável. Selecione um anunciante existente ou crie um novo.

**[!UICONTROL Advertiser URL]:** A página oficial do anunciante. Este campo acelera o processo de aprovação de anúncios com parceiros de inventário.

**[!UICONTROL Timezone]:** (Somente leitura para campanhas existentes) O fuso horário para relatórios e lances.

**[!UICONTROL Customer PO]:** (Opcional) Uma ordem de compra do cliente para a ordem de inserção/ordem de compra.

**[Datas da Campanha]:** As datas de início e término da campanha.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** (Contas de autoatendimento atendidas por agências que usam margens) Opções para gerenciamento de margem:

* **[!UICONTROL Would you like to manage margins for this campaign?]:** Se deseja gerenciar margens para a campanha: *[!UICONTROL Yes]* ou *[!UICONTROL No]* (o padrão). Ao escolher *[!UICONTROL Yes],* especifique as configurações adicionais. Depois de habilitar o gerenciamento de margem e salvar a campanha, você não poderá desabilitá-lo.

* **[!UICONTROL How would you like to compute agency fees?]:** (Campanhas somente com gerenciamento de margem) Como calcular taxas de agência, que são a parte do orçamento bruto da campanha retida e não incluída no gasto líquido:

   * *[!UICONTROL Margin % of Total Budget]:* (padrão) Taxas de computação como uma porcentagem do gasto bruto. Especifique o [!UICONTROL Agency Fee Type] (fixo ou composto) e o [!UICONTROL Margin %] ou [!UICONTROL Composite Margin %].

   * *[!UICONTROL Apply Markup % on top of individual cost components]:* Calcule as taxas como uma porcentagem especificada do custo de mídia, dados e outros custos e/ou [!DNL Adobe] taxas técnicas. Especifique o [!UICONTROL Markup %] e selecione os componentes nos quais aplicar a marcação.

* **[!UICONTROL Agency Fee Type]:** (Campanhas que usam [!UICONTROL Margin % of Total Budget]) O tipo de taxa da agência.

   * *[!UICONTROL Fixed]:* (padrão) permite que a DSP retenha uma porcentagem fixa do gasto bruto como taxas de agência. Especifique o [!UICONTROL Margin %].

   * *[!UICONTROL Composite]:* permite que a DSP retenha uma porcentagem do gasto bruto para contabilizar taxas de agência e taxas de tecnologia [!DNL Adobe]. Especifique o [!UICONTROL Composite Margin %].

* **[!UICONTROL Margin %]:** (Campanhas que usam [!UICONTROL Margin % of Total Budget] com margens fixas) A porcentagem do gasto bruto a ser retida como taxas de agência. Quaisquer alterações no valor da margem são aplicadas apenas aos gastos brutos futuros e não aos gastos brutos históricos da campanha. O valor [!UICONTROL Estimated Tax Withholding] é excluído do gasto bruto antes da aplicação da margem. Veja os exemplos a seguir, que presumem que a campanha não gasta menos ou em excesso.

   * Exemplo 1: suponha que o [!UICONTROL Gross Budget] seja `100 USD` e o [!UICONTROL Margin %] seja `5%` durante todo o voo. No final do voo da campanha, as taxas de agência são computadas como `5 USD` (que é `5% of 100 USD`), e o gasto líquido é `95 USD` (que é `campaign budget [100 USD] - agency fees [5 USD]`).

   * Exemplo 2 com alterações na margem: para a mesma campanha, suponha que [!UICONTROL Margin %] foi alterado de `5%` para `10%` quando o gasto bruto foi `40 USD`. Para o período antes da alteração, as taxas de agência são computadas como `2 USD` (que é `5% of 40 USD`); para o período após a alteração, as taxas de agência são computadas como `6 USD` (que é `10% of 60 USD`). O total de taxas de agência é calculado como `8 USD` (que é `2 USD + 6 USD`), e o gasto líquido é `92 USD` (que é `campaign budget [100 USD] - total agency fees [8 USD]`).

   * Exemplo 3 com retenção de imposto: suponha que o [!UICONTROL Gross Budget] seja `100 USD`, o [!UICONTROL Estimated Tax Withholding] no final do voo da campanha seja `10 USD` e o [!UICONTROL Margin %] seja `5%` durante todo o voo. No final do voo da campanha, as taxas de agência são computadas como `4.5 USD` (que é `5% of (campaign budget [100 USD] - tax withholding [USD 10])`), e o gasto líquido é `85.5 USD` (que é `campaign budget [100 USD] - agency fees [4.5 USD] - tax withholding [10 USD]`).

* **[!UICONTROL Composite Margin %]:** (Campanhas que usam [!UICONTROL Margin % of Total Budget] com margens compostas) A porcentagem do gasto bruto que deve ser retida como [!DNL Adobe] de taxas técnicas e de agência combinadas. As taxas de agência são calculadas subtraindo-se as taxas técnicas da Adobe do valor da margem composta. Quaisquer alterações no valor da margem composta são aplicadas somente aos gastos brutos futuros e não aos gastos brutos históricos da campanha. O valor [!UICONTROL Estimated Tax Withholding] é excluído do gasto bruto antes da aplicação da margem composta.

  Por exemplo, suponha que [!UICONTROL Gross Budget] seja `100 USD`, as tarifas técnicas de [!DNL Adobe] no final do voo de campanha sejam `10 USD` e [!UICONTROL Composite Margin %] seja `17%` durante todo o voo. No final do voo da campanha (supondo que a campanha não gaste menos ou gaste demais), as taxas de agência são computadas como `7 USD` (que é `(17% of 100 USD) - 10`), e o gasto líquido é `93 USD` (que é `campaign budget [100 USD] - agency fees [7 USD]`).

* **[!UICONTROL Markup %]:** (Campanhas que usam [!UICONTROL Apply Markup % on top of individual cost components]) A porcentagem a ser aplicada aos componentes de custo especificados para calcular taxas de agência. Quaisquer alterações no valor de markup são aplicadas somente aos custos futuros e não aos custos históricos da campanha.

* **[!UICONTROL Select cost components on which markup will be applied]:** (Campanhas que usam [!UICONTROL Apply Markup % on top of individual cost components]) Os componentes de custo aos quais [!UICONTROL Markup %] é aplicado. Selecione todos os componentes aplicáveis: *[!UICONTROL Media cost]*, *[!UICONTROL Data and Other costs]* e/ou *[!UICONTROL Adobe tech fees]*. Quaisquer alterações na seleção de componentes são aplicadas somente aos custos futuros e não aos custos históricos da campanha.

  Por exemplo, [!UICONTROL Markup %] é `10%` para &quot;[!UICONTROL Media cost]&quot; e &quot;[!UICONTROL Data and Other costs]. Se, em qualquer ponto do voo da campanha, o custo de mídia for `20 USD`, os dados e outros custos forem `5 USD` e as taxas técnicas de [!DNL Adobe] forem `2 USD`, as taxas de agência serão computadas como `2.50 USD` (que é `10% of (20 USD + 5 USD)`, e o gasto bruto será `29.50 USD` (que é `media cost [20 USD] + data and other costs [5 USD] + [!DNL Adobe] tech fees [2 USD] + agency fees [2.50 USD]`).

**[!UICONTROL Gross Budget]:** (Campanhas somente com gerenciamento de margem) O orçamento bruto da campanha, antes da aplicação dos ajustes marginais especificados.

**[!UICONTROL Budget]:** (Campanhas sem gerenciamento de margem) O orçamento geral da campanha.

**[!UICONTROL Estimated Tax Withholding]:** Retém uma porcentagem do total gasto em taxas de publicidade, taxas de veiculação de anúncios e/ou taxas de dados no nível da conta para impostos locais ou do país. As taxas são estimativas para fins de orçamento e ritmo, portanto, as taxas de imposto faturadas podem variar.

Para estimar impostos a reter:

1. Clique em **[!UICONTROL Update rates here]**.

1. Especifique o **[!UICONTROL Estimated tax rate]** como uma porcentagem.

1. Marque a caixa de seleção ao lado de cada tipo de taxa para o qual reter impostos. Os tipos de taxa incluem:

   * *[!UICONTROL Include estimated tax - ads fee]:* Aplica-se a todos os gastos com mídia da Advertising DSP, incluindo impostos sobre taxas de gerenciamento de campanha.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* Aplica-se a todos os gastos no Advertising DSP, exceto mídia e dados. Ele exclui impostos para taxas de gerenciamento de campanha

   * *[!UICONTROL Include estimated tax - data fee]:* Aplica-se a todos os dados gastos no Advertising DSP.

1. Clique em **[!UICONTROL Submit]**.

>[!NOTE]
>
>* Nos EUA, os estados podem variar em sua inclusão de taxas fiscais entre anúncios, veiculação de anúncios e dados. Para organizações em outros países, inclua todas as três categorias de taxas de imposto para contabilizar IVA.
>
>* Você também pode configurar esses valores nas configurações de taxa da conta.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]:** (Somente leitura para campanhas existentes criadas desde 22 de junho de 2020; não disponível para campanhas criadas antes de 22 de junho de 2020) O nível no qual a DSP direciona anúncios e aplica limites de frequência: *Mesmo dispositivo* para direcionar um dispositivo ou *Pessoas* para direcionar uma pessoa em todos os seus dispositivos conhecidos. **Observação:** o suporte entre dispositivos não está disponível para posicionamentos que direcionem IDs universais.

**[!UICONTROL Device Graph]:** (Somente leitura para campanhas existentes; campanhas com segmentação entre dispositivos com base em pessoas apenas) O gráfico de dispositivos a ser usado para segmentação entre dispositivos e gerenciamento de frequência:

* *[!UICONTROL LiveRamp - U.S. only]:* Disponível a todos os anunciantes para direcionamento entre dispositivos a US$ 0,35 no CPM para impressões que são fornecidas usando o gráfico de dispositivos [!DNL LiveRamp] (ou seja, para dispositivos não encontrados nos segmentos de público-alvo direcionados). Você pode configurar o direcionamento entre dispositivos no nível do posicionamento.

  Essa opção também está disponível para todos os anunciantes, sem taxas, para gestão de frequência e medição de atribuição.

  O suporte entre dispositivos se aplica somente a posicionamentos que direcionem IDs herdadas, mas não a posicionamentos que direcionem IDs universais (incluindo [!DNL LiveRamps]). O direcionamento, o gerenciamento de frequência e a atribuição de IDs universais são aplicados somente no nível de ID.

**[!UICONTROL Frequency Cap]:** (Opcional) O número de vezes que um dispositivo exclusivo, ID universal ou pessoa (dependendo do [!UICONTROL Cross Device Level] especificado e da configuração [!UICONTROL Targeting] do posicionamento) pode receber anúncios da campanha. As opções incluem *[!UICONTROL Unlimited]* ou um valor específico por dia, semana ou mês.

>[!NOTE]
>
> Você pode definir limites de frequência nos níveis de campanha, pacote e posicionamento. O DSP respeita o limite de frequência mais rigoroso na hierarquia de campanha.

**[!UICONTROL Packages]:** Os [pacotes](/help/dsp/campaign-management/packages/package-about.md) a serem incluídos na campanha. Selecione pacotes existentes e/ou crie pacotes para incluir. Se você criar pacotes, consulte as descrições sobre as [configurações de pacote](/help/dsp/campaign-management/packages/package-settings.md) para obter mais informações.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>As configurações a seguir ativam apenas os recursos de medição e relatório. A otimização de desempenho é executada somente no nível do pacote e do posicionamento.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Opcional) Habilita a medição e o relatório [!DNL IAS] de visibilidade, fraude, segurança da marca e verificação de público-alvo, usando as configurações especificadas. Taxas adicionais são aplicadas.

* **[!UICONTROL Measure On]:** O inventário no qual medir: *[!UICONTROL Display and VPAID video inventory]* (o padrão) ou *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >A visibilidade do vídeo pode ser medida somente no inventário VPAID.

* **[!UICONTROL IAS Account ID (AnID)]:** (Anunciantes com suas próprias contas [!DNL IAS]; opcional) a ID de conta [!DNL IAS] da organização, que [!DNL IAS] cobrará diretamente pelo uso.

* **[!UICONTROL IAS Team ID]:** (Anunciantes com suas próprias contas [!DNL IAS]; opcional) a identificação de equipe para a conta [!DNL IAS] da organização, que [!DNL IAS] cobrará diretamente pelo uso. <!-- verify -->

#### Verificação de público-alvo

**[!UICONTROL Comscore Campaign Ratings]:** (Opcional) Habilita a medição e o relatório [!DNL Comscore] validados por [!DNL Campaign Ratings] da verificação de público-alvo, usando as configurações especificadas. Taxas adicionais são aplicadas.

* **[!UICONTROL Target Gender]:** Sexo a ser direcionado: *[!UICONTROL Both]* (padrão), *[!UICONTROL Male]* ou *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** A faixa etária a ser atingida. Use os controles deslizantes esquerdo e direito para reduzir o intervalo conforme necessário.

* **[!UICONTROL Target Country]:** (opcional) um país para direcionar. [!DNL Comscore] mede somente impressões veiculadas em países suportados.

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]:** Habilita o rastreamento para a métrica [!UICONTROL Attention Score] de nível de posicionamento (o número médio ponderado de [!DNL Adelaide] &quot;[!DNL Attention Units]&quot; em impressões). As métricas estão disponíveis para todos os tipos de posicionamento, exceto para [!DNL Roku] TV conectada, pré-implantação somente VPAID e áudio que não é um podcast. O DSP anexa automaticamente uma marca JavaScript a todas as criações associadas, e o [!DNL Adelaide] rastreia os dados de exposição e os envia para o DSP diariamente. Você pode usar a data para otimizar manualmente seus gastos com táticas de posicionamento com melhores pontuações de atenção.

O campo [!UICONTROL Attention Score] está disponível na seção [!UICONTROL Metrics] dos relatórios; nos modos de exibição [!UICONTROL Campaigns], [!UICONTROL Packages] e [!UICONTROL Placements]; e nas guias [!UICONTROL Sites], [!UICONTROL Ads] e [!UICONTROL Inventory] da [exibição de detalhes de posicionamento](/help/dsp/campaign-management/reports/placement-details-view.md).

O uso de [!DNL Adelaide] segmentos para medição incorre em uma taxa de CPM para cada impressão entregue pelos anúncios com [!DNL Adelaide] marcas de medição. Esta taxa é separada das taxas de [direcionamento de atenção no nível de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md).

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Habilita a medição e o relatório de visibilidade próprios usando a tecnologia [!DNL IAB Open Video Viewability (OpenVV)], com base no nível de sensibilidade especificado:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de campanhas](campaign-about.md)
>* [Criar uma campanha](campaign-create.md)
>* [Editar uma campanha](campaign-edit.md)
>* [Exibir o Log de Alterações de uma Campanha](campaign-change-log.md)
