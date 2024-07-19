---
title: Configurar uma visualização  [!DNL Google Analytics]  como fonte de dados
description: Saiba como configurar uma fonte de dados a partir de uma visualização  [!DNL Google Analytics] .
role: User, Admin
exl-id: 9e299e42-4971-49ea-a515-54a97eb13e0d
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# Configurar uma visualização [!DNL Google Analytics] como fonte de dados

*Somente Administradores de Agência, Gerentes de Conta de Agência, Gerentes de Conta de Adobe e Administradores*

Você pode criar uma fonte de dados por [!DNL Google Analytics] combinação de conta, propriedade e visualização.

Para integrar métricas de várias propriedades ou de várias exibições de uma única propriedade, configure uma fonte de dados separada para cada uma.

1. [Executar todos os pré-requisitos para integrar a [!DNL Google Analytics] conta](data-source-prerequisites.md).

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar").

1. Na caixa de diálogo [!UICONTROL Deployment Prerequisites], marque a caixa de seleção para confirmar se a dimensão personalizada necessária &quot;ef_id&quot; está implementada na conta [!DNL Google Analytics] e clique em **[!UICONTROL Continue]**.

   Alguns pré-requisitos podem ter sido executados por outras funções em sua organização. Em caso de dúvidas sobre os pré-requisitos, entre em contato com a equipe de conta do Adobe.

1. Insira as [configurações da fonte de dados](data-source-settings.md):

   1. Na seção **[!UICONTROL Connect to [!DNL Google Analytics]]**, faça o seguinte.

      1. Insira a ID numérica da conta [!DNL Google Analytics].

      1. Insira o endereço de email a ser usado para acessar os dados desta fonte de dados. O endereço de email deve ser registrado em uma conta [!DNL Google] e ter permissões de &quot;Leitura e Análise&quot; para a conta [!DNL Google Analytics]. Consulte as [instruções para atribuir permissões de usuário em [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Para garantir que apenas propriedades e exibições específicas do [!DNL Google Analytics] estejam disponíveis no Adobe Advertising, faça logon usando um endereço de email que tenha acesso somente a essas propriedades e exibições.

         >[!NOTE]
         >
         >Se posteriormente você alterar a senha dessa conta de email, todas as conexões abertas com a conta de email serão fechadas. Para retomar a sincronização de dados, retorne a esta página e [autentique novamente](data-source-reauthenticate.md).

      1. Marque a caixa de seleção para autorizar o Adobe Advertising a acessar as métricas da conta.

      1. Clique em **[!UICONTROL Authenticate]**.

   1. Na seção [!UICONTROL Account Details], especifique a propriedade e a exibição das métricas a serem importadas. Além disso, especifique a dimensão personalizada que é preenchida com o valor do parâmetro de sequência de consulta &quot;ef_id&quot;.

   1. Na seção [!UICONTROL Import Metrics], especifique as métricas a serem incluídas nos feeds.

      Você não pode remover [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces] ou [!UICONTROL Session Duration], que são incluídos automaticamente. É possível adicionar até 16 métricas válidas adicionais ou métricas sem dados.

      >[!WARNING]
      >
      >O [!DNL Google Analytics] permite até 10 métricas em um único feed de dados. Search, Social e Commerce podem oferecer suporte a até dois feeds com um total de 20 métricas, mas o uso de um segundo feed dobra suas chamadas de API para [!DNL Google Analytics]. Se você tiver muitas métricas, selecione somente as métricas que deseja usar nos objetivos de otimização. Veja mais sobre [cotas e limites de chamada para solicitações de API para [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. Na seção [!UICONTROL Metric Tag], digite o nome da tag a ser anexada a cada métrica da fonte de dados.

1. No canto superior direito, clique em **[!UICONTROL Post]**.

   A fonte de dados é chamada de &quot;AccountName > PropertyName > ViewName&quot; e é ativada automaticamente. Para pausar a fonte de dados, consulte &quot;[Pausar um Feed de uma Source de Dados](data-source-pause.md)&quot;.

   As métricas estarão disponíveis no dia seguinte após a conclusão da sincronização diária de dados, que começa às 5:00 no fuso horário do anunciante. Quando as métricas estiverem disponíveis, elas estarão visíveis em [[!UICONTROL Admin] > [!UICONTROL Conversions]](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md). Cada nova métrica de conversão é chamada de &quot;`ga:backEndMetricName_propertyID_viewID`&quot;, onde &quot;backEndMetricName&quot; é o nome da métrica usado pela API. O nome para exibição de cada nova métrica de conversão é &quot;`friendlyMetricName_ga:MetricTag`&quot;, onde &quot;friendlyMetricName&quot; é o nome da métrica que aparece em [!DNL Google Analytics] e &quot;MetricTag&quot; é o [!UICONTROL Metric Tag] definido nas configurações da fonte de dados.

   Você pode adicionar as métricas diretamente ao gerenciamento de campanhas e às visualizações, relatórios e objetivos de otimização do gerenciamento de portfólio.

>[!MORELIKETHIS]
>
>* [Sobre a sincronização [!DNL Google Analytics] de métricas de conversão](data-source-about.md)
>* [Pré-requisitos para configurar uma [!DNL Google Analytics] fonte de dados](data-source-prerequisites.md)
>* [Editar uma [!DNL Google Analytics] fonte de dados](data-source-edit.md)
>* [Pausar sincronização de uma fonte de dados](data-source-pause.md)
>* [Reautenticar uma [!DNL Google Analytics] fonte de dados](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] configurações da fonte de dados](data-source-settings.md)
>* [Apêndice - Disponível [!DNL Google Analytics] métricas](data-source-ga-metrics.md)
