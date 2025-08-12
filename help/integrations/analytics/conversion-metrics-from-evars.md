---
title: Criar métricas de conversão do Adobe Analytics [!DNL eVars]  e props
description: Configure métricas de evento bem-sucedidas personalizadas usando dados de nível  [!DNL eVar] e  [!DNL prop].
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
source-git-commit: be78460b42e1d9622cb781a0a32b01a34464a76d
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# Criar métricas de conversão do Adobe Analytics [!DNL eVars] e [!DNL props]

*Anunciantes com apenas uma integração Adobe Advertising-Adobe Analytics*

Você pode usar as métricas de evento de sucesso para otimizar pacotes do DSP e campanhas de Pesquisa, Social e Commerce com base nos dados do site da Adobe Analytics que melhor se ajustam aos objetivos da sua marca. Você pode configurar métricas de evento bem-sucedidas personalizadas com base em suas [[!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=pt-BR) e [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html?lang=pt-BR) existentes, canalizando dados de nível [!DNL eVar] e [!DNL prop] para um evento. Outras métricas do [!DNL Analytics], incluindo métricas de conversão e métricas de tráfego padrão, personalizadas e reservadas, estão automaticamente disponíveis no DSP e no Search, Social e Commerce.

![Exemplo de uso](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Exemplo de uso")

A maioria das tarefas a seguir deve ser executada por um administrador [!DNL Analytics] ou outro usuário. Se precisar de assistência, entre em contato com a equipe de conta da Adobe.

1. Em [!DNL Analytics], [crie um evento bem-sucedido de espaço reservado](https://experienceleague.adobe.com/pt-br/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-event).

   Use os seguintes parâmetros adicionais:

   **Tipo:** `Counter`

   **Polaridade:** `Up is Good` ou `Up is Bad`

   **Visibilidade:** `Visible Everywhere`

   **Gravação de Evento Exclusiva:** `Always Record Event`

   **Participação:** `Enabled`

   Você não precisa implementar o novo evento no site da sua marca porque ele usa dados existentes que já foram capturados.

1. Criar e validar uma regra de processamento em [!DNL Analytics]:

   >[!NOTE]
   >
   >Somente administradores de conta do [!DNL Analytics] podem criar regras de processamento, a menos que tenham concedido permissão para não administradores.

   1. [Criar uma regra de processamento](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=pt-BR), usando esta configuração:

      * Para a condição que deve ser atendida, especifique o(s) [!DNL eVars] ou [!DNL props] necessário(s).

        Você pode configurar níveis adicionais de granularidade, conforme necessário, para garantir a criação dos eventos mais precisos.

        >[!TIP]
        >
        >A prática recomendada é usar somente um [!DNL eVar] ou [!DNL prop].

      * Para a ação, selecione **Definir Evento** e selecione o evento de espaço reservado.

   1. Em [!DNL Analytics] [!DNL Analysis Workspace], [crie um projeto](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=pt-BR) e coloque o novo evento em uma tabela de forma livre para garantir que os dados sejam preenchidos para a métrica [!DNL eVar] ou [!DNL prop].

1. Entre em contato com a equipe de conta da Adobe para sincronizar a nova métrica com o Adobe Advertising.

Depois que a métrica estiver disponível, você poderá usá-la para criar um objetivo, que poderá ser atribuído a um portfólio de Pesquisa, Social e Commerce ou usar como uma [meta personalizada](/help/dsp/optimization/custom-goal.md) para um pacote do DSP.

Para obter mais informações sobre como criar objetivos, consulte o capítulo do Guia de Otimização em &quot;Objetivos&quot;, disponível no Search, Social e Commerce

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Dados no Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Exibir as métricas de conversão rastreadas para um anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
