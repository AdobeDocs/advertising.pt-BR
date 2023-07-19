---
title: Configurações do relatório personalizado
description: Consulte descrições das configurações de relatório personalizadas.
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
source-git-commit: 3faf43573cb073be828b0740f68f0e7d0612a1ef
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 0%

---

# Configurações do relatório personalizado

**[!UICONTROL Name]** O nome do relatório. O comprimento máximo é de 180 caracteres.

**[!UICONTROL Report Type]** O tipo de relatório: *[!UICONTROL Custom]* (que inclui a maioria das opções disponíveis), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*,  *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*,  *[!UICONTROL Segment]*, *[!UICONTROL Site]*, *[!UICONTROL Household Reach & Frequency]* ou *[!UICONTROL Household Conversions]*.

## [!UICONTROL Apply Filters] Seção

**[!UICONTROL Timezone]:** O fuso horário para relatórios.

**[!UICONTROL Observe Daylight Savings Time]:** Considera o Horário de verão nos horários relatados.

**\[Intervalo de datas\]:** O intervalo de datas para o qual gerar dados. O número de dias disponíveis varia de acordo com o relatório e as dimensões selecionadas. Escolha um:

* **[!UICONTROL Previous N days]:** Inclui dados de um número específico de dias antes de hoje.

* **[!UICONTROL Custom]:** Inclui dados entre datas de início e término específicas. Para relatar dados até o dia anterior, selecione **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]:** Inclui dados do mês anterior.

**[!UICONTROL Add Filters]:** (Opcional) Dimensões adicionais pelas quais filtrar os dados, independentemente das dimensões serem incluídas como colunas no relatório. Os filtros disponíveis variam por tipo de relatório e podem incluir: *[!UICONTROL Account]*\*, *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, * *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]*, e *[!UICONTROL Video Duration]*.

