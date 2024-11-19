---
title: Implementar [!DNL Google Ads] conversões aprimoradas para clientes potenciais
description: Saiba mais sobre o fluxo de trabalho para configurar [!DNL Google Ads] conversões avançadas para clientes potenciais.
feature: Search Campaign Management, Conversions
exl-id: b708c9f2-2962-45d9-8780-4e96ef2ae8f7
source-git-commit: 56161ece4ba9c01cddb86e16796150c391f1a811
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# Implementar [!DNL Google Ads] conversões aprimoradas para clientes potenciais

*[!DNL Google Ads]somente contas*

[[!DNL Google Ads] as conversões aprimoradas para clientes potenciais](https://support.google.com/google-ads/answer/9888656) permitem mapear usuários para conversões offline usando seus dados de conversão primários. Use conversões aprimoradas para clientes potenciais em ambientes em que as IDs de clique não estão disponíveis, como para rastrear vendas por telefone ou email resultantes de clientes potenciais do site.

No Search, Social e Commerce, você pode:

* Exibir suas conversões aprimoradas existentes para clientes potenciais.

  O Search, Social e Commerce sincroniza suas conversões aprimoradas existentes para leads diariamente às 05:00 no fuso horário do anunciante.

* Criar conversões aprimoradas para clientes potenciais.

* Fazer upload de dados de conversão originais e offline para mapear para suas conversões aprimoradas de clientes potenciais.

* Inclua suas conversões aprimoradas para clientes potenciais como métricas nos relatórios e como métricas ponderadas nos objetivos de otimização.

Para usar esse recurso, conclua as etapas a seguir. As etapas para criar tags de rastreamento de conversão e criar ações de conversão podem, opcionalmente, ser revertidas.

1. Em [!DNL Google Ads], aceitar conversões aprimoradas para clientes potenciais:

   1. Abra as configurações de conversão da conta.

   1. Selecione a opção de conversões avançadas para clientes potenciais e aceite os termos de serviço.

   1. Selecione se deseja usar uma marca [!DNL Google] ou [!DNL Google Tag Manager] para criar a marca de conversão.


1. Configure e implemente uma tag [!DNL Google] para a ação de conversão.

   Para obter instruções, consulte a ajuda do [!DNL Google Ads] para criar marcas para conversões aprimoradas de clientes potenciais [usando uma [!DNL Google] marca](https://support.google.com/google-ads/answer/11021502) ou [usando [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11347292).

1. Crie uma ação de conversão para a conversão aprimorada de clientes potenciais no [Search, Social e Commerce](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) ou no [Google Ads](https://support.google.com/google-ads/answer/12216226).

   Para o **Tipo de Conversão,** selecione *Importar Conversão* ou *Importar.*

1. Sempre que necessário, carregue dados primários, incluindo endereços de email com hash ou números de telefone, para atribuir à conversão de uma conta especificada. Você pode concluir esta etapa no [Search, Social e Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) ou usando o [!DNL Google Data Manager].

   * Em Pesquisa, Social e Commerce, você pode baixar um modelo no formato [!DNL Microsoft Excel], inserir seus dados de conversão e salvar o arquivo localmente e, em seguida, carregar o arquivo editado. O modelo inclui colunas para indicar se o usuário consentiu em fazer upload de dados para [!DNL Google] para fins de publicidade e personalização de anúncios.

     Todos os dados carregados são sincronizados em tempo real para [!DNL Google Ads].

   * Para obter mais informações sobre como carregar dados usando o [!DNL Google Data Manager], consulte &quot;[Sobre o Gerenciador de dados](https://support.google.com/google-ads/answer/14639041).&quot;

>[!MORELIKETHIS]
>
>* [Criar uma ação de conversão para uma [!DNL Google Ads] conversão aprimorada para clientes potenciais](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Carregar dados de conversão offline para conversões aprimoradas](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
