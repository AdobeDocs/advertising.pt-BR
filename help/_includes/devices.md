---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---
# Campo Dispositivos nas configurações de campanhas e grupos de anúncios GL e MS

**[!UICONTROL Devices]:** (Opcional; não disponível para [!DNL Google Ads] desempenho máximo de campanhas) Configure ajustes de oferta para diferentes tipos de dispositivos, como porcentagens da oferta de nível de palavra-chave. Por exemplo, se a oferta no nível da palavra-chave for de 1 USD e o ajuste de oferta para smartphones for de 50%, a oferta do smartphone será de 1,50 USD. Por padrão, nenhum valor é inserido (ajuste de oferta=0), e todos os dispositivos são oferecidos no lance de nível de palavra-chave.

Para Google Ads, as porcentagens válidas podem incluir -100 para smartphones e tablets (para não licitar o tipo de dispositivo) e de -90 a 900 para todos os tipos de dispositivos.

Para a Microsoft Advertising, as porcentagens válidas podem incluir:

* Smartphones e tablets: -100 (para não licitar o tipo de dispositivo) e de -90 a 900
* Desktop: de 0 a 900

>[!NOTE]
>* As configurações no nível do grupo de anúncios substituem as configurações no nível da campanha. No entanto, se você excluir um dispositivo no nível da campanha, não será possível substituir a exclusão no nível do grupo de anúncios.
>* Se você atribuir essa campanha a um portfólio otimizado padrão, Search, Social e Commerce determinarão automaticamente o lance base no nível de palavra-chave para ajudar o portfólio a atingir seu objetivo. A rede de publicidade ajusta a oferta conforme especificado para diferentes tipos de dispositivos.
>* (Para todos os grupos de campanhas/anúncios, exceto para [!DNL Microsoft Advertising] grupos de publicidade na rede de público-alvo) Se você atribuir essa campanha a um portfólio otimizado padrão que esteja configurado como &quot;[!UICONTROL Auto-optimize Bid Adjustment Values],&quot; em seguida, o recurso de otimização altera os ajustes de oferta do dispositivo especificado no nível do grupo de anúncios, desde que o valor ideal calculado esteja dentro dos valores mínimo e máximo especificados nas configurações do portfólio e o grupo de anúncios não exclua a licitação para o tipo de dispositivo.