\* *[!UICONTROL Account]* O está disponível para os seguintes tipos de relatório somente quando sua organização está configurada para [relatório entre contas](report-about.md#cross-account-reporting):  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)], e [!UICONTROL Conversion]. Entre em contato com a equipe de conta do Adobe para obter mais informações sobre relatórios entre contas.

Para aplicar um ou mais filtros, faça o seguinte:

* Selecione uma dimensão, selecione o operador (*igual a* ou *não é igual*) e selecione o valor aplicável. Por exemplo, para retornar dados apenas para anúncios precedentes, especifique &quot;[!UICONTROL Ad Type equals Preroll].&quot;
* (Opcional) Adicione outros critérios ao filtro.
* (Opcional) Adicione filtros adicionais, cada um com um ou mais critérios.

## [!UICONTROL Build Your Report] Seção

**[!UICONTROL Select To Add As Report Headers]:**  As colunas de dados, ou cabeçalhos, a serem incluídos no relatório. Para adicionar uma coluna, expanda a categoria e marque a caixa de seleção ao lado do nome da coluna. As colunas disponíveis variam de acordo com o relatório e todas as métricas indisponíveis são desativadas. As categorias de dados disponíveis incluem:

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > A variável [!UICONTROL Household Reach & Frequency] O relatório pode incluir apenas uma dimensão.

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >A variável [!UICONTROL Household Reach & Frequency] O relatório pode incluir métricas de sobreposição ou não, mas não ambas.

* [!UICONTROL Conversion Metrics] (classificado pelo anunciante)

* [!UICONTROL Custom Goals] (classificado pelo anunciante)

Consulte &quot;[Colunas de Relatório Disponíveis](report-columns.md)&quot; para obter descrições de todas as opções.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** A ordem dos cabeçalhos de coluna. Você pode arrastar e soltar qualquer coluna para personalizar a ordem.

## [!UICONTROL Multi-Touch Conversion Options] Seção

**[!UICONTROL Format]:** Gerar ou não um relatório no *[!UICONTROL CSV]* (valores separados por vírgulas) ou *[!UICONTROL Tab]* formato (valores separados por tabulação).

**[!UICONTROL Report Headers]:** Se deseja *[!UICONTROL Include]* ou *[!UICONTROL Do Not Include]* cabeçalhos de coluna.

**[!UICONTROL Attribution Rule Settings]:** (Todos [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment], e [!UICONTROL Site] relatórios com [!UICONTROL Conversion Metrics] ou [!UICONTROL Custom Goals] colunas; anunciantes com rastreamento de conversão de Adobe Advertising somente) No relatório, saiba como atribuir dados de conversão em uma série de eventos que levam a uma conversão. Você pode escolher mais de uma regra se quiser comparar diferenças entre as regras.

>[!NOTE]
>
>Os caminhos de conversão incluem quaisquer impressões e cliques nas janelas de impressão ou retrospectiva de cliques do anunciante, que são configuradas em [!DNL Advertising Search, Social, & Commerce]. Os cliques recebem preferência por impressões durante a atribuição de conversão. Quaisquer cliques em um caminho de conversão receberão crédito total com base na regra de atribuição. As impressões recebem crédito somente quando nenhum clique é rastreado no caminho de conversão.

* *[!UICONTROL Last Event]:* Atribui conversões ao último clique ou impressão no caminho de conversão.

* *[!UICONTROL Weight Last More]:* Atribui conversões a todos os eventos no caminho de conversão, mas atribui mais peso ao último evento e sucessivamente menos peso aos eventos anteriores.

* *[!UICONTROL Even Distribution]:* Atribui conversões igualmente a cada evento no caminho de conversão.

* *[!UICONTROL Weight First More]:* Atribui conversões a todos os eventos no caminho de conversão, mas atribui mais peso ao primeiro evento e sucessivamente menos peso aos eventos seguintes.

* *[!UICONTROL First Event]:* Atribui conversões ao primeiro clique ou impressão no caminho de conversão.

* *[!UICONTROL U-shaped]:* Atribui a conversão a todos os eventos no caminho de conversão, mas atribui mais peso ao primeiro e ao último eventos, com sucessivamente menos peso para os eventos no meio do caminho de conversão.

* *[!UICONTROL Display Only]:*  Conversões de atributos para o último clique ou impressão DSP no caminho de conversão. Isso inclui vídeo e anúncios de TV conectados e exclui cliques em [!DNL Advertising Search, Social, & Commerce] anúncios.

* *[!UICONTROL Social Only]:* Obsoleto

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

**[!UICONTROL Paths as Columns]:**  (Todos [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment], e [!UICONTROL Site] relatórios com [!UICONTROL Conversion Metrics] ou [!UICONTROL Custom Goals] colunas) Quais tipos de conversões relatar quando eventos anteriores ocorreram no mesmo dispositivo. É possível incluir até três tipos. Para cada tipo selecionado, uma coluna separada é incluída para cada métrica de conversão e é anexada com o sufixo especificado ([!UICONTROL (tl)], [!UICONTROL (ct)]ou [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Inclui conversões atribuídas a cliques (CT para click-through) e a impressões (VT para view-through). As conversões atribuídas a impressões são multiplicadas pelo peso de viewthrough especificado. O peso de view-through padrão é de 100%, o que significa que as conversões atribuídas a impressões são contadas como 100% do valor das conversões atribuídas a cliques.

* *[!UICONTROL With Clicks (CT)]:* Inclui somente conversões atribuídas a cliques.

* *[!UICONTROL Impressions Only (VT)]:* Inclui somente conversões atribuídas a impressões porque nenhum clique foi rastreado no caminho de conversão.

**[!UICONTROL Conversion Reporting Based On]:**  Como relatar dados de conversão:

* *[!UICONTROL Conversion Timestamp]:* (O padrão) As conversões serão associadas à data de conversão.

* *[!UICONTROL Event Timestamp]:* As conversões serão relatadas com base na data da impressão ou clique que causou a conversão, conforme determinado pelo parâmetro especificado [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] Seção

**[!UICONTROL Destination Type]:** Escolha um dos seguintes tipos de destino:

* *[!UICONTROL S3]:* Para enviar o relatório concluído a um ou mais [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]), que você especificará nas **[!UICONTROL Destination Name]** campo.
* *[!UICONTROL sFTP]:* Para enviar o relatório concluído para um ou mais locais SFTP, que você especificará no **[!UICONTROL Destination Name]** campo.
* *[!UICONTROL FTP]:* Para enviar o relatório concluído a um ou mais locais FTP, que você especificará no **[!UICONTROL Destination Name]** campo.
* *[!UICONTROL FTP SSL](Atualmente em Beta):* Para enviar o relatório concluído a um ou mais locais SSL FTP, que você especificará no **[!UICONTROL Destination Name]** campo.
* *[!UICONTROL Email]:* Para especificar endereços de e-mail para os quais enviar relatórios completos ou notificações se o relatório for cancelado devido a erros. Para especificar vários endereços, separe-os com vírgulas ou espaços.

>[!NOTE]
>
> Não é possível alterar o tipo de destino depois de salvar o relatório.

**[!UICONTROL Destination Name]:** (Somente tipos de destino S3, FTP, sFTP e FTP SSL) Os nomes dos destinos de relatório para os quais o relatório personalizado será enviado.

* Para especificar um destino existente, selecione um nome de destino na lista. É possível selecionar vários nomes de destino separadamente.

* Para criar um novo destino:

   1. Clique em **Adicionar novo destino**.

   1. Insira o [configurações de destino do relatório](/help/dsp/reports/report-destinations/report-destination-settings.md)e clique em **Salvar**.

   1. De volta às configurações do relatório, clique em **Nomes de Destino de Atualização.**

      O novo destino agora está disponível na lista de destinos existentes, e você pode adicioná-lo ao relatório.

**[!UICONTROL Frequency]:** (Para cada [!UICONTROL Destination Name] Frequência de envio do relatório para o destino: *[!UICONTROL Once]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]* ou *[!UICONTROL Monthly]*.

## [!UICONTROL Save Report] Seção

**[!UICONTROL Send & Save]:** Quando enviar o relatório: *[!UICONTROL On Schedule]* ou *[!UICONTROL Run Now]*. Os relatórios agendados serão entregues até às 9:00 no fuso horário da conta.

>[!NOTE]
>
>Você pode [executar um relatório personalizado a qualquer momento](report-run-now.md) do [!UICONTROL Reports] exibição.

>[!MORELIKETHIS]
>
>* [Sobre Relatórios Personalizados](/help/dsp/reports/report-about.md)
>* [Criar um relatório personalizado](/help/dsp/reports/report-create.md)
>* [Duplicar um relatório personalizado](/help/dsp/reports/report-copy.md)
>* [Editar um relatório personalizado](/help/dsp/reports/report-edit.md)
>* [Executar um relatório personalizado](/help/dsp/reports/report-run-now.md)
>* [Configurações do relatório personalizado](/help/dsp/reports/report-settings.md)
>* [Sobre destinos de relatórios](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Colunas de Relatório Disponíveis](/help/dsp/reports/report-columns.md)
