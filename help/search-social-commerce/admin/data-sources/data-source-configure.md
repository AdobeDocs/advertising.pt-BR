---
title: Configurar um [!DNL Google Analytics] exibir como fonte de dados
description: Saiba como configurar uma fonte de dados a partir de um [!DNL Google Analytics] exibição.
role: User, Admin
exl-id: 583cf9aa-861c-4faf-a707-1def4e983b93
feature: Search Admin, Search Data Sources
source-git-commit: b730716565dfae9cb32556eaede1c3f29f316ac7
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# Configurar um [!DNL Google Analytics] exibir como fonte de dados

*Somente administradores de agências, gerentes de conta de agências, gerentes de conta do Adobe e administradores*

É possível criar uma fonte de dados por [!DNL Google Analytics] combinação de conta, propriedade e visualização.

Para integrar métricas de várias propriedades ou de várias exibições de uma única propriedade, configure uma fonte de dados separada para cada uma.

1. [Execute todos os pré-requisitos para integrar o [!DNL Google Analytics] account](data-source-prerequisites.md).

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar").

1. No [!UICONTROL Deployment Prerequisites] , marque a caixa de seleção para confirmar que a dimensão personalizada necessária &quot;ef_id&quot; está implementada na [!DNL Google Analytics] e clique em **[!UICONTROL Continue]**.

   Alguns pré-requisitos podem ter sido executados por outras funções em sua organização. Em caso de dúvidas sobre os pré-requisitos, entre em contato com a equipe de conta do Adobe.

1. Insira o [configurações da fonte de dados](data-source-settings.md):

   1. No **[!UICONTROL Connect to [!DNL Google Analytics]]** faça o seguinte.

      1. Insira a ID numérica para o [!DNL Google Analytics] conta.

      1. Insira o endereço de email a ser usado para acessar os dados desta fonte de dados. O endereço de e-mail deve ser registrado em um [!DNL Google] conta e têm permissões de &quot;Ler e analisar&quot; para a [!DNL Google Analytics] conta. Consulte a [instruções para atribuição de permissões de usuário no [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Para garantir que apenas [!DNL Google Analytics] as propriedades e as visualizações estão disponíveis no Adobe Advertising, faça logon usando um endereço de email que tenha acesso somente a essas propriedades e visualizações.

         >[!NOTE]
         >
         >Se posteriormente você alterar a senha dessa conta de email, todas as conexões abertas com a conta de email serão fechadas. Para retomar a sincronização de dados, retorne a esta página e [reautenticar](data-source-reauthenticate.md).

      1. Marque a caixa de seleção para autorizar o Adobe Advertising a acessar as métricas da conta.

      1. Clique em **[!UICONTROL Authenticate]**.

   1. No [!UICONTROL Account Details] especifique a propriedade e a visualização das métricas que serão importadas. Além disso, especifique a dimensão personalizada que é preenchida com o valor do parâmetro de sequência de consulta &quot;ef_id&quot;.

   1. No [!UICONTROL Import Metrics] especifique as métricas a serem incluídas no(s) feed(s).

      Você não pode remover [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces]ou [!UICONTROL Session Duration], que são incluídos automaticamente. É possível adicionar até 16 métricas válidas adicionais ou métricas sem dados.

      >[!WARNING]
      >
      >[!DNL Google Analytics] permite até 10 métricas em um único feed de dados. A Search, Social e Commerce pode oferecer suporte a até dois feeds com um total de 20 métricas, mas o uso de um segundo feed dobra suas chamadas de API para [!DNL Google Analytics]. Se você tiver muitas métricas, selecione somente as métricas que deseja usar nos objetivos de otimização. Veja mais sobre [cotas e limites de chamada para solicitações de API para [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. No [!UICONTROL Metric Tag] insira o nome da tag a ser anexada a cada métrica da fonte de dados.

1. No canto superior direito, clique em **[!UICONTROL Post]**.

   A fonte de dados é chamada de &quot;AccountName > PropertyName > ViewName&quot; e é ativada automaticamente. Para pausar a fonte de dados, consulte &quot;[Pausar um feed de uma fonte de dados](data-source-pause.md).&quot;

   As métricas estarão disponíveis no dia seguinte após a conclusão da sincronização diária de dados, que começa às 5:00 no fuso horário do anunciante. Quando as métricas estiverem disponíveis, elas ficarão visíveis no [[!UICONTROL Admin] > [!UICONTROL Transaction Properties]](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md). Cada nova métrica de conversão é chamada de &quot;`ga:backEndMetricName_propertyID_viewID`,&quot; onde &quot;backEndMetricName&quot; é o nome da métrica usada pela API. O nome de exibição para cada nova métrica de conversão é &quot;`friendlyMetricName_ga:MetricTag`,&quot; onde &quot;friendlyMetricName&quot; é o nome da métrica que aparece em [!DNL Google Analytics] e &quot;MetricTag&quot; é o [!UICONTROL Metric Tag] definido nas configurações da fonte de dados.

   Você pode adicionar as métricas diretamente ao gerenciamento de campanhas e às visualizações, relatórios e objetivos de otimização do gerenciamento de portfólio.

>[!MORELIKETHIS]
>
>* [Sobre sincronização [!DNL Google Analytics] métricas de conversão](data-source-about.md)
>* [Pré-requisitos para configurar um [!DNL Google Analytics] fonte de dados](data-source-prerequisites.md)
>* [Editar um [!DNL Google Analytics] fonte de dados](data-source-edit.md)
>* [Pausar sincronização de uma fonte de dados](data-source-pause.md)
>* [Reautenticar um [!DNL Google Analytics] fonte de dados](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] configurações da fonte de dados](data-source-settings.md)
>* [Apêndice - Disponível [!DNL Google Analytics] métricas](data-source-ga-metrics.md)
