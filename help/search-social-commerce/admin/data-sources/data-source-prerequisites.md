---
title: Pré-requisitos para configurar um [!DNL Google Analytics] fonte de dados
description: Saiba mais sobre as etapas que devem ser concluídas antes de configurar um [!DNL Google Analytics] fonte de dados.
role: User, Admin
exl-id: cbb2ad6d-8494-4fa4-928c-238b25bda3a6
feature: Search Admin, Search Data Sources
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Pré-requisitos para configurar um [!DNL Google Analytics] fonte de dados

Antes de poder configurar um [!DNL Google Analytics] fonte de dados, você deve estabelecer o parâmetro de sequência de consulta de Pesquisa, Social e Comércio &quot;ef_id&quot; como a chave primária para transmitir os dados do [!DNL Google Analytics] para Pesquisar, Social e Comércio. Configurar a chave primária para cada [!DNL Google Analytics] combinação de conta e propriedade para a qual você deseja sincronizar dados. Outras pessoas na sua organização podem precisar concluir essas tarefas; veja abaixo para obter mais informações.

Se os URLs da página de aterrissagem de seus anúncios ou palavras-chave ainda não incluírem os redirecionamentos de Pesquisa, Social e Comércio, adicione-os primeiro.

## Pré-requisito 1: Implementar um token de pesquisa, social e comércio (parâmetro de sequência de consulta &quot;ef_id&quot;) nos URLs da página inicial para todas as contas de publicidade aplicáveis

Em cada clique de pesquisa paga para as campanhas relevantes, uma única `ef_id` deve ser gerado e anexado ao URL da página inicial como uma sequência de consulta, como `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`, onde `&ef_id=abcde:123456789:s` é o símbolo anexar, `ef_id` e `ef_id` valor. Para incluir uma ef_id, as contas e campanhas da rede de anúncios relevantes devem ter a [!UICONTROL Tracking Type] &quot;[!UICONTROL EF Redirect]&quot; e o [!UICONTROL Redirect Type] &quot;[!UICONTROL Token].&quot;

Para contas e campanhas existentes, a ef_id provavelmente já está implementada.

Se a ef_id não for incluída, peça ajuda à sua equipe de conta do Adobe.

Quando todos os pré-requisitos estiverem concluídos, a variável `ef_id` é usada como chave primária para enviar dados do [!DNL Google Analytics] para Pesquisar, Social e Comércio.

## Pré-requisito 2: Capturar o token de Pesquisa, Social e Comércio (parâmetro de sequência de consulta &quot;ef_id&quot;) em uma dimensão personalizada para cada relevante [!DNL Google Analytics] propriedade

Repita as seguintes tarefas para cada [!DNL Google Analytics] combinação de conta e propriedade para a qual você deseja sincronizar dados. Consulte [[!DNL Google Analytics] documentação sobre criação e implementação de dimensões personalizadas](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) para obter ajuda com essas tarefas.

1. Entrada [!DNL Google Analytics], crie uma dimensão personalizada com o nome &quot;`ef_id`&quot;. Defina o escopo da dimensão como [!DNL User]e defina a dimensão como ativa.

   >[!NOTE]
   >
   >Este pré-requisito requer a permissão de edição para as propriedades relevantes.

1. Atualize seu [!DNL Google Analytics] código de rastreamento para capturar o valor do parâmetro de sequência de consulta ef_id quando ele está presente no URL da página inicial e armazená-lo na dimensão personalizada ef_id.

   >[!NOTE]
   >
   >O ef_id deve estar somente nos URLs da página inicial.

   Por exemplo, se o URL da landing page for `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`, o valor da dimensão ef_id em [!DNL Google Analytics] é `abcde:123456789:s`.

   >[!NOTE]
   >
   >Esse pré-requisito deve ser preenchido por um desenvolvedor qualificado.

>[!MORELIKETHIS]
>
>* [Sobre sincronização [!DNL Google Analytics] métricas de conversão](data-source-about.md)
>* [Configurar um [!DNL Google Analytics] exibir como fonte de dados](data-source-configure.md)
>* [Editar um [!DNL Google Analytics] fonte de dados](data-source-edit.md)
>* [Pausar sincronização de uma fonte de dados](data-source-pause.md)
>* [Reautenticar um [!DNL Google Analytics] fonte de dados](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] configurações da fonte de dados](data-source-settings.md)
>* [Apêndice - Disponível [!DNL Google Analytics] métricas](data-source-ga-metrics.md)
