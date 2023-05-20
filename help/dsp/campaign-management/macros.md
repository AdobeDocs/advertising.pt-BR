---
title: Publicidade de macros DSP
description: Consulte as macros disponíveis para rastreamento geral e para rastrear cliques em anúncios de exibição de terceiros.
feature: DSP Ads
exl-id: 7058c988-c544-4a61-84dd-eec4ce88ceba
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# Publicidade de macros DSP

Uma macro é um comando curto ou abreviação para uma instrução e geralmente segue o formato `${MACRO_NAME}`. As macros incluídas no código criativo ou URLs de click-through se expandem em uma string de código mais longa que o servidor de publicidade pode entender. O servidor de anúncios DSP executa macros quando o anúncio é veiculado ou clicado.

As macros do servidor de anúncios são úteis para transmitir informações importantes ao DSP ou a servidores de anúncios de terceiros. As macros são usadas com mais frequência durante o tráfico de código criativo ou metadados de terceiros e personalizados (como pixels de terceiros).

É possível inserir manualmente uma macro em qualquer lugar, como em uma tag VAST, em qualquer URL ou em um pixel de evento do DSP ou de terceiros. No entanto, cada cliente e parceiro do DSP tem um formato de tag de anúncio diferente, e as macros devem ser inseridas em pontos diferentes na tag de acordo. Cada vez que trabalhar com um novo cliente ou parceiro, peça a ele documentação sobre onde inserir as macros em suas tags de anúncio que o DSP trafica.

## Macros de rastreamento gerais

Use macros de rastreamento geral em todos os tipos de anúncios e tags para transmitir dados específicos, conforme necessário.

| Macro | Descrição de Substituição | Tipo |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | A ID da conta. | inteiro |
| `${TM_AD_ID}` | A chave do anúncio (adKey). | string |
| `${TM_AD_ID_NUM}` | A ID do anúncio. | inteiro |
| `${TM_ADVERTISER_ID}` | A ID do anunciante. | inteiro |
| `${TM_CAMPAIGN_ID}` | A chave da campanha. | string |
| `${TM_CAMPAIGN_ID_NUM}` | A ID da campanha. | inteiro |
| ` ${TM_CLICK_URL}` | O URL de redirecionamento, que permite aos servidores de publicidade rastrear e contar cliques de publicidade. Quando o anúncio é veiculado, se o usuário clicar nele, a macro é ativada e o clique é registrado e contado para fins de relatório. | string |
| ` ${TM_CLICK_URL_URLENC}` | O URL de redirecionamento codificado, que permite aos servidores de publicidade rastrear e contar cliques de anúncios. Quando o anúncio é veiculado, se o usuário clicar nele, a macro é ativada e o clique é registrado e contado para fins de relatório. Não use essa macro, a menos que você esteja criando anúncios de terceiros e seu fornecedor exija codificação de URL. | string |
| `${TM_FEED_ID}` | A chave para o posicionamento de mídia (feedKey). | string |
| `${TM_FEED_ID_NUM}` | A ID para o posicionamento de mídia. | inteiro |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | A chave do site para o posicionamento. Obrigatório para [!DNL AppsFlyer] rastreadores de cliques para anúncios de instalação de aplicativos móveis.<!-- should map to placement_site_key column of placement_site table --> | string |
| `${TM_PLACEMENT_ID}` | A chave de posicionamento (cpKey). | string |
| `${TM_PLACEMENT_ID_NUM}` | A ID de posicionamento. | inteiro |
| `${TM_RANDOM}` | Cache Buster: um número aleatório entre 1 e 1000000. | long |
| `${TM_SESSION_ID}` | A ID da sessão, que corresponde a uma única recuperação da tag de anúncio. | string |
| `${TM_SITE_DOMAIN_URLENC}` | O subdomínio da página analisado do URL na solicitação de oferta; codificado em URL. Não compatível com anúncios em banner, click-to-play. | string |
| ` ${TM_SITE_NAME}` | O nome do site para o posicionamento. | string |
| `${TM_SITE_URL_URLENC}` | O URL transmitido na solicitação de oferta; codificado no URL. Não compatível com anúncios em banner, click-to-play. | string |
| `${TM_SITE_ID_NUM}` | A ID do site para o posicionamento. | inteiro |
| `${TM_TIMESTAMP}` | O carimbo de data e hora Unix indicando o número de segundos decorridos desde a meia-noite (00:00 UTC) de 1º de janeiro de 1970. | long |
| ` ${TM_VIDEO_DURATION}` | A duração do vídeo do anúncio em segundos. | inteiro |

