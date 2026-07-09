---
title: Macros disponíveis para rastrear URLs
description: Referencie as macros que você pode adicionar aos URLs da sua página inicial, URLs de rastreamento e criações de terceiros.
feature: Creative Experiences, Creative Experiences
exl-id: d0cbbb21-467d-4ed1-bc6e-ded1b045b98b
TQID: https://experienceleague.adobe.com/J5jfIECrL29NngVOulEgHKZBHYqBmoz4680HzEzhIng
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 3c3bffe0c28bb24c0df9385f9cc91be1376a66d2
workflow-type: tm+mt
source-wordcount: 319
ht-degree: 0%

---

# Macros disponíveis para rastrear URLs

<!-- More feature metadata???  -->

Você pode incluir qualquer uma das seguintes macros em seus criativos de terceiros, em URLs de rastreamento de terceiros para suas experiências e em URLs de páginas de aterrissagem para seu próprio uso.

Algumas macros disponíveis, ou suas equivalentes, são incluídas automaticamente nas tags de experiência.

<!--
 Later: 

| Macro | Description | Automatically in experience tags for Advertising DSP? | Automatically in experience tags for [!DNL Google Campaign Manager 360]? |
| --- | --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Tracks and reports the campaign ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ebuy!` |
| `${TM_SITE_ID_NUM}` | Tracks and reports the site ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%esid!` |
| `${TM_PLACEMENT_ID_NUM}` | Tracks and reports the placement ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%epid!` |
| `${TM_AD_ID_NUM}` | Tracks and reports the ad ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%eaid!` |
| `${TM_CREATIVE_ID_NUM}` | Tracks and reports the creative ID from the DSP | N/A | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ecid!` |
| `${TM_SESSION_ID}` | Tracks and reports the impression ID from the DSP. If a value isn't returned, Advertising Creative generates one. | Yes | &mdash; |
| `${TM_ACC_EXPERIENCE_ID}` | Tracks and reports the Advertising Creative experience ID | &mdash; | &mdash; |
| `${TM_ACC_CREATIVE_ID}` | Tracks and reports the Advertising Creative creative ID | &mdash; | &mdash; |
| `${TM_RANDOM}` | A random number between 1 and 1000000 | &mdash; | &mdash; |
| `${TM_TIMESTAMP}` | The Unix Timestamp (in seconds) | &mdash; | &mdash; |
| `${TM_CLICK_URL_URLENC}` | (For third-party ads from vendors who require URL encoding) The encoded click redirect URL, which enables ad servers to track and count ad clicks. When the ad is served and the user clicks on it, the macro is activated, and the click is recorded and counted for reporting purposes. | Yes | &mdash; |
| `${TC_1}` | Custom tracking code 1. | &mdash; | &mdash; |
| `${TC_2}` | Custom tracking code 2. | &mdash; | &mdash; |
| `${TC_3}` | Custom tracking code 3. | &mdash; | &mdash; |
| `${TC_4}` | Custom tracking code 4. | &mdash; | &mdash; |
| `${TC_5}` | Custom tracking code 5. | &mdash; | &mdash; |
| `${GDPR_ENFORCED}` | Whether GDPR enforcement is required for the bid request. Values: **1** = GDPR should be enforced, **0** = GDPR should not be enforced. | &mdash; | &mdash; |
| `${GDPR_CONSENT}` | The GDPR consent value received from the supply partner in the bid request. Typically: **1** = consent provided, **0** = no consent provided. | &mdash; | &mdash; |
-->

| Macro | Descrição | Automaticamente nas tags de experiência do Advertising DSP? |
| --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Rastreia e relata a ID da campanha na DSP | Sim |
| `${TM_SITE_ID_NUM}` | Rastreia e relata a ID do site da DSP | Sim |
| `${TM_PLACEMENT_ID_NUM}` | Rastreia e relata a ID de posicionamento da DSP | Sim |
| `${TM_AD_ID_NUM}` | Rastreia e relata a ID do anúncio da DSP | Sim |
| `${TM_CREATIVE_ID_NUM}` | Rastreia e relata a ID de criação da DSP | N/D |
| `${TM_SESSION_ID}` | Rastreia e relata a ID de sessão associada à solicitação de anúncio. Se um valor não for retornado, o Advertising Creative gera um. | Sim |
| `${TM_ACC_EXPERIENCE_ID}` | Rastreia e relata a ID de experiência do Advertising Creative | — |
| `${TM_ACC_CREATIVE_ID}` | Rastreia e relata a ID de criação da Advertising Creative | — |
| `${TM_RANDOM}` | Um número gerado aleatoriamente entre 1 e 1.000.000. Geralmente usado para eliminação de cache. | — |
| `${TM_TIMESTAMP}` | O timestamp UNIX® (em segundos) | — |
| `${TM_CLICK_URL_URLENC}` | (Para anúncios de terceiros de fornecedores que exigem codificação de URL) O URL de redirecionamento de clique codificado, que permite que os servidores de publicidade rastreiem e contem cliques de anúncios. Quando um usuário clica no anúncio, a macro é ativada e o clique é registrado e contado para fins de relatório. | Sim |
| `${TC_1}` | Código de rastreamento personalizado 1. | — |
| `${TC_2}` | Código de rastreamento personalizado 2. | — |
| `${TC_3}` | Código de rastreamento personalizado 3. | — |
| `${TC_4}` | Código de rastreamento personalizado 4. | — |
| `${TC_5}` | Código de rastreamento personalizado 5. | — |
| `${GDPR_ENFORCED}` | Se a aplicação do GDPR é necessária para a solicitação de oferta. Valores: **1** = O GDPR deve ser aplicado, **0** = O GDPR não deve ser aplicado. | — |
| `${GDPR_CONSENT}` | O valor de consentimento do GDPR recebido do parceiro de fornecimento na solicitação de oferta. Normalmente: **1** = consentimento fornecido, **0** = nenhum consentimento fornecido. | — |

>[!MORELIKETHIS]
>
>* [Adicionar criações padrão a uma biblioteca criativa](/help/creative/creative-libraries/creative-add-standard.md#creative-add-third-party)
>* [Configurações de criação padrão](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party)
>* &lbrack;Configurações de experiência direcionadas*[Configurações de experiência não direcionadas](/help/creative/experiences/experience-settings-no-targeting.md)
