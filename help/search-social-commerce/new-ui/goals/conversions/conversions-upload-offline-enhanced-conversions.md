---
title: (Nova interface do usuário) Fazer upload de dados de conversão offline para conversões aprimoradas
description: Saiba como carregar dados de conversão offline próprios para mapear a [!DNL Google Ads] conversões avançadas para clientes potenciais e [!DNL Microsoft Advertising] conversões avançadas.
feature: Conversions
feature_v2: id: e6916c1b-e939-4e0b-99f5-768e83e1e99fid: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: d068b149-b9d1-421c-9033-a51495366ddc
source-git-commit: 0bfee2b52410b5cab8e9b3dfba35effc36fc40e1
workflow-type: tm+mt
source-wordcount: 903
ht-degree: 0%

---

# Fazer upload de dados de conversão offline para conversões aprimoradas

*[!DNL Google Ads]e [!DNL Microsoft Advertising] contas apenas*

Você pode carregar dados de conversão offline primários, incluindo endereços de email com hash e números de telefone, para mapear para suas [[!DNL Google Ads] conversões avançadas](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) e [[!DNL Microsoft Advertising] conversões avançadas](https://help.ads.microsoft.com/#apex/ads/en/60178) existentes. Todos os dados carregados são sincronizados em tempo real com a rede de publicidade.

## (Nova interface de usuário) Fazer upload de dados para conversões aprimoradas

*recurso do Beta*

1. No menu principal, clique em **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Acima da tabela de dados, clique em **[!UICONTROL Set up Conversion]**.

1. Especifique as configurações de upload de dados:

   1. Na guia [!UICONTROL Basic Details]:

      1. Selecione o [!UICONTROL Setup Method] *[!UICONTROL Data Upload]*.

      1. Selecione o [!UICONTROL Platform]: *[!UICONTROL Google]* ou *[!UICONTROL Microsoft]*.

      1. Clique em **[!UICONTROL Next]**.

   1. Na guia [!UICONTROL Configure]:

      1. (Opcional) Para baixar um modelo com todos os [campos de dados obrigatórios](#enhanced-conversions-leads-data) no formato [!DNL Microsoft Excel], clique em **[!UICONTROL Download Template]** e baixe o arquivo de acordo com o procedimento normal do navegador.

         É possível editar o arquivo para incluir seus dados, salvar as alterações e, em seguida, fazer upload do arquivo para a conta de rede de publicidade especificada.

      1. Selecione a conta de rede de publicidade para a qual os dados serão carregados.

      1. Na caixa [!UICONTROL Upload Conversion File], siga um destes procedimentos:

         * Arraste um arquivo para a caixa.

         * Clique em **[!UICONTROL Browse File]** e selecione um arquivo para carregar do seu dispositivo ou rede.

   1. Clique em **[!UICONTROL Review and Save]** para examinar as configurações.

   1. Clique em **[!UICONTROL Upload]**.

## (Interface herdada) Fazer upload de dados para conversões aprimoradas

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]** e depois clique na guia **[!UICONTROL Upload]**.

1. Selecione a rede de publicidade e depois a conta.

1. (Opcional) Para baixar um modelo com todos os [campos de dados obrigatórios](#enhanced-conversions-leads-data) no formato [!DNL Microsoft Excel], clique em **[!UICONTROL View Template]** e baixe o arquivo de acordo com o procedimento normal do navegador.

   É possível editar o arquivo para incluir seus dados, salvar as alterações e fazer upload do arquivo na próxima etapa.

1. Clique em **[!UICONTROL Choose File]** e selecione um arquivo para carregar do seu dispositivo ou rede.

## Dados necessários para arquivos carregados {#enhanced-conversions-leads-data}

### Dados acima da tabela

`Parameters:TimeZone=insert_timezone`

Insira o fuso horário da conta neste local ou na coluna &quot;[!UICONTROL Conversion Time]&quot; para cada linha. Use a\) ([!DNL [!DNL Google Ads] somente]) o [formato de ID de fuso horário com suporte](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) ou b\) o deslocamento GMT, conforme indicado por + ou - e a diferença de tempo de 4 dígitos (como -0500 para Nova York, +0100 para Berlim ou +0000 para o Horário de Greenwich).

### Colunas e valores de tabela para [!DNL Google Ads]