{style="table-layout:auto"}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## Macros específicas para dispositivos móveis

| Macro | Descrição de Substituição | Tipo |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore]) A ID da plataforma, que corresponde ao sistema operacional do dispositivo:<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` quando a plataforma não for nenhuma das opções acima</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore]) O nome do modelo do dispositivo, codificado em URL. | string |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore]) O ambiente em que o anúncio foi veiculado:<ul><li>`a` = aplicativo móvel</li><li>`b` = site móvel</li></ul> | sequência de caracteres (`a` ou `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen]) A ID da plataforma, que corresponde ao sistema operacional do dispositivo:<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` quando a plataforma não for nenhuma das opções acima</li></ul> | string |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen]) O tipo de dispositivo no qual o anúncio foi visualizado:<ul><li>`TAB` = tablet</li><li>`PHN` = dispositivo móvel</li><li>`computer` = computador</li></ul> | string |
| `${UOO}` | ([!DNL Nielsen]) Se o usuário desativou ou não o rastreamento de anúncios:<ul><li>`1` (sinalizador DNT = 1) = o usuário recusou o rastreamento de anúncios</li><li>`0` (sinalizador DNT = 0) = o usuário optou por participar do rastreamento de anúncios</li></ul> | inteiro (`0` ou `1`) |
| `${TM_BUNDLE}` | A variável [!DNL iOS] ou [!DNL Android] ID do pacote da app store. Exemplos: com.zynga.wwf2.free ou id804379658 | string |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` indica se o licitante determina que a solicitação de oferta é proveniente da origem da União Europeia e requer a aplicação do GDPR:<ul><li>`1` = O GDPR deve ser aplicado</li><li>`0` = O GDPR não deve ser aplicado</li></ul>`gdpr_consent=${GDPR_CONSENT}` é o valor de consentimento transmitido pelo parceiro de fornecimento na solicitação de oferta de entrada:<ul><li>Na maioria dos casos, é uma string de consentimento codificada em base64url ou daisybit (exemplo: BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMgBkIDIgM0AgOJxAnQA)</li><li>`0` = sem consentimento</li><li>`1` = consentimento</li></ul> | daisybit ou inteiro |

{style="table-layout:auto"}

## Clique em Macros para anúncios de exibição de terceiros

Para rastrear com precisão os cliques de anúncios usando tags de exibição de terceiros, o DSP exige uma macro de clique de exibição. Somente uma versão da macro é necessária; a macro relevante depende do tipo de tag.

| Macro | Descrição de Substituição | Tipo |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | O URL de redirecionamento que permite que os servidores de publicidade rastreiem e contem cliques de anúncios na plataforma. | string |
| `${TM_CLICK_URL_URLENC}` | O URL de redirecionamento que habilita os servidores de publicidade que exigem codificação de URL para rastrear e contar cliques de publicidade na plataforma. | string |

{style="table-layout:auto"}

O DSP insere automaticamente macros de clique de exibição em uma tag de exibição de terceiros ao:

* Exportar tags de publicidade de um parceiro de servidor de publicidade <!-- [Needs PM confirmation.] -->
* Upload em massa [!DNL Flashtalking] ou [!DNL Google DoubleClick for Advertisers] adicionar tags diretamente no DSP

Se uma macro de clique estiver ausente ao criar um anúncio de exibição, o DSP exibirá uma mensagem de aviso solicitando que você insira manualmente a macro de clique de exibição apropriada na área correta da tag.

## Solução de problemas de erros de macro

Ao adicionar macros ao código, certifique-se de usar a sintaxe exata da macro. Ao validar as macros, o DSP verifica se a macro corresponde exatamente a uma das macros válidas.

Erros são gerados se houver caracteres ausentes no início ou no fim do nome da macro. Por exemplo, você verá uma mensagem de erro se:

* Você esquece um ou mais caracteres no início do nome da macro, como `${`. Se você não incluir a sintaxe completa, a entrada não será reconhecida como uma macro válida.
* A macro não termina com um conjunto válido de caracteres, como `}`.

>[!MORELIKETHIS]
>
>* [Configurações do anúncio de áudio](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Configurações do Anúncio de TV Conectado](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Configurações do anúncio de exibição](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Configurações do anúncio móvel](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Configurações do anúncio nativo](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Configurações do anúncio antes da exibição](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [Configurações de Anúncio de Vídeo Universal](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)

