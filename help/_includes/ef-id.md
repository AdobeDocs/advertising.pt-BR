---
source-git-commit: dede10acca1540a10699be3c14564a6f9360edd2
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---
# IDs EF do Adobe Advertising

## IDs EF do Adobe Advertising

A ID de EF é um token exclusivo que o Adobe Advertising usa para associar a atividade a um clique ou exposição de anúncios online em um navegador ou dispositivo individual. As EF IDs atuam principalmente como chaves para enviar dados do [!DNL Analytics] e dados do Customer Journey Analytics para a Adobe Advertising para otimização de relatórios e ofertas no Adobe Advertising.

Para [!DNL Analytics], a ID EF é armazenada em [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou [!DNL rVar] (reservada [!DNL eVar]) dimensão (ID EF Adobe Advertising).

Para o Customer Journey Analytics, a ID EF é armazenada na propriedade `trackingIdentities` do objeto `conversionDetails`, que faz parte do [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension].

### Formatos de ID EF {#ef-id-formats}

>[!NOTE]
>
>EF IDs fazem distinção entre maiúsculas e minúsculas. Se uma implementação do [!DNL Analytics] ou do Customer Journey Analytics forçar o rastreamento de URL em minúsculas, o Adobe Advertising não reconhecerá a EF ID. Isso afeta os lances e os relatórios da Adobe Advertising, mas não afeta os relatórios do Adobe Advertising no [!DNL Analytics] ou na Customer Journey Analytics.

#### [!DNL Google Ads] anúncios de pesquisa

```
{gclid}:G:s
```

em que:

* `gclid` é o [!DNL Google Click ID] (GCLID).
* `s` é o tipo de rede (s para pesquisa).

#### [!DNL Microsoft Advertising] anúncios de pesquisa

```
{msclkid}:G:s
```

em que:

* `msclkid` é o [!DNL Microsoft Click ID] (MSCLKID).
* `s` é o tipo de rede (s para pesquisa).

#### Exibir anúncios e anúncios de pesquisa em outros mecanismos de pesquisa

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

em que:

* &lt;*ID de visitante do Adobe Advertising*> é um identificador exclusivo por visitante (como UhKVaAAABCkJ0mDt). Também chamado de *ID do surfer*.

* &lt;*carimbo de data/hora*> é a hora no formato AAAAMMDDHHMMSS (como 20190821192533 para Ano 2019, Mês 08, Dia 21, Hora 19:25:33).

* &lt;*tipo de canal*> é o tipo de canal responsável pelo clique ou exposição:

   * `d` para um clique em um anúncio de exibição do DSP (click-through de exibição)
   * `i` para obter uma impressão de um anúncio de exibição do DSP (view-through)
   * `s` para um clique em um anúncio de Pesquisa (click-through de pesquisa).

Exemplo `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`
