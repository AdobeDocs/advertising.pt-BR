---
title: Pré-requisitos para configurar uma fonte de dados  [!DNL Google Analytics]
description: Saiba mais sobre as etapas que devem ser concluídas antes de configurar uma fonte de dados  [!DNL Google Analytics] .
role: User, Admin
exl-id: 97b0c149-5f82-4a1e-a5d9-aeab43cbd88f
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Pré-requisitos para configurar uma fonte de dados [!DNL Google Analytics]

Antes de configurar uma fonte de dados [!DNL Google Analytics], é necessário estabelecer o parâmetro de sequência de consulta de Pesquisa, Social e Commerce &quot;ef_id&quot; como a chave primária para transmitir dados de [!DNL Google Analytics] para Pesquisa, Social e Commerce. Configure a chave primária para cada combinação de conta e propriedade do [!DNL Google Analytics] para a qual deseja sincronizar dados. Outras pessoas na sua organização podem precisar concluir essas tarefas; veja abaixo para obter mais informações.

Se os URLs da página de aterrissagem de seus anúncios ou palavras-chave ainda não incluírem os redirecionamentos de Pesquisa, Social e Commerce, adicione-os primeiro.

## Pré-requisito 1: Implementar um token de Pesquisa, Social e Commerce (parâmetro de sequência de consulta &quot;ef_id&quot;) nos URLs da página inicial para todas as contas de publicidade aplicáveis

Em cada clique de pesquisa paga para as campanhas relevantes, um `ef_id` exclusivo deve ser gerado e anexado à URL da página de aterrissagem como uma sequência de consulta, como `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`, em que `&ef_id=abcde:123456789:s` é o símbolo de acréscimo, a chave `ef_id` e o valor `ef_id`. Para incluir uma ef_id, as contas e campanhas relevantes da rede de publicidade devem ter [!UICONTROL Tracking Type] &quot;[!UICONTROL EF Redirect]&quot; e [!UICONTROL Redirect Type] &quot;[!UICONTROL Token].&quot;

Para contas e campanhas existentes, a ef_id provavelmente já está implementada.

Se a ef_id não for incluída, peça ajuda à sua equipe de conta do Adobe.

Quando todos os pré-requisitos forem concluídos, o `ef_id` será usado como chave primária para transmitir dados do [!DNL Google Analytics] para o Search, Social e Commerce.

## Pré-requisito 2: Capturar o token de Pesquisa, Social e Commerce (parâmetro de sequência de consulta &quot;ef_id&quot;) em uma dimensão personalizada para cada propriedade [!DNL Google Analytics] relevante

Repita as seguintes tarefas para cada combinação de conta e propriedade do [!DNL Google Analytics] para a qual deseja sincronizar dados. Consulte [[!DNL Google Analytics] documentação sobre como criar e implementar dimensões personalizadas](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) para obter ajuda com essas tarefas.

1. Em [!DNL Google Analytics], crie uma dimensão personalizada com o nome &quot;`ef_id`&quot;. Defina o escopo da dimensão como [!DNL User] e defina a dimensão como ativa.

   >[!NOTE]
   >
   >Este pré-requisito requer a permissão de edição para as propriedades relevantes.

1. Atualize o código de rastreamento [!DNL Google Analytics] para capturar o valor do parâmetro de cadeia de caracteres de consulta ef_id quando ele estiver presente na URL da página de aterrissagem e armazená-lo na dimensão personalizada ef_id.

   >[!NOTE]
   >
   >O ef_id deve estar somente nos URLs da página inicial.

   Por exemplo, se a URL da página de aterrissagem for `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`, o valor da dimensão ef_id em [!DNL Google Analytics] será `abcde:123456789:s`.

   >[!NOTE]
   >
   >Esse pré-requisito deve ser preenchido por um desenvolvedor qualificado.

>[!MORELIKETHIS]
>
>* [Sobre a sincronização [!DNL Google Analytics] de métricas de conversão](data-source-about.md)
>* [Configurar uma  [!DNL Google Analytics] exibição como fonte de dados](data-source-configure.md)
>* [Editar uma [!DNL Google Analytics] fonte de dados](data-source-edit.md)
>* [Pausar sincronização de uma fonte de dados](data-source-pause.md)
>* [Reautenticar uma [!DNL Google Analytics] fonte de dados](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] configurações da fonte de dados](data-source-settings.md)
>* [Apêndice - Disponível [!DNL Google Analytics] métricas](data-source-ga-metrics.md)
