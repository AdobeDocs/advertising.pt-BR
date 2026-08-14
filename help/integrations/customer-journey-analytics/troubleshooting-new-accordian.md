---
title: Solução de problemas de dados do Adobe Advertising no Customer Journey Analytics
description: Saiba como solucionar e resolver problemas de dados do Adobe Advertising no Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
hide: true
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 21280b9826b60e69d9f4829062db1b140aba5c88
workflow-type: tm+mt
source-wordcount: 3204
ht-degree: 0%

---

# Solução de problemas de dados do Adobe Advertising no Customer Journey Analytics

A seguir estão possíveis problemas, suas possíveis causas e soluções.

## Lista de todos os sintomas em potencial

| Problema | Mais informações |
| ------- | ---------------- |
| Nenhuma chamada alloy() está visível na guia Rede do navegador | Consulte a seção &quot;[Problemas de instalação e instalação](#issues-installation-setup)&quot; > &quot;[A extensão WebSDK não inicializa](#websdk-extension-doesn't-initialize)&quot; |
| Erro do console: liga não definida | Consulte &quot;[Problemas de instalação e configuração](#issues-installation-setup)&quot; > &quot;[A extensão WebSDK não inicializa](#websdk-extension-doesn't-initialize)&quot; |
| Não há solicitações de interação ou coleta para edge.adobedc.net | Consulte &quot;[Problemas de instalação e configuração](#issues-installation-setup)&quot; > &quot;[A extensão WebSDK não inicializa](#websdk-extension-doesn't-initialize)&quot; |
| As solicitações atingem a borda, mas retornam erros 400 ou 500 | Consulte a seção &quot;[Problemas de instalação e instalação](#issues-installation-setup)&quot; > &quot;[Sequência de dados não configurada ou configurada incorretamente](#datastream-not-configured-or-misconfigured)&quot; |
| Nenhum dado é exibido nos relatórios do Adobe Analytics ou Adobe Advertising | Consulte a seção &quot;[Problemas de instalação e instalação](#issues-installation-setup)&quot; > &quot;[Sequência de dados não configurada ou configurada incorretamente](#datastream-not-configured-or-misconfigured)&quot; |
| Erro na resposta da rede: &quot;sequência de dados não encontrada&quot; | Consulte a seção &quot;[Problemas de instalação e instalação](#issues-installation-setup)&quot; > &quot;[Sequência de dados não configurada ou configurada incorretamente](#datastream-not-configured-or-misconfigured)&quot; |
| Nenhuma conversão de view-through ou click-through é registrada para a página da Web | Consulte a seção &quot;[problemas de configuração de extensão do Advertising](#advertising-extension-setup-issues)&quot; |
| `_experience.adcloud` está ausente na carga do Experience Data Model (XDM) para click-throughs | Consulte a seção &quot;[problemas de configuração de extensão do Advertising](#advertising-extension-setup-issues)&quot; |
| As conversões são confirmadas em uma ferramenta de depuração, mas não aparecem nos relatórios do Adobe Advertising | Consulte a seção &quot;[problemas de configuração de extensão do Advertising](#advertising-extension-setup-issues)&quot; |
| A ID de visitante muda entre páginas | Consulte a seção &quot;[Problemas de identidade e ECID](#identity-and-ecid-issues)&quot; |
| Os segmentos de público-alvo do Advertising não correspondem | Consulte a seção &quot;[Problemas de identidade e ECID](#identity-and-ecid-issues)&quot; |
| O depurador mostra que as condições da regra não são atendidas | Consulte a seção &quot;[Regras ou eventos não estão sendo acionados](#rules-or-events-aren't-firing)&quot; |
| A ação [!UICONTROL Send Event] nunca é executada | Consulte a seção &quot;[Regras ou eventos não estão sendo acionados](#rules-or-events-aren't-firing)&quot; |
| As alterações feitas em [!DNL Tags] não são refletidas no site ativo | Consulte a seção &quot;[Problemas de compilação e publicação da biblioteca](#library-build-and-publishing-issues)&quot; |
| Uma atualização de extensão foi aplicada, mas o comportamento antigo persiste | Consulte a seção &quot;[Problemas de compilação e publicação da biblioteca](#library-build-and-publishing-issues)&quot; |
| A chamada de evento de envio `alloy()` foi bem-sucedida (com uma resposta 200), mas os dados de conversão do Adobe Advertising estão ausentes nos relatórios | Consulte a seção &quot;[Problemas de validação de esquema para campos Advertising](#schema-validation-for-advertising-fields)&quot; |
| A carga XDM no depurador não mostra nenhum objeto `_experience.adcloud` | Consulte a seção &quot;[Problemas de validação de esquema para campos Advertising](#schema-validation-for-advertising-fields)&quot; |
| Nenhum dado de relatório de resumo está disponível no Customer Journey Analytics para Advertising DSP ou Advertising Search, Social e Commerce. | Consulte a seção &quot;[Relatórios de problemas](#reporting-issues)&quot; > &quot;[Relatórios de resumo](#summary-reporting)&quot; |
| Os dados de relatórios de resumo estão disponíveis no Customer Journey Analytics para o Anunciante 1, mas não para o Anunciante 2. | Consulte a seção &quot;[Relatórios de problemas](#reporting-issues)&quot; > &quot;[Relatórios de resumo](#summary-reporting)&quot; |
| (Usuários do Search, Social e Commerce) Os dados de relatórios de resumo estão disponíveis no Customer Journey Analytics para uma conta do [!DNL Google Ads], [!DNL Meta Ads] ou [!DNL Microsoft Advertising], mas não para outra conta. | Consulte a seção &quot;[Relatórios de problemas](#reporting-issues)&quot; > &quot;[Relatórios de resumo](#summary-reporting)&quot; |
| Os dados de relatórios de resumo no Customer Journey Analytics Workspace são diferentes dos dados no Advertising DSP ou Advertising Search, Social e Commerce, ou os dados de resumo estão ausentes em algumas campanhas e entidades de campanha. | Consulte a seção &quot;[Relatórios de problemas](#reporting-issues)&quot; > &quot;[Relatórios de resumo](#summary-reporting)&quot; |
| Os dados de conversão (como `Page Views`) não estão disponíveis para uma dimensão de relatório (como `Campaign`) no CJA Customer Journey Analytics Workspace. | Consulte a seção &quot;[Relatórios de problemas](#reporting-issues)&quot; > &quot;[Relatórios de nível de evento](#event-level-reporting)&quot; |

## Problemas de instalação e configuração {#issues-installation-setup}

### A extensão WebSDK não inicializa {#websdk-extension-doesn&#39;t-initialize}

#### Problemas:

* Nenhuma chamada alloy() está visível na guia Rede do navegador
* Erro do console: liga não definida
* Não há solicitações de interação ou coleta para edge.adobedc.net

#### Possíveis causas e verificação/resolução

+++ Biblioteca não publicada ou em estado de rascunho

Vá para [Fluxo de Publicação](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) e verifique se a biblioteca que contém a extensão WebSDK está no estado aprovado/publicado.

+++

+++ O código de inserção está ausente ou no ambiente incorreto

Verifique se o código de inserção do [!DNL Tags] na página da Web faz referência ao ambiente correto (Dev/Stage/Prod). Procure o ambiente na tag `<head>` para a tag de script `//assets.adobedtm.com/...`.

+++

+++ Conflito de carga assíncrono vs. síncrono

Verifique se apenas um código de inserção [!DNL Tags] está presente por página da Web. Códigos incorporados duplicados causam condições de corrida.

+++

+++ Bloqueio da política de segurança de conteúdo (CSP)

Adicione `edge.adobedc.net` e `assets.adobedtm.com` à sua CSP `connect-src` e `script-src` diretivas.

+++

### Sequência de dados não configurada ou configurada incorretamente {#datastream-not-configured-or-misconfigured}

#### Problemas:

* As solicitações atingem a borda, mas retornam erros 400 ou 500
* Nenhum dado é exibido nos relatórios do Adobe Analytics ou do Adobe Advertising<!-- It's not useful to organize this info by cause, not symptom -->
* Erro na resposta da rede: &quot;sequência de dados não encontrada&quot;

#### Possíveis causas e verificação/resolução

+++ A ID da sequência de dados da propriedade de tag está ausente ou incorreta

1. Em [!DNL Tags], abra as [configurações da sequência de dados](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams) para sua propriedade de marca.
1. Confirme se o campo [!UICONTROL Datastream] aponta para o fluxo de dados correto para cada ambiente (desenvolvimento, preparo e produção), bem como para o esquema e o conjunto de dados corretos.

   Cada ambiente deve ter seu próprio fluxo de dados, a menos que você compartilhe explicitamente um fluxo de dados em todos os três ambientes.

+++

+++ Os serviços de sequência de dados não estão habilitados para a propriedade de tag

[Abra as configurações da sequência de dados](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) e verifique se os seguintes serviços estão habilitados:

* Adobe Advertising (para conversão/sincronização de público)
* Adobe Experience Platform (para assimilação de perfil)

+++

+++ Incompatibilidade de sandbox

Verifique se o fluxo de dados pertence à mesma sandbox da Adobe Experience Platform que o esquema e o conjunto de dados. Um erro comum é criar um fluxo de dados na sandbox de produção, mas apontar esquemas para a sandbox de desenvolvimento.

+++

### [!UICONTROL Advertising] problemas de configuração de extensão {#advertising-extension-setup-issues}

#### Problemas:

* Nenhuma conversão de view-through ou click-through é registrada para a página da Web.

  Para verificar se as conversões são registradas:

  1. Abra a página da Web com `ef_id=test&s_kwcid=test` anexada à URL.
  1. Abra a ferramenta de inspeção de código do seu navegador (geralmente chamada de [!DNL Inspect]), abra a guia [!DNL Network] e procure uma chamada interativa para event_type=&quot;advertising.enrichment_ct&quot; no Adobe Experience Platform.
  1. Na interface da Coleção de Dados, [abra a definição de esquema](https://experienceleague.adobe.com/en/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas) para os dados de site que deseja coletar e confirme se `xdm->_experience->adcloud->conversionDetails->trackingCode` e `trackingIdentities` contêm `ef_id` e `s_kwcid`.

* `_experience.adcloud` está ausente na carga do Experience Data Model (XDM) para click-throughs.

* As conversões são confirmadas em uma ferramenta de depuração, mas não aparecem nos relatórios do Adobe Advertising

#### Possíveis causas e verificação/resolução

+++ O serviço `Adobe Advertising` não está habilitado para a sequência de dados

1. Em [!DNL Tags], abra as [configurações da sequência de dados](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams) para sua propriedade de marca.
1. Ative os seguintes serviços e salve as configurações:
   * Adobe Advertising (para conversão/sincronização de público)
   * Adobe Experience Platform (para assimilação de perfil)

+++

+++ O componente `Adobe Advertising` não está habilitado para a extensão [!UICONTROL WebSDK]

O componente `Adobe Advertising` na extensão WebSDK está desabilitado por padrão e deve ser habilitado explicitamente antes que qualquer rastreamento de click-throughs ou view-throughs do Adobe Advertising seja funcional, independentemente de como o esquema ou as regras XDM são configurados.

1. Em [!DNL Tags], abra as [opções de compilação da propriedade nas definições de configuração do Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/custom-build-components).
1. Habilite o componente **Advertising** e salve as configurações.
1. Recrie a biblioteca e publique-a novamente.

+++

+++ Somente as conversões click-through são registradas; as conversões view-through nunca aparecem

Esse é o comportamento padrão esperado. Quando o componente `Adobe Advertising` estiver habilitado, o rastreamento de click-through ficará ativo automaticamente usando os parâmetros de consulta de URL `s_kwcid` e `ef_id`. O rastreamento de view-through é desativado por padrão e requer configuração adicional — consulte o próximo item.

+++

+++ O rastreamento de view-through não está habilitado ou configurado

1. Habilite o serviço Adobe Advertising para a sequência de dados:
   1. Vá para [!UICONTROL Data Collection] > [!UICONTROL Datastreams] no Adobe Experience Platform e abra a sequência de dados usada pela propriedade [!DNL Tags].
   1. Selecione **Adicionar Serviço**, **Adobe Advertising** e **Adobe Experience Platform** e **Salvar**.
1. Configurar anunciantes no Adobe Advertising DSP:
   1. Em [!DNL Tags], vá para [!UICONTROL Extensions] > [!UICONTROL Installed] > **Adobe Experience Platform Web SDK** > [!UICONTROL Configure].
   1. Na seção [!UICONTROL Advertiser], selecione um anunciante na lista suspensa e ative-o. Para configurar vários anunciantes, selecione **Adicionar anunciante**.
1. Verifique se os pixels de conversão de view-through estão sendo acionados:
   1. No Depurador [!DNL Adobe Experience Platform], confirme se a chamada de interação inclui `stitchId` no campo `xdm.query`.
   1. Confirme na guia do navegador [!UICONTROL Network] que um evento do tipo `advertising.enrichment` foi acionado e inclui `stitchId` em `xdm.query`.

As conversões de view-through são acionadas somente a cada 30 minutos, independentemente do número de visitas. Se você não vir uma chamada interativa, limpe o cache do navegador e tente novamente.

+++

+++ (Se nenhum evento de view-through for acionado no Experience Platform após a chamada de interação de Viewthrough) O anunciante foi digitado manualmente em vez de selecionado na lista suspensa

Selecione novamente o anunciante na lista suspensa [!UICONTROL Advertiser] em vez de inseri-lo manualmente.

+++

+++ (Se nenhum evento de view-through no Experience Platform depois que a chamada de interação de Viewthrough for acionada) Nenhuma ID de anunciante será enviada com a chamada de interação de view-through

Confirme se um anunciante está configurado e habilitado na seção [!UICONTROL Advertiser] da configuração da extensão WebSDK. Em seguida, recompile e publique a biblioteca.

+++

Antes de abrir um tíquete de suporte para problemas de configuração de extensão do [!UICONTROL Advertising], verifique o seguinte:

* Os serviços **Adobe Advertising** e **Adobe Experience Platform** são adicionados à sequência de dados.
* O componente **Adobe Advertising** está habilitado na configuração da extensão WebSDK.
* A biblioteca foi recriada e republicada após a ativação do componente.
* Para rastreamento de click-through, a URL da página de aterrissagem contém `s_kwcid` e `ef_id` no clique do anúncio.
* Para rastreamento view-through, um anunciante é configurado no Adobe Advertising DSP com a ID correta do anunciante.
* A extensão WebSDK é versão 2.36.0 ou posterior.

## Problemas de identidade e ECID {#identity-and-ecid-issues}

### Problemas:

* A ID de visitante muda entre páginas
* Os segmentos de público-alvo do Advertising não correspondem

### Possíveis causas e verificação/resolução

+++ Cookies de terceiros estão bloqueados

Migre para a coleção de dados CNAME primários configurando um domínio primário na configuração de borda da sequência de dados.

+++

+++ `idMigrationEnabled` está definido como `false` enquanto um cookie `s_ecid` herdado está presente

Defina `idMigrationEnabled: true` na configuração base do SDK da Web para migrar a ECID existente dos cookies `s_ecid` ou `AMCV_`.

+++

### Regras ou eventos não estão sendo acionados {#rules-or-events-aren&#39;t-trigger}

#### Problemas:

* O depurador mostra que as condições da regra não são atendidas
* A ação [!UICONTROL Send Event] nunca é executada

#### Verificação e resolução

+++ Verifique o seguinte:

* A regra é salva e incluída na build da biblioteca ativa.
* O tipo de evento corresponde ao comportamento real da página (como [!UICONTROL Library Loaded] vs. [!UICONTROL DOM Ready] vs. [!UICONTROL Window Loaded]).
* As condições da regra não são muito restritivas. Faça o teste removendo temporariamente as condições para isolar o problema.
* A ordem da regra está correta. Se várias regras compartilharem o mesmo evento, verifique a ordenação da regra.
* Nenhum erro do JavaScript exibido anteriormente na página está interrompendo a execução. Verifique se há exceções não detectadas no console do navegador.

+++

### Problemas de build e publicação da biblioteca {#library-build-and-publishing-issues}

#### Problemas:

* As alterações feitas em [!DNL Tags] não são refletidas no site ativo
* Uma atualização de extensão foi aplicada, mas o comportamento antigo persiste

#### Possíveis causas e verificação/resolução

+++ As alterações não foram adicionadas a uma biblioteca

Em [!UICONTROL Publishing Flow], confirme se suas alterações foram adicionadas a uma biblioteca no ambiente de desenvolvimento. Vá para [!UICONTROL Libraries], abra a biblioteca de trabalho, selecione **Adicionar todos os recursos alterados** e selecione **Salvar e criar**.

+++

+++ O navegador está armazenando em cache uma biblioteca antiga

Faça uma atualização forçada (Ctrl+Shift+R ou Cmd+Shift+R) ou abra a página em uma janela incógnita/privada. Limpe totalmente o cache do navegador se o problema persistir.

+++

+++ O código incorporado destina-se ao ambiente errado

Confirme se o código de inserção na página é o código de inserção de produção, se você estiver testando o comportamento da produção.

+++

+++ A build da biblioteca falhou silenciosamente

Vá para [!UICONTROL Publishing Flow] e verifique se a biblioteca mostra um estado [!UICONTROL Build Failed]. Abra a biblioteca e revise o log de criação — causas comuns são configurações de regras inválidas ou conflitos de versão de extensão.

+++

### Problemas de validação de esquema para campos do Advertising {#schema-validation-for-advertising-fields}

#### Problemas:

* A chamada de evento de envio `alloy()` foi bem-sucedida (com uma resposta 200), mas os dados de conversão do Adobe Advertising estão ausentes nos relatórios
* A carga XDM no depurador não mostra nenhum objeto `_experience.adcloud`

#### Possíveis causas e verificação/resolução

+++ O grupo de campos [!UICONTROL Advertising] está ausente do esquema

Verifique se o grupo de campos [!UICONTROL Advertising] foi adicionado ao esquema.

1. Vá para Adobe Experience Platform > [!UICONTROL Data Management] > [!UICONTROL Schemas].
1. Abra o esquema usado pelo seu fluxo de dados.
1. No painel [!UICONTROL Field Groups], confirme se a **Extensão completa do ExperienceEvent da Adobe Advertising Cloud** está listada.
1. Se estiver ausente, selecione **Adicionar**, pesquise por **Adobe Advertising Cloud**, selecione **Extensão completa do Adobe Advertising Cloud ExperienceEvent** e salve as configurações.

>[!NOTE]
>A republicação da biblioteca [!DNL Tags] não é necessária somente para alterações de esquema, mas você deve remapear o elemento de dados XDM em [!DNL Tags] se novos campos forem adicionados.

+++

+++ Os campos obrigatórios do Adobe Advertising estão ausentes no esquema.

Verifique se os campos obrigatórios do Adobe Advertising estão presentes no esquema em `_experience.adcloud.conversionDetails`.

| Caminho do campo | Tipo | Descrição |
| ----- | --- | --- |
| `_experience.adcloud.conversionDetails.trackingCode` | String | Mapeia a conversão para o clique de anúncio de origem. Preenchido a partir do parâmetro de consulta `s_kwcid` na URL da página de aterrissagem. |
| `_experience.adcloud.conversionDetails.trackingIdentity` | String | Armazena a identidade exclusiva e outros detalhes do evento de conversão de view-through ou click-through rastreado. Preenchido a partir do parâmetro de consulta `ef_id` na URL da página de aterrissagem. |

Se um dos campos estiver ausente, confirme se o grupo de campos **Extensão completa do Adobe Advertising Cloud ExperienceEvent** foi salvo no esquema e atualize o editor de esquema.

+++

+++ O URL da página de aterrissagem não inclui os parâmetros de consulta necessários.

Certifique-se de que o URL da landing page inclua os parâmetros de consulta necessários. Em um click-through de anúncio, a URL da página de aterrissagem deve conter ambos os parâmetros de consulta, por exemplo `https://www.example.com/landing-page?s_kwcid=AL!12345!3!abc123&ef_id=abc123xyz:G:s`

| Parâmetro ausente | Causa provável |
| ----- | --- |
| `s_kwcid` | A marcação automática não está habilitada nas configurações de campanha do Adobe Advertising Search ou do DSP. |
| `ef_id` | O URL da página de aterrissagem não está usando um redirecionamento rastreado pelo Adobe Advertising, ou o acréscimo da ID de EF não está ativado nas configurações da campanha. |

+++

+++ Alguns parâmetros na carga XDM estão ausentes ou vazios.

Para validar a carga XDM de saída, abra o Depurador [!DNL Adobe Experience Platform] ou a guia do navegador [!UICONTROL Network], filtre por `edge.adobedc.net` e inspecione o corpo da solicitação de interação. Uma carga de click-through válida é semelhante ao seguinte:

```json
{
  "events": [{
    "xdm": {
      "eventType": "advertising.clicks",
      "_experience": {
        "adcloud": {
          "conversionDetails": {
            "trackingCode": "AL!12345!3!abc123",
            "trackingIdentity": "abc123xyz:G:s"
          }
        }
      }
    }
  }]
}
```

Se `trackingCode` ou `trackingIdentity` estiverem vazios ou ausentes:

* O parâmetro de consulta não estava presente na página quando a regra foi acionada. Verifique o URL e o tempo de evento da regra.
* O grupo de campos está ausente do esquema. Revise as etapas do esquema acima.

+++

## Problemas de relatório {#reporting-issues}

### Relatório de resumo {#summary-reporting}

#### Problemas e verificação/resolução

+++ Nenhum dado de relatório de resumo está disponível no Customer Journey Analytics para Advertising DSP ou Advertising Search, Social e Commerce.

Verifique o seguinte:

* O Customer Journey Analytics Workspace está referenciando a visualização de dados correta.

* O feed do Adobe Advertising para o Customer Journey Analytics está ativado. Verifique com a equipe de conta da Adobe.

* Sua dimensão/classificação/conjunto de dados de pesquisa da Adobe Advertising e seu conjunto de dados de resumo estão incluídos na conexão com o Customer Journey Analytics.

* Suas dimensões e métricas de resumo do Adobe Advertising estão incluídas na visualização de dados do Customer Journey Analytics.

Se você verificar todas as configurações acima, mas ainda não visualizar os dados de resumo, abra um tíquete de suporte para sua organização em [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support).

+++

+++ Os dados de relatórios de resumo estão disponíveis no Customer Journey Analytics para o Anunciante 1, mas não para o Anunciante 2.

Verifique o seguinte:

* O feed do Adobe Advertising para o Customer Journey Analytics é ativado para o Anunciante 2. Verifique com a equipe de conta da Adobe.

* A configuração &quot;[!UICONTROL Backfill all existing data]&quot; está habilitada para seus três conjuntos de dados (dimensão/classificação/pesquisa, resumo e métricas de evento) na conexão do Customer Journey Analytics.

Se você verificar todas as condições acima, mas ainda não vir os dados de resumo, abra um tíquete de suporte para sua organização em [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support).

+++

+++ (Usuários do Search, Social e Commerce) Os dados de relatórios de resumo estão disponíveis no Customer Journey Analytics para uma conta do [!DNL Google Ads], [!DNL Meta Ads] ou [!DNL Microsoft Advertising], mas não para outra conta.

Verifique se o feed do Adobe Advertising para o Customer Journey Analytics está ativado para a conta de rede de anúncios específica. Verifique com a equipe de conta da Adobe.

Se o feed estiver habilitado para uma conta, mas você ainda não vir os dados de resumo, abra um tíquete de suporte para sua organização em [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support). Inclua o [!UICONTROL Account ID] para a conta de rede de publicidade.

+++

+++ Os dados de relatórios de resumo no Customer Journey Analytics Workspace são diferentes dos dados no Advertising DSP ou Advertising Search, Social e Commerce, ou os dados de resumo estão ausentes em algumas campanhas e entidades de campanha.

Verifique o seguinte:

* Você está usando os mesmos intervalos de datas no [!DNL Workspace] e no relatório do Adobe Advertising.

* Nenhum filtro ou segmento aplicado em [!DNL Workspace] e no relatório do Adobe Advertising está causando diferenças nos dados.

* O [!UICONTROL Time Zone] da sua visualização de dados do Customer Journey Analytics corresponde ao [[!UICONTROL Default Timezone] da sua conta do Advertising DSP](/help/dsp/admin/user-own-profile-edit.md).

* A configuração &quot;[!UICONTROL Backfill all existing data]&quot; está habilitada para seus três conjuntos de dados (dimensão/classificação/pesquisa, resumo e métricas de evento) na conexão do Customer Journey Analytics.

Se tiver certeza de uma discrepância de dados, abra um tíquete de suporte para sua organização em [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support). Inclua o [!UICONTROL Account ID] para a conta de rede de publicidade. Para mostrar evidências da discrepância, inclua capturas de tela e planilhas. Sua equipe de conta da Adobe pode corrigir retroativamente o feed de dados para resolver a discrepância, se necessário.

+++

### Relatórios no nível do evento {#event-level-reporting}

#### Problemas e verificação/resolução

+++ Os dados de conversão (como `Page Views`) não estão disponíveis para uma dimensão de relatório (como `Campaign`) no CJA Customer Journey Analytics Workspace.

Verifique o seguinte, começando pelos itens com menos barreiras de verificação:

* Você está usando a visualização de dados correta.

* As métricas de conversão aplicáveis são eventos da Web/online, que o Adobe Advertising pode atribuir às dimensões.

* O Adobe Advertising está rastreando click-throughs e view-throughs no site aplicável. <!-- Link to validation instructions in the user guide -->

* Na conexão Customer Journey Analytics do conjunto de dados de classificações, os valores das configurações [!DNL Key] e [!DNL Matching Key] estão corretos: [!DNL Key]: `Tracking Code` (_customername.adLens2.trackingCode), [!DNL Matching Key]: `Tracking Code` (event._experience.adcloud.conversionDetails.trackingCode)

* O serviço [!DNL Adobe Advertising] é adicionado à sequência de dados do Adobe Experience Platform, o esquema mapeado para a sequência de dados é `XDM ExperienceEvent Schema` e o grupo de campos `Adobe Advertising Cloud ExperienceEvent Full Extension` é adicionado ao esquema `XDM ExperienceEvent`.

* As configurações do Adobe Advertising são definidas corretamente na extensão WebSDK e publicadas.

Se você verificar todas as configurações acima, mas ainda não visualizar os dados de conversão, abra um tíquete de suporte para sua organização em [https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support). Inclua o [!UICONTROL Account ID] para a conta de rede de publicidade.

+++

<!--

+++ Question

Answer

+++

+++ Question

Answer

+++

+++ Question

Answer

+++

-->

## Ferramentas de validação e depuração

### Adobe Experience Platform Debugger

Instale a extensão [!DNL Adobe Experience Platform Debugger] para [!DNL Chrome]. Ele fornece:

* Uma exibição em tempo real de todas as chamadas `alloy()` do SDK da Web
* Validação do ambiente e da ID da sequência de dados
* Inspeção de carga XDM
* Detalhes de solicitação e resposta do Edge Network

Verificações de chave no depurador:

| Guia | O que verificar |
| ----- | --- |
| [!UICONTROL Summary] | Confirma que o SDK da Web foi detectado e mostra a versão instalada. |
| [!UICONTROL Adobe Experience Platform WebSDK] | Mostra cada evento acionado, a carga XDM completa e a resposta da borda. |
| [!UICONTROL Adobe Advertising] | Confirma a captura da ID do AMO e a chamada de interação XDM com o tipo de evento `advertising.enrichment`. |

### Guia Rede do navegador

Filtrar por `edge.adobedc.net` para inspecionar solicitações de borda bruta:

* URL de solicitação: `https://[org-id].data.adobedc.net/ee/v2/interact`
* Método: `POST`
* Status: `200` (íntegro), `400` (carga inválida) ou `500` (erro de servidor ou de sequência de dados)

Verifique a carga da solicitação para:

* O `dataStreamId` correto
* A presença de um objeto `xdm` com os campos esperados
* Um `identityMap` com a ECID preenchida

### Validação do console

Verifique a versão do WebSDK instalada:

```js
window.alloy.version
```

Acionar manualmente um evento de teste:

```js
alloy("sendEvent", {
  xdm: {
    eventType: "web.webpagedetails.pageViews",
    web: {
      webPageDetails: { name: "Test Page", URL: window.location.href }
    }
  }
}).then(result => console.log("Edge response:", result))
  .catch(err => console.error("Send event error:", err));
```

## Lista de verificação de referência rápida

Verifique o seguinte antes de abrir um tíquete de suporte:

* A extensão WebSDK está na versão mais recente.
* A biblioteca é publicada e o código incorporado está correto para o ambiente.
* A ID da sequência de dados está definida corretamente para desenvolvimento, preparo e produção.
* Todos os serviços de sequência de dados necessários estão habilitados.
* O componente [!UICONTROL Advertising] está habilitado na configuração da extensão WebSDK e uma ID de anunciante do DSP está configurada.
* O esquema XDM inclui o grupo de campos [!UICONTROL Advertising].
* A regra [!UICONTROL Send Event] inclui um mapa de identidade e é acionada no evento correto.
* Nenhuma CSP ou configuração de privacidade do navegador está bloqueando solicitações de borda.
* O Depurador [!DNL Adobe Experience Platform] confirma que os eventos estão atingindo a borda.
* Nenhum erro do JavaScript no console do navegador está interrompendo a execução.
* O grupo de campos **Extensão completa do Adobe Advertising Cloud ExperienceEvent** é adicionado ao esquema.
* `_experience.adcloud.conversionDetails.trackingCode` está presente no esquema.
* `_experience.adcloud.conversionDetails.trackingIdentity` está presente no esquema.
* A URL da página de aterrissagem contém `s_kwcid` e `ef_id` no click-through.
* O Depurador [!DNL Adobe Experience Platform] confirma que `conversionDetails` está preenchido na carga de saída.

## Quando escalonar

Entre em contato com a Equipe de conta da Adobe ou com a equipe de engenharia se:

* As solicitações do Edge retornam erros persistentes de `500` após a validação da sequência de dados.
* [!UICONTROL Advertising] conversões são confirmadas no depurador, mas não aparecem nos relatórios após 24-48 horas.
* Uma atualização de versão do WebSDK apresenta uma regressão que não estava presente na versão anterior. Inclua os números de versão específicos no tíquete de suporte.

>[!MORELIKETHIS]
>
>* [Visão geral](overview.md)
>* [Adobe Advertising IDs usadas por [!DNL Customer Journey Analytics]](ids.md)
>* [Pré-requisitos](prerequisites.md)
>* [Configurar a coleta de dados, a transferência de dados e os relatórios](set-up.md)
>* [Métricas e dimensões do Adobe Advertising no Customer Journey Analytics](advertising-data-in-cja.md)
>* (Usuários do Adobe Analytics) [Coletar dados históricos para IDs AMO e IDs EF para uso no Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
