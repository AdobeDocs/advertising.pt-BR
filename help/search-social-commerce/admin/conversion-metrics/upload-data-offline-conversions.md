---
title: Fazer upload de dados de conversão offline para conversões aprimoradas
description: Saiba como carregar dados de conversão offline próprios para mapear a [!DNL Google Ads] conversões avançadas para clientes potenciais e [!DNL Microsoft Advertising] conversões avançadas.
feature: Conversions
exl-id: 5c5dfbb8-3b17-4973-8012-fc7f0e97e33b
source-git-commit: eb7320fdddce4895a689c32ec6fb1e44cb8f2705
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 0%

---

# Fazer upload de dados de conversão offline para conversões aprimoradas

*[!DNL Google Ads]e [!DNL Microsoft Advertising] contas apenas*

Você pode carregar dados de conversão offline primários, incluindo endereços de email com hash e números de telefone, para mapear para suas [[!DNL Google Ads] conversões avançadas](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) e [[!DNL Microsoft Advertising] conversões avançadas](https://help.ads.microsoft.com/#apex/ads/en/60178) existentes. Todos os dados carregados são sincronizados em tempo real com a rede de publicidade.

## Carregar dados para conversões aprimoradas

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]** e depois clique na guia **[!UICONTROL Upload]**.

1. Selecione a rede de publicidade e depois a conta.

1. (Opcional) Para baixar um modelo com todos os [campos de dados obrigatórios](#enhanced-conversions-leads-data) no formato [!DNL Microsoft Excel], clique em **[!UICONTROL View Template]** e baixe o arquivo de acordo com o procedimento normal do navegador.

   É possível editar o arquivo para incluir seus dados, salvar as alterações e fazer upload do arquivo na próxima etapa.

1. Clique em **[!UICONTROL Choose File]** e selecione um arquivo para carregar do seu dispositivo ou rede.

## Dados necessários para arquivos carregados {#enhanced-conversions-leads-data}

### Dados acima da tabela

`Parameters:TimeZone=insert_timezone`

Insira o fuso horário da conta neste local ou na coluna &quot;[!UICONTROL Conversion Time]&quot; para cada linha. Use a\) ([!DNL Google Ads only]) o [formato de ID de fuso horário com suporte](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) ou b\) o deslocamento GMT, conforme indicado por + ou - e a diferença de tempo de 4 dígitos (como -0500 para Nova York, +0100 para Berlim ou +0000 para o Horário de Greenwich).

### Colunas e valores de tabela para [!DNL Google Ads]

| Coluna | Descrição |
| ------ | ----------- |
| Email | O endereço de email do usuário, que deve ser transformado em hash usando o algoritmo SHA -256. Cada linha deve incluir um valor de Email ou um valor de Número de Telefone. |
| Número de telefone | O número de telefone do usuário, que deve ser transformado em hash usando o algoritmo SHA -256. Deve incluir um código de país e pode conter traços e outros símbolos. Cada linha deve incluir um valor de Email ou um valor de Número de Telefone. |
| Nome da conversão | (Obrigatório) O nome da ação de conversão. |
| Tempo de conversão | (Obrigatório) A hora em que o evento de conversão ocorreu em um [formato de hora com suporte](https://support.google.com/google-ads/answer/7014069#prepare_data). Se você não incluir a ID de fuso horário da conta na linha `Parameters:TimeZone=insert_timezone` acima da tabela de dados, inclua o fuso horário de cada linha usando a\) o [formato de ID de fuso horário com suporte](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) ou b\) o deslocamento GMT, conforme indicado por + ou - e a diferença de tempo de 4 dígitos (como -0500 para Nova York, +0100 para Berlim ou +0000 para o Horário de Greenwich). |
| Valor de conversão | (Obrigatório) O valor numérico de conversão. |
| Moeda de conversão | O código de moeda do evento de conversão. |
| Adicionar dados do usuário | (Aplicável para dados relativos a usuários no Espaço Econômico Europeu (EEE) ou Reino Unido (Reino Unido)) Indica se o consentimento do usuário foi dado para enviar dados do usuário para [!DNL Google] para fins de personalização de anúncios. Os valores podem incluir `Granted`, `Denied` ou \[null\] (que é enviado para [!DNL Google Ads] como `Unspecified`). **Observação:** [!DNL Google Ads] atualmente não impõe consentimento para conversões avançadas para clientes potenciais, mas pode fazê-lo no futuro. |
| Ad Personalization | (Aplicável para dados relativos a usuários no Espaço Econômico Europeu (EEE) ou Reino Unido (Reino Unido)) Indica se o consentimento do usuário foi dado para enviar dados do usuário para [!DNL Google] para fins de publicidade. Os valores podem incluir `Granted`, `Denied` ou \[null\] (que é enviado para [!DNL Google Ads] como `Unspecified`). **Observação:** [!DNL Google Ads] atualmente não impõe consentimento para conversões avançadas para clientes potenciais, mas pode fazê-lo no futuro. |

### Colunas e valores de tabela para [!DNL Microsoft Advertising]

Para obter mais instruções sobre como usar o modelo, consulte [https://help.ads.microsoft.com/#apex/3/56852](https://help.ads.microsoft.com/#apex/3/56852).

| Coluna | Descrição |
| ------ | ----------- |
| Nome da conversão | (Obrigatório) O nome da meta de conversão. |
| Tempo de conversão | (Obrigatório) A hora em que o evento de conversão ocorreu. Se você não incluir a ID de fuso horário da conta na linha `Parameters:TimeZone=insert_timezone` acima da tabela de dados, inclua o fuso horário de cada linha usando o deslocamento GMT, conforme indicado por + ou - e a diferença de tempo de 4 dígitos (como -0500 para Nova York, +0100 para Berlim ou +0000 para o Horário de Greenwich). Para obter uma lista de fusos horários de várias cidades, consulte [https://learn.microsoft.com/en-us/advertising/guides/time-zones](https://learn.microsoft.com/en-us/advertising/guides/time-zones), mas certifique-se de usar o formato especificado aqui em vez do formato na lista de fusos horários. |
| Valor de conversão | (Obrigatório) O valor numérico de conversão. |
| Moeda de conversão | O código de moeda do evento de conversão. |
| ID de cliques do Microsoft | O identificador de clique [!DNL Microsoft] exclusivo associado (MSCLKID). Este campo pode estar vazio para conversões offline aprimoradas. |
| Endereço de email com hash | O endereço de email do usuário, que deve ser transformado em hash usando o algoritmo SHA -256. Para conversões offline aprimoradas, cada linha deve incluir um valor de Endereço de email com hash ou um valor de Número de telefone com hash. |
| Número de telefone com hash | O número de telefone do usuário, que deve ser transformado em hash usando o algoritmo SHA -256. Deve incluir um código de país e pode conter traços e outros símbolos. Para conversões offline aprimoradas, cada linha deve incluir um valor de Endereço de email com hash ou um valor de Número de telefone com hash. |

>[!MORELIKETHIS]
>
>* [Implementar [!DNL Google Ads] conversões aprimoradas para clientes potenciais](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [Implementar [!DNL Microsoft Advertising] conversões offline aprimoradas](/help/search-social-commerce/campaign-management/special-workflows/microsoft-enhanced-conversions.md)
>* ([!DNL Google Ads only])[Criar uma ação de conversão para uma [!DNL Google Ads] conversão aprimorada para clientes potenciais](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Carregar métricas de conversão rastreadas por Pesquisa, Social e Commerce para [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