| Coluna | Descrição |
| ------ | ----------- |
| [!UICONTROL Email] | O endereço de email do usuário, que deve ser transformado em hash usando o algoritmo SHA -256. Cada linha deve incluir um valor [!UICONTROL Email] ou [!UICONTROL Phone Number]. |
| [!UICONTROL Phone Number] | O número de telefone do usuário, que deve ser transformado em hash usando o algoritmo SHA -256. Deve incluir um código de país e pode conter traços e outros símbolos. Cada linha deve incluir um valor [!UICONTROL Email] ou [!UICONTROL Phone Number]. |
| [!UICONTROL Conversion Name] | (Obrigatório) O nome da ação de conversão. |
| [!UICONTROL Conversion Time] | (Obrigatório) A hora em que o evento de conversão ocorreu em um [formato de hora com suporte](https://support.google.com/google-ads/answer/7014069#prepare_data). Se você não incluir a ID de fuso horário da conta na linha `Parameters:TimeZone=insert_timezone` acima da tabela de dados, inclua o fuso horário de cada linha usando a\) o [formato de ID de fuso horário com suporte](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) ou b\) o deslocamento GMT, conforme indicado por + ou - e a diferença de tempo de 4 dígitos (como -0500 para Nova York, +0100 para Berlim ou +0000 para o Horário de Greenwich). |
| [!UICONTROL Conversion Value] | (Obrigatório) O valor numérico de conversão. |
| [!UICONTROL Conversion Currency] | O código de moeda do evento de conversão. |
| [!UICONTROL Ad User Data] | (Aplicável para dados relativos a usuários no Espaço Econômico Europeu (EEE) ou Reino Unido (Reino Unido)) Indica se o consentimento do usuário foi dado para enviar dados do usuário para [!DNL Google] para fins de personalização de anúncios. Os valores podem incluir `Granted`, `Denied` ou \[null\] (que é enviado para [!DNL Google Ads] como `Unspecified`). **Observação:** [!DNL Google Ads] atualmente não impõe consentimento para conversões avançadas para clientes potenciais, mas pode fazê-lo no futuro. |
| [!UICONTROL Ad Personalization] | (Aplicável para dados relativos a usuários no Espaço Econômico Europeu (EEE) ou Reino Unido (Reino Unido)) Indica se o consentimento do usuário foi dado para enviar dados do usuário para [!DNL Google] para fins de publicidade. Os valores podem incluir `Granted`, `Denied` ou \[null\] (que é enviado para [!DNL Google Ads] como `Unspecified`). **Observação:** [!DNL Google Ads] atualmente não impõe consentimento para conversões avançadas para clientes potenciais, mas pode fazê-lo no futuro. |

### Colunas e valores de tabela para [!DNL Microsoft Advertising]

Para obter mais instruções sobre formatação e hash dos dados, consulte a documentação do [!DNL Microsoft Ads] em [Conversões aprimoradas](https://help.ads.microsoft.com/#apex/ads/60178).

| Coluna | Descrição |
| ------ | ----------- |
| [!UICONTROL Email] | O endereço de email do usuário, que deve ser transformado em hash usando o algoritmo SHA -256. Cada linha deve incluir um valor [!UICONTROL Email] ou [!UICONTROL Phone Number]. |
| [!UICONTROL Phone Number] | O número de telefone do usuário, que deve ser transformado em hash usando o algoritmo SHA -256. Deve incluir um código de país e pode conter traços e outros símbolos. Para conversões offline aprimoradas, cada linha deve incluir um valor [!UICONTROL Email] ou [!UICONTROL Phone Number]. |
| [!UICONTROL Conversion Name] | (Obrigatório) O nome da ação de conversão. |
| [!UICONTROL Conversion Time] | (Obrigatório) A hora em que o evento de conversão ocorreu. Se você não incluir a ID de fuso horário da conta na linha `Parameters:TimeZone=insert_timezone` acima da tabela de dados, inclua o fuso horário de cada linha usando o deslocamento GMT, conforme indicado por + ou - e a diferença de tempo de 4 dígitos (como -0500 para Nova York, +0100 para Berlim ou +0000 para o Horário de Greenwich). Para obter uma lista de fusos horários de várias cidades, consulte [https://learn.microsoft.com/en-us/advertising/guides/time-zones](https://learn.microsoft.com/en-us/advertising/guides/time-zones), mas certifique-se de usar o formato especificado aqui em vez do formato na lista de fusos horários. |
| [!UICONTROL Conversion Value] | (Obrigatório) O valor numérico de conversão. |
| [!UICONTROL Conversion Currency] | O código de moeda do evento de conversão. |

>[!MORELIKETHIS]
>
>* [Implementar [!DNL Google Ads] conversões aprimoradas para clientes potenciais](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [Implementar [!DNL Microsoft Advertising] conversões offline aprimoradas](/help/search-social-commerce/campaign-management/special-workflows/microsoft-enhanced-conversions.md)
>* [Criar uma ação de conversão para uma [!DNL Google Ads] conversão aprimorada para clientes potenciais](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Carregar métricas de conversão rastreadas por Pesquisa, Social e Commerce para [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
